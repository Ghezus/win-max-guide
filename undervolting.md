Undervolting on the GPD WIN MAX using QuickCPU

First of: Why would anyone try and undervolt his device? The simple answer is by puting less power/voltage into the CPU it runs a lot cooler and the battery lasts longer, best of all there should be no noticable preformance diffrence. 

To get started we will need to get a few tools from the internet: 

* [QuickCPU](https://coderbag.com/product/quickcpu) - Get the x64 version and install it, we will use this to set the undervolt
* CPU and GPU stress tests:
	- [Prime95](https://www.mersenne.org/download/) - For CPU, CPU cache and Uncore - Free
	- [Furmark](https://geeks3d.com/furmark/) - For GPU - Free
	- [Aida64 Extreme](https://www.aida64.com/products) - Can test all in one go - $39.95

Instead of running these stress test tools its also possible to use normal benchmark tool's or just running your favorite games. Just note that when adjusting undervolts it might happen that you BSOD or freeze your system since you are lowering voltage to the CPU and that could make your system unstable. 

After installing QuickCPU open the program and on the top right click "Advanced CPU Settings" a new windows will open on this window click "FIVR Control". We are now at the window where we do all our setup. On the left you will see the domain list we will be adjusting each of these domain's one at a time, skipping "GPU Unslice". I always start at the top of the list with the CPU core and do the following steps untill all are at a good value and the system is still running stable. 

<image of FIVR control window with voltage offset labeled>

When doing this I always note down what everything is a before testing stability because when the system crashes you will need to know where you are at. 

1. Step down the voltage offset by 10
2. Run your stress test if the system is stable return to step 1, if not goto step 3. (When changing CPU run a CPU stresstest and when changing GPU use a GPU stresstest)
3. If the system becomes unstable return to the last working value, return to step 1 now using a smaller step. 

Keep doing this untill you hit the biggest undervolt on the given domain without making your system unstable and crash or freeze. When you find this value do the same for the next domain, and just keep going untill you find the best undervolt value for each of the domains of your processor. Make sure that when you go to the next domain the previous ones are set to your previously obtained value. 

After finding your undervolt values you will want to make sure these are set when starting your system, currently the only way of doing this is making sure QuickCPU start with a FIVR profile.
