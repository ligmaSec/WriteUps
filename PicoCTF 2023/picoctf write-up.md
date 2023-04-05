Here are some challenges I found interesting from the 2023 edition of picoCTF

# Binary Exploitation
## Hijacking - 200pts 

###### Description
>Getting root access can allow you to read the flag. Luckily there is a python file that you might like to play with.
Additional details will be available after launching your challenge instance.

the user we are given is in the sudoers file, but he cannot execute most of the programs, except for the vi editor somehow (dunno if it was made on purpose), so you could do `sudo vi /challenge` and select the right file within vi's integrated file browser in order to get the flag

## VNE - 200pts

###### Description
>We've got a binary that can list directories as root, try it out !!

Additional details will be available after launching your challenge instance.
it's a binary that executes ls + the content of an environment variable without sanitizing it so you can just put your payload as is in the environment variable :

```sh
ctf-player@pico-chall$ export SECRET_DIR="-l /challenge/metadata.json | cat /challenge/metadata.json" && ./bin 
Listing the content of -l /challenge/metadata.json | cat /challenge/metadata.json as root: 
{"flag": "picoCTF{flag}", "password": "8a707622"}
```

---
# General skills

## Specialer - 400pts

###### Description
>Reception of Special has been cool to say the least. That's why we made an exclusive version of Special, called Secure Comprehensive Interface for Affecting Linux Empirically Rad, or just 'Specialer'. With Specialer, we really tried to remove the distractions from using a shell. Yes, we took out spell checker because of everybody's complaining. But we think you will be excited about our new, reduced feature set for keeping you focused on what needs it the most. Please start an instance to test your very own copy of Specialer.
Additional details will be available after launching your challenge instance.


I pressed tab to get the available commands autocompletions and got this :

```sh
Specialer$ 
!          bind       compopt    elif       fc         if         printf     shift      true       while
./         break      continue   else       fg         in         pushd      shopt      type       {
:          builtin    coproc     enable     fi         jobs       pwd        source     typeset    }
[          caller     declare    esac       for        kill       read       suspend    ulimit     
[[         case       dirs       eval       function   let        readarray  test       umask      
]]         cd         disown     exec       getopts    local      readonly   then       unalias    
alias      command    do         exit       hash       logout     return     time       unset      
bash       compgen    done       export     help       mapfile    select     times      until      
bg         complete   echo       false      history    popd       set        trap       wait   
```

there were not much useful commands, but I recalled that you could print files using echo as following :
`Specialer$ echo "$(<ala/kazam.txt)"`
result : `return 0 picoCTF{flag}`

---
# Reverse-Engineering

## No way out - 200pts

###### Description
>Put this flag in standard picoCTF format before submitting. If the flag was `h1_1m_7h3_f14g` submit `picoCTF{h1_1m_7h3_f14g}` to the platform. [Windows game](https://artifacts.picoctf.net/c/285/win.zip), [Mac game](https://artifacts.picoctf.net/c/285/mac.app.zip)


This is a unity game, so the language here is C#. I used dnspy to edit the Unity Assembler dll.
The goal is to reach the flag located behind the walls so my first thought was to disable walls collision but didnt succeed, so as a second attempt I decided I could modify the jump value to jump higher than the walls and reach the flag, it worked.
```C#
if(Input.GetButton("Jump") && this.canMove && this.characterController.isGrounded && !this.isClimbing)
{
    this.moveDirection.y = 50f;
}
```

as soon as you reach the giant flag in-game, a prompt with the flag appears

## Ready gladiator 2 - 400pts

###### Description
>Can you make a CoreWars warrior that wins every single round?
Additional details will be available after launching your challenge instance.


During this challenge I discovered some kind of neat hobby (a game actually) that revolves around an assembler-like language, the goal is to build your "warrior" from redcode instructions in order to beat your opponent.

We are presented with an redcode "imp", the simplest codewars warrior yet so hard to beat. After some researches, I found that there is a type of warrior that can beat it, the **gate**. There are many examples available there http://moscova.inria.fr/~doligez/corewar/by-types/idx.htm.
```asm
➜  picoctf nc saturn.picoctf.net 65511 < test.s
Warrior1:
;gate
;name gate
;author ligma
;assert 1
jmp     0,      <-69
end

Rounds: 100
Warrior 1 wins: 100
Warrior 2 wins: 0
Ties: 0
You did it!
picoCTF{flag}
```

the imp in question
```asm
;redcode
;name Imp Ex
;assert 1
mov 0, 1
end
```
