---
description: You need WiFi right?
---

# Patching the Kexts

After you install macOS Big Sur or update to a newer version of macOS Big Sur, you'll have to patch the kexts. Kexts, aka Kernel Extensions, are the drivers for your Mac, like the WiFi drivers or the I/O drivers. Since your Mac is unsupported, some of the drivers for your Mac may have been removed, patching these is as simple as a click of a button.

{% hint style="info" %}
If you have a late 2013 iMac \(or upgraded your WiFi card on a 2012/2013 Mac\), you won't need to patch the kexts, everything should work out of the box.
{% endhint %}

There are two places that you can patch the kexts from, the first being the post-install app in your Applications folder, and another is the mini-post-install app on a patched installer USB. If you did a Clean Install, you'll need to use the mini-post-install app on the patched installer USB. If you did an update with the post-install app, you'll need to use the post-install app in your Applications folder. If you did an update with the patched installer USB, you probably have a choice, but it's generally better to use the post-install app in your Applications folder.

{% hint style="warning" %}
If you see the "Optimizing Your Mac" notification, give it time. It uses the volume that Patch Kexts needs to modify, so you cannot patch the kexts while that is going. If you do, you might run into weird errors \(usually concerning mounting a volume saying the resource is busy\). It's best to give this process 5 to 15 minutes \(if you have an HDD or Fusion Drive, give it the full 15\). This error can be solved by trying again when the "Optimizing Your Mac" process is done.
{% endhint %}

## Patching with the Full Post-Install App

To use the post-install app in your Applications folder, you first need to launch it. If you did an update with the post-install app, chances are, it's already open. Once you have it launched, click on the Patch Kexts section.

There, you can click "Start Patching Kexts" and enter your password \(your password is needed to mount the system volume, modify system files, and rebuild the kernel collection\).

The patcher will launch into the process \(it doesn't take too long, but give it time\), and soon it'll say "Restart to Finish". You can either click on that button \(it doesn't do anything in v0.2.1 due to a bug\) or restart manually.

## Patching with the Patched Installer USB Mini-app

To patch the kexts with the mini-post-install app on the patched installer USB, you have to boot into the patched installer USB. Make sure the installer USB is plugged into your Mac, restart it, holding down the option key, then select "Install macOS Big Sur" on the screen that shows. It'll show the Apple logo, and soon, you'll be booted into the installer USB.

Once it finishes booting, you'll see a list of five apps, the bottom one should be the Patched Sur app. Select that, then click the Continue button in the corner of the window. In just a second, Patched Sur will launch.

In the Patched Sur window, you'll see a button and a volume selector. The volume selector will show all the volumes on your Mac, and all you need to do is select the volume you installed Big Sur on with the macOS installer earlier. In most cases, this will be "Macintosh HD". If you select the wrong one, the patcher will probably automatically detect that, and error out. You'll have to quit and relaunch the app to try again.

After you select your volume, click Start Patching Kexts. This will start the patch kexts process that will only take a couple of moments. This doesn't take too long, but give it time in case it does. Once it is done, there will be a "Restart to Finish" button, and you can click that to reboot back into your Big Sur installation where you will have your kexts patched, and you'll be done. The patcher full post-install app will also be added to your Applications folder, so you can use that to update macOS/patch the kexts later on and also do some other things. For now, though, enjoy Big Sur!

