# How to Log Into a Course-specific Account on `ieng6`

This can be done in two easy parts

## 1. Install VScode

I had previously installed VScode before logging into a course specific account,
but if you do not already have VScode installed you can do so at [https://code.visualstudio.com/](https://code.visualstudio.com/).
Follow the website's instructions until you are able to open VScode, which will look something like this:

<img width="960" alt="Screenshot_20230112_101620" src="https://user-images.githubusercontent.com/97120058/212162766-ba840a7d-06aa-47df-9153-495fc6307b39.png">

Before moving onto the next step, if you are on a windows machine make sure you install `git` for Windows which contains tools necessary for the rest of this tutorial. I had git installed previously, but if you do not have it installed go to [https://git-scm.com/downloads](https://git-scm.com/downloads) to install the latest version of git. 

## 2. Remotely Connecting

For these next steps you will need to open a terminal in VScode. Either enter Ctrl or Command+` or press Terminal -> New Terminal in the menu. 

<img width="960" alt="Screenshot_20230113_022430" src="https://user-images.githubusercontent.com/97120058/212430507-62ed2927-c256-42f6-9b4b-40f4dd66c00a.png">


Use the command below but replace the `zz` with the letters in your account

` ssh cs15lwi23zz@ieng6.ucsd.edu `

You will likely get a message like this:

<img width="457" alt="Screenshot_20230113_022348" src="https://user-images.githubusercontent.com/97120058/212430546-4dfd6080-55c5-4a00-90bc-3332ce5e17bc.png">


Since this is the first time you are connecting to the server, this is nothing to worry about and you can simply type yes. 

After this you will be prompted to enter your password. Note that you will not be able to see your as you type it in the terminal.

One you do that, you're all set! From here you can try all sorts of commands:
*cd~
*cd
*ls -lat
*ls -a
*ls <directory>

When you wish to exit either press Ctrl-D or run the command `exit`. Here is me running a few commands on my own and then logging out of the remote server

<img width="442" alt="Screenshot_20230112_103255" src="https://user-images.githubusercontent.com/97120058/212431118-de679e47-bccc-4c1b-b9c8-0e3ded8d5994.png">




