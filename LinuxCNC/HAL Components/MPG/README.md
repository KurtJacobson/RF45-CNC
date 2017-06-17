## MPG HAL Component

### NAME  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; mpg − 4 axis MPG with multiplexed axis and increment selector switches

### SYNOPSIS
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; loadrt mpg[count=N|names=name1[,name2...]]

### FUNCTIONS
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **mpg.**_N_

### PINS  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **mpg.**_N_**.axis0** bit in  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Input from out0 of the axis selection switch  

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **mpg.**_N_**.axis1** bit in  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Input from out1 of the axis selection switch

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **mpg.**_N_**.scale0** bit in  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Input from out0 of the scale selection switch

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **mpg.**_N_**.scale1** bit in  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Input from out1 of the scale selection switch

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **mpg.**_N_**.mpg_scale** float out  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Outputs selected mpg scale

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **mpg.**_N_**.enable-x** bit out  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; _TRUE_ if x-axis is selected (**axis0**=_FALSE_ and **axis1**=_FALSE_)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **mpg.**_N_**.enable-y** bit out  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; _TRUE_ if y-axis is selected (**axis0**=_TRUE_ and **axis1**=_FALSE_)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **mpg.**_N_**.enable-z** bit out  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; _TRUE_ if z-axis is selected (**axis0**=_FALSE_ and **axis1**=_TRUE_)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **mpg.**_N_**.enable-a** bit out  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; _TRUE_ if a-axis is selected (**axis0**=_TRUE_ and **axis1**=_TRUE_)

### PARAMETERS  

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **mpg.**_N_**.mpg-scale1** float rw (default: _.01_)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Desired jog scale for first increment switch position  

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **mpg.**_N_**.mpg-scale2** float rw (default: _.001_)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Desired jog scale for second increment switch position  

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **mpg.**_N_**.mpg-scale3** float rw (default: _.0001_)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Desired jog scale for third increment switch position  

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **mpg.**_N_**.mpg-scale4** float rw (default: _.00001_)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Desired jog scale for fourth increment switch position  

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **mpg.**_N_**.mpg_pulses** s32 rw (default: 4)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Number of pulses per MPG detent  

### LICENSE

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; GPL
