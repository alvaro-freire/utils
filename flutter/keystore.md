## Generate SHA-1 fingerprint of Keystore Certificate

1. Generate file with SHA-1 fingerprint:

```sh
keytool -genkey -v -keystore /path-to-key/keystore.jks -keyalg RSA -keysize 2048 -validity 10000 -alias YourAppName
```

> You will have to set up a password, the rest of the fields are not needed to be filled.

2. Create `key.properties` file in `project-dir/android`:

```
storePassword=PASSWORD
keyPassword=PASSWORD
keyAlias=YOURAPPNAME
storeFile=PATH_TO_KEYSTORE.JKS
```

3. That's it. You can check your SHA-1 key:

```zsh
╭─user at machine in ~ 22-10-26 - 20:22:29
╰─○ keytool -list -v -keystore PATH_TO_KEYSTORE/keystore.jks -alias YourAppName

Enter keystore password:  
Alias name: YourAppName
Creation date: Oct 26, 2022
Entry type: PrivateKeyEntry
Certificate chain length: 1
Certificate[1]:
Owner: CN=Unknown, OU=Unknown, O=Unknown, L=Unknown, ST=Unknown, C=Unknown
Issuer: CN=Unknown, OU=Unknown, O=Unknown, L=Unknown, ST=Unknown, C=Unknown
Serial number: XXXXXXXXXXXXXXXX
Valid from: Wed Oct 26 20:06:09 CEST 2022 until: Sun Mar 13 19:06:09 CET 2050
Certificate fingerprints:
	 SHA1: XX:XX:XX:XX:XX:XX:XX:XX:XX:XX:XX:XX:XX:XX:XX:XX:XX:XX:XX:XX
	 SHA256: XX:XX:XX:XX:XX:XX:XX:XX:XX:XX:XX:XX:XX:XX:XX:XX:XX:XX:XX:XX:XX:XX:XX:XX:XX:XX:XX:XX:XX:XX:XX:XX
Signature algorithm name: SHA256withRSA
Subject Public Key Algorithm: 2048-bit RSA key
Version: 3

Extensions: 
...
...
```
