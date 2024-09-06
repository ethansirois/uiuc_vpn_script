Please visit the folder for the course that you want to use the automatic VPN&SSH connection to. In there, select your OS. In that folder you should see a README.md with specific information and guidance for utilizing the script for that specific course.
NOTE: I believe that Windows users can use the Linux scripts if they use ```wsl``` to emulate Linux, and then run the scripts. I could be pretty wrong on that though. It has not been tested (to my knowledge...).

Note that if SSH hangs (it is just sitting there and nothing is happening for ~10 seconds), just hit CTRL-C to cancel the process, and try running the script again. This is a bug that happens every once in a while with the script that I am working to fix. It shouldn’t be an issue, but just might require you to rerun the script.
See the comments in the files for some more notes and troubleshooting. Specifically, the comments of ```{any course}env``` and ```uiucvpnup``` files.

Let me know if you have any difficulties or questions. It should be noted that you are storing your password in a text file on your computer, which could be a security risk. I do not take responsibility for anything that happens as a result of this, although I will say that with 2FA, I don't personally think that it is that risky. If it makes you feel more secure, you can change the 391env script to take command-line input for your password rather than storing it in the file. 
Also, use this script for any SSH setting! Many courses require that you SSH into an EWS machine (CS 128 and CS 341 for sure). To use this script for other courses, just copy 426 to a new file for that course, and then change the SSH address in that new file to your different SSH address. I'll do an example for CS 341.

1. Run the following command in your terminal to copy the file:
```
cp 426env 341env
```
2. Enter 341env and change the SSH address from ...@....ews.illinois.edu to ...@fa24-cs341.ews.illinois.edu.
That's it. Then you can analogously run:
```
341env
```
in your terminal from any directory to enter the 341 EWS environment.
