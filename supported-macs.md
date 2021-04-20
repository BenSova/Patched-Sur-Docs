---
description: >-
  Which unsupported Macs are supported. How can they be both? They are
  unsupported according to Apple, supported according to me. Thanks to BarryKN
  for originally compiling this.
---

# Supported Macs



{% hint style="warning" %}
Remember that this information is incomplete and may not be 100% correct yet, but I'll add more information over time and fix any errors as I learn about them.
{% endhint %}

## 2012/2013 Macs

All 2012 and 2013 Macs are fully supported. They have full graphics acceleration and everything works perfectly fine. WiFi may not work after installation, however, patching the kexts with a couple clicks of a button fixes this. Only Late 2013 iMacs don't need WiFi patches, so you're ready right out of the box. 

## 2011 Macs

{% hint style="danger" %}
"No graphics acceleration" is a tremendous, almost exponential, slowdown that **SHOULD NOT** be ignored. For instance, consider a simple task, simply minimizing a Safari window:

* Late 2012 13" MacBook Pro: &lt;1 second
* Early 2011 13" MacBook Pro: 14 seconds
* Late 2009 13" MacBook: 25 seconds

Keep in mind, Mojave and Catalina will probably receive security updates until roughly September 2021 and September 2022 respectively \(give or take a month\), so most users do not need to urgently upgrade to Big Sur.
{% endhint %}

On most of these Macs, THERE WILL BE NO graphics acceleration WHICH SHOULD NOT BE IGNORED. Check the red box above to learn simply how bad those Macs will run. If you really want to be dumb and ignore me, well, I can't stop you from that, but at least make a backup. If you don't make a backup and ignore me, then you'll be in a whole lot of pain later on, and that's not my fault. Other than graphics acceleration, you'll be pretty much fine after you patch the kexts.

Note: If you have a 2011 iMac and upgrade the GPU, then you will have graphics acceleration, and Patched Sur will alert you if you do not have a Metal capable GPU.

## 2010

On most of these Macs, THERE WILL BE NO graphics acceleration WHICH SHOULD NOT BE IGNORED. Check the red box above to learn simply how bad those Macs will run. If you really want to be dumb and ignore me, well, I can't stop you from that, but at least make a backup. If you don't make a backup and ignore me, then you'll be in a whole lot of pain later on, and that's not my fault. Other than graphics acceleration, you'll be pretty much fine after you patch the kexts.

Note: 2010 15"/17" MacBook Pros, 2010 iMacs currently cannot boot Big Sur since they crash while loading a specific kext. 

## 2009

At this point, it gets really confusing, and I don't have a definitive answer to whether they do or don't work. Either way, chances are your Mac will not boot with Big Sur, and even if it does, you'll basically only have a turtle, that's extremely slow and struggles to minimize Safari. 

## 2008/2007/2006/2005/2004/2003/2002/2001/2000

Sadly, these Macs are way too old to even boot Big Sur, so they do not support this patcher.

Note: 2008 Mac Pros do work with Big Sur, but not with this patcher. I recommend checking out [StarPlayrX's BigMac Patcher ](https://github.com/StarPlayrX/BigMac)for those.

