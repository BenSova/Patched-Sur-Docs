# Update Hangs At ~40%

There's a small chance that the updater will hang at 40% with the Apple logo. To be clear, I don't mean when Patched Sur says "Preparing for Update", I mean when you are at the Apple Logo with a progress bar and it appears to be at 40%.

{% hint style="danger" %}
Please note that the updater will hang in places and that's perfectly normal. Only use the below solution if the updater has hung at what looks like 40% without moving at all for 45 minutes. If you try the below solution and you have 1% or 99%, you could corrupt the system files, and require a reinstall, possibly losing your data if you don't have a backup.
{% endhint %}

If you are absolutely sure it is hanging \(at least 45 minutes without any movement\) at around 40% \(if you're unsure about if it's at 40%, it probably is, it'll be obvious if it's not\), then you can continue. What you're going to do might sound a bit scary, but I promise you, as long as you are in a spot that I just said, you will be fine.

The solution is to turn off your Mac then turn it back on. Yes, it's that simple. This is generally a bad idea when your Mac is updating, but multiple times this has proven to be successful. After you turn back on your Mac, it will continue doing what it was doing and soon you'll be on the log-in screen.

{% hint style="info" %}
If your keyboard or mouse doesn't work after this happens, the solution that was found was interesting, to say the least. Just unplug your keyboard/mouse and plug it back in, then do that again, and again, and keep on doing it until it works.
{% endhint %}

After your Mac finishes booting and you unlock it, you'll have to [patch the kexts](../postinstall-after-upgrade/patching-the-kexts.md) again \(unless you are a Late 2013 iMac\), which can be done with the post-install app that's in your Applications folder and probably also already open. If you have a way to access the internet before patching the kexts, I heavily suggest installing recovery before patching the kexts. That way if something goes wrong while patching the kexts, you'll be fine.

