A very primitive approach to remove the offset on 4718, you should not use it on other device unless you are willing to send the device back to DATAQ for recal!

1. Run this program, and keep gain and offset at all ZERO and push the button. This step remove digital offset adjustment for the device
2. Exit this program
3. Short all inputs and run WinDaq to show ALL channels, and write down the current offsets, for example, -160mV on Channel 1....
4. Calculate the digital offset adjustment for each channel, with 32768*(Offset/5V). With the above example of -160mV, you will get 32768*(-0.16/5)=-1035
5. Negate this number, in the above example, we use 1035
6. Run the program again
7. Change the offset to 1035
8. Push the button to digitally remove all offsets
9. Exit this program
10. Run Windaq again and you will see all offset is removed
