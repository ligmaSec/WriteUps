# General Skills

## SansAlpha - 400 points

Without using letters, we need to print the content of `blargh/flag.txt`.

solution :
calling /bin/base64 binary using wildcards :
`/???/???[!_]64 ??????/????.???`

tip : we're using exclude `[!_]` to exclude "/bin/x86_64" binary, otherwise it would have been only `/???/????64`


# Forensics

## endianness-v2 - 300 points

We are given a supposedly endian-swapped file and we need to find the flag.

When doing a hexdump of the file using xxd, we see the following: \
``00000000: e0ff d8ff 464a 1000 0100 4649 0100 0001  ....FJ....FI....
``
\
which looks familiar, since JPEG's magic bytes look like this : \
``00000000: ffd8 ffe0 0010 4a46 4946 0001 0100 0001  ......JFIF......
``
\
We can see that the bytes are indeed swapped, but instead of 2 bytes being inverted, it's four. 
so ``dd if=challengefile of=output_file conv=swab`` __won't__ help us here, so I wrote a script that inverts 4 bytes instead :

```python
with open('challengefile', 'rb') as f:
    data = f.read()

with open('output_file', 'wb') as f:
    for i in range(0, len(data), 4):
        f.write(data[i:i+4][::-1])```
