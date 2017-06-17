# MPG HAL Component

**NAME**
mpg − 4 axis MPG with multiplexed axis and increment selector switches

**SYNOPSIS**
                                      loadrt mpg[count=N|names=name1[,name2...]]
**FUNCTIONS**
mpg.N

**PINS**

mpg.N.axis0 bit in
Input from out0 of the axis selection switch
mpg.N.axis1 bit in
Input from out1 of the axis selection switch
mpg.N.scale0 bit in
Input from out0 of the scale selection switch
mpg.N.scale1 bit in
Input from out1 of the scale selection switch

mpg.N.mpg_scale float out
Outputs selected mpg scale

mpg.N.enable-x bit out
TRUE if x-axis is selected (axis0=FALSE and axis1=FALSE)

mpg.N.enable-y bit out
TRUE if y-axis is selected (axis0=TRUE and axis1=FALSE)

mpg.N.enable-z bit out
TRUE if z-axis is selected (axis0=FALSE and axis1=TRUE)

mpg.N.enable-a bit out
TRUE if a-axis is selected (axis0=TRUE and axis1=TRUE)

PARAMETERS


mpg.N.mpg-scale1 float rw (default: .01)
Desired jog scale for first increment switch position
mpg.N.mpg-scale2 float rw (default: .001)
Desired jog scale for second increment switch position
mpg.N.mpg-scale3 float rw (default: .0001)
Desired jog scale for third increment switch position
mpg.N.mpg-scale4 float rw (default: .00001)
Desired jog scale for fourth increment switch position
mpg.N.mpg_pulses s32 rw (default: 4)
Number of pulses per MPG detent
LICENSE


GPL


Installing the MPG HAL Component

The mpg.comp file can be downloaded at the bottom of this page. If you have the LinuxCNC development packages the easiest way to install it is to say

        sudo halcompile --install mpg.comp

while in the directory where mpg.comp is located.


If you don't have the LinuxCNC development packages you can install them by saying

        sudo apt-get install linuxcnc-dev


You could also just place the precompiled mpg.ko file found at the bottom of this page in you LinuxCNC components folder.
