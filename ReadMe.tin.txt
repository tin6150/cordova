

# installed android studio and java the normal gui way.

# npm was avail from windows cmd (previously installed by me?  don't remember).
# had to run npm from cmd, not a cygwin bash shell, not mobaxterm shell

# npm install -g cordova # from cmd worked, direct internet connection, cmd did not understand proxy


## https://cordova.apache.org/docs/en/latest/guide/platforms/android/

## https://cordova.apache.org/docs/en/latest/guide/cli/


# cordova works in cygwin bash 
cordova create psg com.skinforum.psg PocketSurvivalGuide

cd psg
cordova platform add android --save

cordova platform ls 
cordova requirements


# vi config.xml
# vi platforms/android/AndroidManifest.xml
#       hopefully using android-19 which is 4.4 KitKat and above

# seems like can't run build inside dropbox dir
# cuz CamelCase of fodername is mangled once dropbox sync the folder 
# and this result in unaccesible path in linux
# eg platforms/android/CordovaLib

# can't build in windows, cuz looks for gradlew which isn't found... not sure if there are more tricks...

cordova build android

#cordova emulate android  # ??:L
#cordova run android





#/home/sn-dropbox/Dropbox/code/cordova/psg/platforms/android/ant-build/MainActivity-debug.apk
#--> psg.16.903.apk   # 16 MB


new local build:
cp -p /home/sn/code-local/psg/platforms/android/ant-build/MainActivity-debug.apk   /home/sn/code-local/psg.16.903c.apk
#  apk is 6.2 MB (zip compressed file really)  this version removed android/* pkg :)
#  

