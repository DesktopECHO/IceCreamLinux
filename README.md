# Ice Cream Linux

Most Android 4 _(AKA: Ice Cream Sandwich)_ devices run a 3.0.x Linux kernel.  If you want to run a GNU-based Linux disribution alongside Android in a chroot, this is a showstopper because glibc 2.24 (releassed late 2016) requires kernel 3.2 or newer.  As a result, Linux distributions built from 2017 onward won't work with the majority of Android 4.x devices out there.

This project is a Linux environment based on glibc 2.23 from Ubuntu Xenial, with packages backported and rebuilt from newer Ubuntu sources.  Its goal is to run newer versions of Chrome and Firefox on Android 4.x devices made from 2011 onward. 

The environment can be accessed on-device or remotely via RDP protocol.  
Folder redirection and audio work out of the box.  

Current functionality:

- Chromium 128 and Firefox 140.  Chromium seems to work better overall.
- [Spot](https://github.com/xou816/spot) GTK Spotify Client
- Pi-hole DNS Server.  Note you should not use the built-in updater (Source code changes are needed to work with old kernels).
- Device becomes an AirPlay target.  This lets you AirPlay enable **any** wired or bluetooth speaker attached to your Android device

**Requires a rooted device.**

# Instructions

- Download/install the Linux Deploy APK.  [Version 2.5.1](https://github.com/meefik/linuxdeploy/releases/tag/2.5.1) is the latest version for Android 4.x.
  
- Download the Ice Cream Linux [disk image](https://github.com/DesktopECHO/IceCreamLinux/releases/latest/download/icl.tgz) and copy it to your device.

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
     
<table border="0">
  <tr>
    <td><img alt="xfce" src="https://github.com/user-attachments/assets/37356f63-bed4-408f-939c-b01a5148acac" width="100%"/></td>
    <td width="30"></td>
    <td><img alt="chromium" src="https://github.com/user-attachments/assets/7c46d28f-b605-4dbf-b9d8-f607350f7f3a" width="100%"/></td>
    <td width="30"></td>
    <td><img alt="thunar" src="https://github.com/user-attachments/assets/89c9257e-5cd2-4d64-b532-cc7d62a7d5fa" width="100%"/></td>
  </tr>
  <tr>
    <td align="center">XFCE4 Desktop.  The 'Start' button can be dragged anywhere onscreen.</td>
    <td></td>
    <td align="center">Full desktop versions of Chromium 128 amd Firefox 140</td>
    <td></td>
    <td align="center">File Manager with Android sdcard redirection</td>
  </tr>
</table>

<br>

<table border="0">
  <tr>
    <td><img alt="yt" src="https://github.com/user-attachments/assets/86fa28f1-3ea9-4853-8a95-4aea0cc50536" width="100%"/></td>
    <td width="30"></td>
    <td><img alt="spot" src="https://github.com/user-attachments/assets/76eba08f-51be-44af-a2fb-c22f2813d9ee" width="100%"/></td>
    <td width="30"></td>
    <td><img alt="neofetch" src="https://github.com/user-attachments/assets/da0990d9-0eff-45d9-96ba-5b8fa336c7f8" width="100%"/></td>
  </tr>
  <tr>
    <td align="center">YouTube Web App - other PWA's have been tested and work well.</td>
    <td></td>
    <td align="center">Spotify Player (Spot GTK4 Rust Client)</td>
    <td></td>
    <td align="center">ICL on a 14 year old Galaxy S2 with 845MB RAM and 3.0 Kernel</td>
  </tr>
</table>

