# Ice Cream Linux

Most Android 4 _(AKA: Ice Cream Sandwich)_ devices run a 3.0.x Linux kernel.  If you want to run a GNU-based Linux disribution alongside Android in a chroot, this is a showstopper because glibc 2.24 (releassed late 2016) requires kernel 3.2 or newer.  As a result, Linux distributions built from 2017 onward won't work with the majority of Android 4.x devices out there.

This project is a Linux environment based on glibc 2.23 from Ubuntu Xenial, with packages backported and rebuilt from newer Ubuntu sources.  Its goal is to run newer versions of Chrome and Firefox on Android 4.x devices made from 2011 onward. 

The environment can be accessed on-device (localhost) or remotely using any RDP client.  Folder redirection and audio both work.  

Current functionality:

- AirPlay enable _any_ wired or bluetooth speaker attached to your Android device.
- Chromium 128.  Firefox 140 is available optionally, but Chromium seems to work better overall.
- [Spot](https://github.com/xou816/spot) GTK Spotify Client.
- Pi-hole DNS Server.  Note you should not use the built-in updater, as source code changes are needed to run with older kernels.

**Requires a rooted device.**

# Installation

- Install walk-thru on [YouTube](https://youtube.com/shorts/fUjbu7cb-1Y?si=6b8pq-6DyteZcY7j)
  
- Download and install the [ICL Deploy APK](https://github.com/DesktopECHO/IceCreamLinux/releases/latest/download/icldeploy.apk).  Older devices with SSL issues can use this [HTTP link](http://desktopecho.com/icldeploy.apk)

- Open ICL Deploy:

  - Tap **⋮** for more options (Three dots at the top right of screen)
  
  - Tap **Install** to create a new instance.  It will take a few minutes to download and deploy the new instance.
    
  - Tap **Start** to run the Linux instance.  It will take a minute or two to configure the instance.  
  
  - Microsoft Remote Desktop will launch, click "Accept" when the license agreement appears.  Do not interrupt the device while it finalizes the configuration.
 
  - You will be logged into a minimal XFCE 4.18 desktop and the device is ready for AirPlay.
  
<img width="2421" height="483" alt="image" src="https://github.com/user-attachments/assets/6edcebb9-268c-4a8f-a02e-6e9adab802ad" />

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

# Configure Autostart
<img width="1452" height="573" alt="image" src="https://github.com/user-attachments/assets/871d1fb8-3420-4f5d-a197-9500fb82a47f" />
