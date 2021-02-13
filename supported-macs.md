---
description: >-
  Which unsupported Macs are supported. How can they be both? They are
  unsupported according to Apple, supported according to me. This list is by
  Barry K. N. for his patcher, but it applies here as well
---

# Supported Macs



{% hint style="warning" %}
Remember that this information is incomplete and may not be 100% correct yet, but I'll add more information over time and fix any errors as I learn about them.
{% endhint %}

{% hint style="danger" %}
Also, note that on 2011 and earlier Macs, "no graphics acceleration" is a tremendous, almost exponential, slowdown. For instance, consider a simple benchmark, simply minimizing a Safari window:

* Late 2012 13" MacBook Pro: &lt;1 second
* Early 2011 13" MacBook Pro: 14 seconds
* Late 2009 13" MacBook: 25 seconds

Keep in mind, Mojave and Catalina will probably receive security updates until roughly September 2021 and September 2022 respectively \(give or take a month\), so most users do not need to urgently upgrade to Big Sur.
{% endhint %}

## Mostly/Fully Supported Macs

By the way, with the exception of Mac Pros, all of the Macs in this section officially support Catalina. This section is basically "Macs without official Big Sur support but with Metal support", with the exception of pre-2012 iMacs that have upgraded GPUs. \(In fact, a 2011 iMac with upgraded GPU is almost equivalent to this category. Earlier iMacs may have compatibility problems caused by other components; see below.\)

