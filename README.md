Wi-Fi Transfer for Android

A native Android app for exchanging files with the Android and desktop versions on the same local network. The app automatically announces a random name, shows discovered devices, and sends selected documents only after the recipient gives consent.
Building

Requires JDK 17 and Android SDK Platform 36. The project includes a Gradle wrapper.
powershell

.\gradlew.bat assembleDebug

The APK will be created at app/build/outputs/apk/debug/app-debug.apk.
Transfer

On both devices, open the app and connect to the same Wi-Fi network. On the sender, select the device and files. The recipient will see the contents of the transfer and can accept or decline the request. On Android 10+, files are saved to the shared folder Downloads/Wi-Fi Transfer; on Android 8–9, to Android/data/com.captstoyev.wifitransfer/files/Download/Wi-Fi Transfer.

Discovery uses UDP port 8766, and transfer uses TCP port 8765. The router must allow local broadcast packets and connections between devices. The transfer is performed without TLS, so use only a trusted network.

Author: Capt. Stoyev Igor.
