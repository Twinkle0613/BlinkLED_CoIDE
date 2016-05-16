Developed STM32F103C8T6 By using CoIDE
======================================

##Problem 1
>In the CoIDE V1.7.8 version, I have faced the problem which is the default linker-script can't be changed. 
It is due to some bug in CoIDE that doesn't update properly the changes that was made to the selection of linker-script.
Now, I have a solution to solve this problem. To overcome this problem need to follow 2 step:

1. Close The CoIDE. Note: If you still open the CoIDE, However you change the linker-script that is always set by defualt.

2. Open blink.coproj file,
   1. The "UseMemoryLayout" value must be set to 0.
   2. The "nostartfiles" value must be set to 0.
   3. The "LocateLinkFile path" msut be set to the path to the linker-script you want.

The image was shown in below.
![Alt text](https://github.com/Twinkle0613/BlinkLED_CoIDE/blob/master/Image/coproj.png)
