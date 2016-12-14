This is used to get Google Play Movies and TV and Google Play Music successfully installed on the FireTV stick with FireOS 5.2.1.1 in only 5 steps! The Google Play Store is installed in the process, but I haven't yet thoroughly tested it to ensure that everything works. I recommend using Linux as you install these APK files, as the process is considerably simpler. If you wish to use Mac OS or Windows, then you will need to find and install the Android Debug Bridge program, and the commands given below may differ. Additionally, the two machines must be connected to the same wireless network throughout the process.

### Step 1: (On FireTV device)    
 - Navigate to Settings > Developer Options    
 - Enable "ADB Debugging"    
 - Enable "Apps from Unknown Sources"    

### Step 2: (On Linux PC)    
- Install the Android Debug Bridge:     
	`sudo apt-get install adb`


### Step 3: (On Linux PC)      
- Run the below commands:       
	`adb kill-server`    
	`adb start-server`    
	`adb connect [IP-Address of FireTV device]`     
 
The IP-Address of the FireTV device can be found through Settings > System > About > Network
     
     
### Step 4: (On Linux PC)     
- Navigate to the directory containing the APK files. 
- Install the packages in this order:    
	`adb install com.google.android.gsf.login_4.4.4-1227136-19_minAPI8(nodpi)_apkmirror.com.apk`    
	`adb install com.google.android.gms_8.7.03_(2645110-230)-8703230_minAPI21(armeabi-v7a)(nodpi).apk`    
	`adb install com.android.vending_6.0.2-leanback-80430286_minAPI21(nodpi).apk`    
	`adb install com.google.android.music-5.7.1780Q.1590147-1780-minAPI14.apk`    
	`adb install com.google.android.videos-3.6.16-tv-36164-minAPI21.apk`    
    
     
### Step 5 (On FireTV device):
- Restart your FireTV device, and begin using the apps! Note that there is a bug when logging into a Google app for the first time: after successfully logging into your Google Account using two-factor authentication, the App may restart the login process without warning -- just back out of the second login prompt using the back button on your FireTV remote, and you should find yourself successfully signed-in.
