These APK files are used to get Google Play Movies and TV and Google Play Music successfully installed on the FireTV stick with FireOS 5.2.1.1. The Google Play Store is installed in the process, but I haven't yet thoroughly tested it to ensure that everything works.

Step 1:
- Install the Android Debug Bridge "sudo apt-get install adb"


Step 2:
- Run the below commands:
	adb kill-server
	adb start-server
	adb connect [IP-Address of FireTV Stick]

The IP-Address of the FireTV stick can be found through Settings > System > About > Network


Step 3:
- Install the packages using the command:
	adb install [package name]

- Install the packages in this order:
	com.google.android.gsf.login_4.4.4-1227136-19_minAPI8(nodpi)_apkmirror.com.apk
	com.google.android.gms_8.7.03_(2645110-230)-8703230_minAPI21(armeabi-v7a)(nodpi).apk
	com.android.vending_6.0.2-leanback-80430286_minAPI21(nodpi).apk
	com.google.android.music-5.7.1780Q.1590147-1780-minAPI14.apk
	com.google.android.videos-3.6.16-tv-36164-minAPI21.apk


Step 4:
- Restart the FireTV Stick, and begin using the apps! Note that there is a bug when logging in. After successfully logging into your Google Account using two-factor authentication, the App may restart the login process without warning -- just back out of the login prompt using the back button, and you should find yourself successfully signed-in.
