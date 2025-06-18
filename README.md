# Ice Cream Linux

A Linux environment based on Ubuntu sources with modern web browsers for Android 4.x and other devices running old Linux kernels (2.6.24 to 3.1.10).  The environment can be accessed on-device or remotely via RDP protocol.  Folder redirection and audio playback/recording work out of the box.

Build 14 includes Firefox 140, Chrome 128, [spot](https://github.com/xou816/spot) GTK Spotify Client, and a GTK [audio recorder](https://launchpad.net/~audio-recorder/+archive/ubuntu/ppa).

**Requires a rooted device.**

# Instructions

- Download/install the Linux Deploy APK.  [Version 2.5.1](https://github.com/meefik/linuxdeploy/releases/tag/2.5.1) is the latest version for Android 4.x.
  
- Download the Ice Cream Linux [disk image](https://github.com/DesktopECHO/IceCreamLinux/releases/download/15/icl15.tgz) and copy it to your device.

- Download/Install an RDP client to connect to the Linux instance on your device:

  - Android 4.1+ · [Remote Desktop 8 8.1.82.445](https://www.apkmirror.com/apk/microsoft-corporation/microsoft-remote-desktop/microsoft-remote-desktop-8-1-82-445-release/)

  - Android 4.0.3+ · [Remote Desktop 8 8.1.28.2](https://www.apkmirror.com/apk/microsoft-corporation/microsoft-remote-desktop/microsoft-remote-desktop-8-1-28-2-release/)
    
- In Linux Deploy options, enable the SysV Init System.

- Import the image into Linux Deploy.  

- Start the Instance.  New SSH Keys and SSL certificates are regenerated during the deploymemt's first-run.

- Open your RDP client and conect to the instance, either locally by using `localhost` for the device name, or remotely using the device's IP address or mDNS name.

<img width="400" height="640" alt="screen" src="https://github.com/user-attachments/assets/53d7302e-f447-444e-9716-08b5c11b8431" /> · <img width="400" height="640" alt="screen1" src="https://github.com/user-attachments/assets/a30932a8-725f-4a91-b02a-aebd65c27f3c" />
