# Tools

## SSL Pinning

    Cydia Substrate: Install the Android-SSL-TrustKiller ↗ package.
    Frida: Use the frida-multiple-unpinning ↗ script.
    Objection: Use the android sslpinning disable command.
    Xposed: Install the TrustMeAlready ↗ or SSLUnpinning ↗ module.

To add your proxy's certificate use the following command:
keytool -importcert -v -trustcacerts -file proxy.cer -alias aliascert -keystore "res/raw/truststore.bks" -provider org.bouncycastle.jce.provider.BouncyCastleProvider -providerpath "providerpath/bcprov-jdk15on-164.jar" -storetype BKS -storepass password

To list certificates in the BKS truststore use the following command:
keytool -list -keystore "res/raw/truststore.bks" -provider org.bouncycastle.jce.provider.BouncyCastleProvider -providerpath "providerpath/bcprov-jdk15on-164.jar"  -storetype BKS -storepass password

## Proxyes

BurpSuite
    ``sudo apt update && sudo apt install -y burpsuite``
    Install the BurpSuite certificate on the Android device
Proxyman (available only on macOS)
mitmproxy
Charles Proxy

### Android Interception Process

    Start the Proxy software and configure it

    Set proxy on the emulator/physical device network settings

    Intercept HTTP traffic

    Import CA Certificates and trust them in the Certificate Store

    Intercept HTTPS Traffic (failing with active SSL Pinning)

    Use Objection/Frida tools to bypass SSL Pinning and intercept HTTPS Traffic

## MobSF Dynamic Analysis:

    🔗 MobSF Dynamic Analyzer
        Supports x86, x86_64 architecture Android 4.1 - 11.0, up to API 30

    🔗 Setting up MobSF dynamic analyzer for security testing of Android applications - Sarvesh Sharma
    

