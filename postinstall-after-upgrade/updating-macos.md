---
description: 'Don''t worry, it''ll get easier.'
---

# Updating macOS

If you open the post-install app and try to open the updater, there are two different screens you might run into. The first being the update the patcher app screen and the second being the update macOS screen. Both will provide a simple outlook of information about the new up. If you want to learn some more about updating the app, head over to the Updating The Post Install App section to learn the basics of how it works. 

{% hint style="info" %}
Due to some problems with the scripts that are supposed to turn off the macOS compatibility check in startosinstall, I have been unable to include the **Update without a USB** functionality as of right now. Until these problems are resolved, I won't release the updater. 
{% endhint %}

This process is the same as the initial upgrade to Big Sur. You make a USB then use it to reinstall macOS. I'll give a quick rundown of what you need to do just to clarify everything.

### Make an Installer USB

Making a macOS Big Sur Installer USB is relatively simple. You only need two things, a copy of macOS Big Sur and a USB drive. With Patched Sur you only need a copy of Patched Sur and the USB drive. 

To get Patched Sur, download the most recent release from GitHub \(or from [this link](https://github.com/BenSova/Patched-Sur/releases/download/v0.0.5/Patched-Sur.dmg)\) and open the app \(do not move it to your Applications folder\). 

After you have it open, run through the initial prompts until selecting all the preferences you want, like the [Update Track](../preinstall-catalina/release-tracks.md) and Install Method \(you will want to choose Update for that\).

Once you see the Download macOS 11.X screen, just click Download if that's the version you want, otherwise click View Other Versions to see other versions or use your own.

After the download, enter your password and select the USB drive you want to use, remember that it will be completely erased. It'll erase the drive, add a copy of macOS recovery to it, and patch it. 

### Reinstall macOS

At the end of that process, you'll see the finished screen and all you have to do is turn off your Mac, then turn it back on again holding the option key. The boot picker will come up and you can click EFI Boot, observe your Mac shut down, then turn it on with the option key again, this time selecting Install macOS Big Sur.

Your Mac will then boot into macOS Big Sur recovery, and all you have to do is click \(Re\)Install macOS Big Sur, press agree without reading anything, choose your main drive \(not the USB drive\), and let it go.

### Patch the Kexts

Finally, once your new version of Big Sur boots, you'll be able to patch the kexts and be finally updated and done. If you have a Late 2013 iMac, you should be fine since everything should work out of the box.

To do this, open the Applications folder or Launchpad and then click Patched Sur. Once it launches, you can select Patch Kexts then Start and enter your password. After it's done, it'll prompt you to restart your Mac and everything will be fine after that!

