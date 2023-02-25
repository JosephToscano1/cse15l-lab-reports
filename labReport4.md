# Editing a File Utilizing Git in the Terminal

Despite what people may think, it is not at all necessary to use a website when working with git.
Similar to how java can be used as a command line tool as opposed to in a visual editor like VSCode, 
git can be operated entirely from the terminal of a machine, which is helpful when making small scale changes
or working remotely. 

In this lab I utilized git along with shortcuts in the command terminal to speedily make a small
edit to a file in the lab7 respository which I had forked on my GitHub account.

These are the following steps executed:


1. Log into ieng6
2. Clone the fork of the lab7 repository to the remote machine
3. Run the associated tests for the ListExamples.java file
4. Edit the code to fix the failing test
5. Run the tests, demonstrating that they now succeed
6. Commit and push the resulting change to my Github account

## 1. Log into ieng6

<img width="401" alt="Screenshot_20230225_010110" src="https://user-images.githubusercontent.com/97120058/221380671-d159465b-7606-41d5-884d-4f7bfa2dce7c.png">

This was one of the more straightforward steps. I had already entered this command relatively recently, so I decided to press `<up>` on the keyboard until
I saw the command, roughly 12 times. Unfortunately, because I used the randomart shortcut on a lab computer rather than my own, I wasn't able to bypass entering my password.

keys pressed: `<up><up><up><up><up><up><up><up><up><up><up><up> <enter> [Password] <enter>`

## 2. Clone the fork of lab7 repository

<img width="416" alt="Screenshot_20230225_010215" src="https://user-images.githubusercontent.com/97120058/221380815-ebf3fdea-6752-4b1d-86f3-8fac64beec00.png">

This command was also straight forward. I had the link copied to my clipboard, so all I had to do was right click after typing `git clone`.
However, this step would later on be proven to be a mistake as I copied the http link instead of the ssh link from Github. Why this was a mistake will be explained in step 6.

keys pressed `[git clone] <rclick>`

## 3. Run ListExamples Tests

<img width="769" alt="Screenshot_20230225_010604" src="https://user-images.githubusercontent.com/97120058/221380916-46a35de2-5bb8-44f0-a658-fd2aaabd274b.png">

These commands were also in my bash command history, so I decided to access them using the up arrow keys.

Keys Pressed: `<up><up><up><up><up><up><up><up><up><up> <enter> <up><up><up><up><up><up><up><up><up><up><up><up> <enter>`

## 4. Edit Buggy Code

In order to get the screen below, I decided to edit the file with `nano ListExamples.java`. `vim` would also work in this case but I prefer using `nano`.
Here I was able to use `<tab>` to bypass typing `ListExamples.java` in full. 

<img width="830" alt="Screenshot_20230225_011224" src="https://user-images.githubusercontent.com/97120058/221381102-1f8b6d8d-cdac-440b-a4a9-ef335e35c727.png">

Once I was at this screen, I used the `<down>` and `<right>` arrow keys to navigate to the bug-causing code and make a change. After pressing `ctrl+X` to exit,
I was prompted with this next screen. I then typed `Y` and then `<enter>` to save the changes to the file under the same name as before, overwriting the file contents.

<img width="425" alt="Screenshot_20230225_012322" src="https://user-images.githubusercontent.com/97120058/221381242-4e03b737-aad2-4e62-ad0d-f349ecc6aa3c.png">

<img width="418" alt="Screenshot_20230225_012340" src="https://user-images.githubusercontent.com/97120058/221381249-ae7e85b4-b959-48c8-bae6-4ea1c0dfec81.png">

After this I ran the command to compile all .java files which was luckily earlier in my command history this time.

Keys Pressed: `nano Li <tab> .java <down>...<right>... <ctrl+X> <Y> <enter> <up><up><up> <enter>`

## 5. Run Tests Demonstrating Success

<img width="757" alt="Screenshot_20230225_011151" src="https://user-images.githubusercontent.com/97120058/221381405-7d32ac5d-c132-46a5-9d96-6a5904c03225.png">

This command is identical to the first time this was run, only now it was nicer because the command was earlier in my bash history.

Keys Pressed: `<up><up><up><up> <enter>`

## 6. Commit and Push Changes

This was straightforward except for pushing the changes. This is where step #2 got its revenge the first time I attempted this lab on my own.

<img width="399" alt="Screenshot_20230225_011439" src="https://user-images.githubusercontent.com/97120058/221381516-58d1bf9a-3999-40af-bd30-94ace9cdc9d6.png">

These commands were identical for both attempts. I used `<tab>` to save time typing for `git add`.

On the first attempt, because I accidentally cloned using the https linked repository as opposed to the ssh linked repository.
I configured my github account to allow ssh linked repositories during the lab, but I had forgotten to clone using the ssh link.

Failed push when using http cloned repo:

<img width="900" alt="Screenshot_20230225_011718" src="https://user-images.githubusercontent.com/97120058/221381663-683b9f18-149e-4e2d-992f-11295d87ec4a.png">

Sucessful push when using ssh cloned repo:

<img width="657" alt="Screenshot_20230225_012518" src="https://user-images.githubusercontent.com/97120058/221381683-5895337d-1171-47a1-b94c-6466a02f8e7d.png">

Although frustrating, I decided to screenshot both results as this would remind me to check how I clone repositories in the future.

Proof that the push was successful:

<img width="452" alt="Screenshot_20230225_012543" src="https://user-images.githubusercontent.com/97120058/221381708-d9b7fa57-aa34-44fa-83e1-a1da0d3331a4.png">

Keys Pressed: `git add L<tab>.java git commit -m "File Fixed! :)" git push `






