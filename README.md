# smceb.github.io  


# git command  
~~~
git clone https://github.com/smceb/smceb.github.io.git  
cd smceb.github.io/  
echo "Hello World!" > index.html  
git config --list  

git config user.name "name"  
git config user.email "email"  
git config --global user.name "name"  
git config --global user.email "email"  
git config --global --unset user.name "name"  
git config --global --unset user.email "email"  

git add --all  
git status  
git commit -m "commit comment"  
git push -u origin main  
~~~

https://github.github.io  


# Android package signature  
> Check signature  
apksigner verify -v app-release.apk  


# adb command  
adb shell pm disable-user com.android.test ==> Disable package  
adb shell dumpsys restriction_policy | grep "firmware"  
adb shell dumpsys device_policy > log.txt  
  
### How to get signature checksum of Android package?  
> keytool -list -printcert -jarfile <app-release.apk> | grep -Po "(?<=SHA256:) .*" | xxd -r -p | openssl base64 | tr -d '=' | tr -- '+/=' '-_'  

