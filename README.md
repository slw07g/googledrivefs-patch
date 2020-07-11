To get Google Drive File Stream running in Big Sur beta, run the following commands in a Terminal:

```sudo kextload "/Applications/Google Drive File Stream.app/Contents/MacOS/dfsfuse.kext"

1>/dev/null 2>/dev/null /Applications/Google\ Drive\ File\ Stream.app/Contents/MacOS/Google\ Drive\ File\ Stream &```
