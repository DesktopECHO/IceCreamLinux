# Ice Cream Linux

A Linux environment based on Ubuntu sources with modern web browsers for Android 4.x and other devices running old Linux kernels (2.6.24 to 3.1.10).  The environment can be accessed on-device or remotely via RDP protocol.  Folder redirection and audio playback/recording work out of the box.

Build 15 includes Firefox 140, Chrome 128, [spot](https://github.com/xou816/spot) GTK Spotify Client, and a GTK [audio recorder](https://launchpad.net/~audio-recorder/+archive/ubuntu/ppa).

**Requires a rooted device.**

# Instructions

- Download/install the Linux Deploy APK.  [Version 2.5.1](https://github.com/meefik/linuxdeploy/releases/tag/2.5.1) is the latest version for Android 4.x.
  
- Download the Ice Cream Linux [disk image](https://github.com/DesktopECHO/IceCreamLinux/releases/download/15/icl15.tgz) and copy it to your device.

- Download/Install an RDP client to connect to the Linux instance on your device:

  - Android 4.1+ · [Remote Desktop 8 8.1.82.445](https://www.apkmirror.com/apk/microsoft-corporation/microsoft-remote-desktop/microsoft-remote-desktop-8-1-82-445-release/)

  - Android 4.0.3+ · [Remote Desktop 8 8.1.28.2](https://www.apkmirror.com/apk/microsoft-corporation/microsoft-remote-desktop/microsoft-remote-desktop-8-1-28-2-release/)
    
- In Linux Deploy options:

  - Enable the SysV Init System
    
  - Set a password for the default user (username: _android_)

- Deploy the instance and wait a few minutes for it to complete.  

- Start the Instance.  SSH Keys and SSL certificates will be regenerated during the deploymemt's first-run.

- Open your RDP client and conect to the instance:
 
   - When running the RDP client directly on the deivice, set `localhost` for the device name
     
   - For remote connections, set to the device's IP address or mDNS name (_devicename.local_)
 
   - Set the username (android) and the password you set in Linux Deploy
 
   - Enable folder, audio, and microphone redirection as needed
     
   - If the device has a touch screen, set mouse click to 'Tap' style


# Desktop Session
     
A minimal desktop environment will appear.  Tap the launcher (Android icon) for a list of apps:

<img width="400" height="640" alt="screen" src="https://github.com/user-attachments/assets/53d7302e-f447-444e-9716-08b5c11b8431" />

Chrome 128 on libc6 2.23:

<img width="400" height="640" alt="screen1" src="https://github.com/user-attachments/assets/a30932a8-725f-4a91-b02a-aebd65c27f3c" />
