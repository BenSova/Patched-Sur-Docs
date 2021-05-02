# Select USB Volume

After the downloads are done, you have to select a volume to create the macOS installer on. This is preferably a USB drive but some other external media like an external SSD \(but not an SD card since sometimes those are problematic\) will work. Once you select it, press "Continue", acknowledge that the volume you selected will be completely erased without any data left \(except other partitions sometimes\) and press "Continue and Erase".

### What to do if your drive doesn't show up.

Some drives won't show up because of how Patched Sur validates whether a volume can be used or not.

The first thing to check is to make sure the drive is external, older versions of the patcher had a tendency to erase the entire drive including other partitions, so using a system disk is not allowed, in that case, go get an actual external drive like a USB drive or external SSD \(sometimes, SD Cards are considered internal drives and there's no way I can work around this\).  
  
Another thing to check is if the drive is formatted as MacOS Extended \(Journaled\). To check this, open Disk Utility, select your device in the sidebar, and in the overview under the name, it'll say whether it's MacOS Extended \(Journaled\) or another format like APFS or Fat32. If it is something else, click Erase in the toolbar, and erase your drive to be formatted as MacOS Extended \(Journaled\).  
  
The final thing you can check is if the drive has GUID Partition Map. To check this, open Disk Utility, then click the Sidebar icon and select "Show all Devices". After you click that, you should see the brand and name of your external device shown. Click on the item on the sidebar titled with your USB's brand name then select Erase. Make sure that the device will have both a GUID Partition Map \(instead of Master Boot Record or other\) and is formatted as MacOS Extended \(Journaled\) in the popup, then press erase.  
  
If neither of those worked, open Terminal and type in `diskutil list`, then drag in your USB drive and press enter. Take the info that's outputted by that and send it to me \([ubensova@gmail.com](mailto:ubensova@gmail.com)\).