* If you have a 2013 or later Mac, please check [Apple's official list of supported Mac models](https://www.apple.com/macos/big-sur-preview/) \(search the page for "See if"\) first, to make sure that you actually need Patched Sur.
* Late 2013 iMac: Everything should work \(and, after step 14, you're finished -- no need for step 15 and later\). Note that there have been some reports of very poor performance with Fusion Drives on this model when running Big Sur, which may be why Apple does not support Big Sur on this model.
* 2010/2012 Mac Pro: I have received positive feedback about this patcher, but I do not know which features work perfectly and which don't. If I had to guess which features might be problematic, I would guess sleep and Wi-Fi. patch-kexts.sh \(step 15\) should fix Wi-Fi, but I don't know what effect it might have on sleep. \(You should upgrade the graphics card, as you would for official compatibility with macOS Mojave.\)
* 2009 Mac Pro: Once it's flashed to MacPro5,1 firmware, it should be equivalent to a 2010/2012 Mac Pro. \(As with those, you will want to upgrade to a Mojave-compatible graphics card.\) However, note that some people have had their flashed MacPro4,1s enter boot loops during installation. We don't yet know what causes this or why it only happens sometimes.
* 2012 MacBook Pro: Everything except WiFi works after installation, but there is a patch for it, so it'll work fine with Big Sur.
* Other 2012/2013 Macs: Most things should work after the initial installation, except for Wi-Fi \(unless you have upgraded to an 802.11ac Wi-Fi card\) or possibly GPU switching \(on 15" MacBook Pros\). Step 15 of the installation process fixes Wi-Fi support, but GPU switching may not yet be a solved problem.

## Partially Supported Macs

Most models that officially support High Sierra, but not Mojave, fall into this category. The exceptions are the Mid 2010 15" and 17" MacBook Pros \(see the Incompatible category below\), and possibly the Late 2009/Mid 2010 iMacs \(see the "Unknown status" category below\).

* Note that 2009-2010 iMacs that have been upgraded with Metal GPUs also need certain kext patches which are not \(yet?\) provided by this patcher.
* 2011 Macs: Several features may not work after initial installation \(after step 14 finishes\), including sleep, screen brightness control, Wi-Fi \(unless you have upgraded to an 802.11ac Wi-Fi card\), and graphics acceleration \(unless you have upgraded the GPU in a 2011 iMac\). With the exception of a 2011 iMac with upgraded GPU, no 2011 Mac models have graphics acceleration under Big Sur. Make sure to use the `--2011`command line option in step 15. This fixes sound and Wi-Fi on all 2011 Macs. On 13" MacBook Pros it also fixes sleep and brightness control, and installs the correct Intel framebuffer driver \(this is still unaccelerated, but it still increases speed somewhat -- enough to make full-screen YouTube in Safari work with very few frame drops, although this pegs both CPU cores\). For 15" and 17" MacBook Pros, disabling the discrete GPU will probably increase performance, and sleep and brightness control probably won't work without disabling it. \(That isn't to say that sleep and brightness control will necessarily work even with the discrete GPU disabled -- but it might possibly work if you have a way of disabling the GPU that also keeps sleep and display brightness functional in a dosdude-patched Mojave or Catalina.\) MacBook Airs should be equivalent to the 13" MacBook Pro in terms of compatibility with Big Sur and this patcher.
* Mid 2010 white MacBook, 2010 13" MacBook Pro, 2010 MacBook Air: In addition to the features which don't work after initial installation on the 2011 13" MacBook Pros \(Wi-Fi, sound, graphics acceleration, sleep, display brightness control\), Ethernet doesn't work. The `--2010` option for patch-kexts.sh \(step 15\) installs fixes for Wi-Fi, sound, and Ethernet, as well as drivers that enable the GeForce Tesla \(9400M/320M\) framebuffer \(thereby fixing sleep and display brightness control\). The framebuffer driver does not provide acceleration; the lack of graphics acceleration plus the relatively slow Penryn CPU means performance is sluggish. On at least some of these models, step 6 may fail with errors.
* Late 2009 white MacBook, Late 2009 21.5" iMac, 2010 Mac Mini: In addition to the features which don't work after initial installation on the 2011 13" MacBook Pros \(Wi-Fi, sound, graphics acceleration, sleep, display brightness control\), Ethernet and USB 1.1 also don't work. The `--2010` option for patch-kexts.sh \(step 15\) installs fixes for Wi-Fi, sound, Ethernet, and USB, as well as drivers that enable the GeForce Tesla \(9400M/320M\) framebuffer \(thereby fixing sleep and display brightness control\). The framebuffer driver does not provide acceleration; the lack of graphics acceleration plus the relatively slow Penryn CPU means performance is sluggish. Also, the installation has to be performed on a newer Mac first \(basically a 2010 or newer Mac, or a 2009 or later Mac Pro\), with patch-kexts.sh --2010 run on that same newer Mac, _then_ moved over to the old Mac \(via either a hard drive/SSD transplant or by using a USB enclosure or USB hard drive/SSD\). Otherwise, the installer will boot because USB 2.0 works, but the keyboard and trackpad won't work because USB 1.1 doesn't work. USB support in the installer for these Macs is planned for a future patcher release.

## Potentially Unsupported Mac

* Late 2009 27" iMac: Compatibility will vary based on the CPU. If your Late 2009 27" iMac has a Core 2 Duo CPU, then it is equivalent to a Late 2009 21.5" iMac \(see above\). If it has a Core i5 or i7, CPU, then it is equivalent to a 2010 iMac and is therefore incompatible \(see below\).

## Unsupported Mac

* 2010 15"/17" MacBook Pro, 2010 iMac: These are crashing in AppleACPICPU.kext during boot. Someone needs to create a patch to fix it, or these Macs will not be running Big Sur.
* Any Macs with a pre-Penryn CPU. Basically, this means the original MacBook Air as well as all 2006/2007 Macs \(except for iMacs with upgraded CPUs\).

## Unsuppored But Might Be In The Future

* Macs which have a Penryn CPU but which do not officially support High Sierra: These include pre-2008 iMacs with upgraded CPUs, as well as all 2008 and most 2009 Mac models \(any 2009 models not listed above\). All of these require "legacy USB" support, just like \(for instance\) 2010 white MacBooks. Once support for those MacBooks is improved in a future patcher release, perhaps support for some of these Macs will be worth revisiting.
* Without a Metal GPU upgrade \(certainly possible on 2008 Mac Pros, not sure about the iMacs, not possible on the MacBooks and Mac Minis\), these are expected to be unusably slow.

