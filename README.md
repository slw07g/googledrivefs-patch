To get Google Drive File Stream running in Big Sur beta, run the following commands in a Terminal:

```
sudo kextload "/Applications/Google Drive File Stream.app/Contents/MacOS/dfsfuse.kext"

1>/dev/null 2>/dev/null /Applications/Google\ Drive\ File\ Stream.app/Contents/MacOS/Google\ Drive\ File\ Stream &
```

Update (2020-11-24):

I upgraded to Big Sur 11.1 Beta and began encountering issues with Google Drive File Stream again. The kext appeared to be the culprit again. To resolve the issues, I ran the first command mentioneda above:
```
sudo kextload "/Applications/Google Drive File Stream.app/Contents/MacOS/dfsfuse.kext"
```
I was then presented with a prompt indicating I needed to approve the kext in Settings >> Security & Privacy >> General tab. After approving, I had to reboot. You would think Google Drive FS would start fine this time, but I needed to run the `kextload` command again and the quit and relaunch Google Drive FS. It appeared to work fine now.

It's possible that the kextload may be required at each boot until google fixes Google Drive.
