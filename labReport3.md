# Interesting Ways in Which to Use the Grep Command

The `grep` terminal command stands for global regular expression print, and is most commonly
used for printing any lines that match a given pattern.

Source: [What Does Grep Stand For?](https://kb.iu.edu/d/abnd#:~:text=grep%20Global%20regular%20expression%20print,pattern%3A%20g%2Fre%2Fp)


In previous labs we have used this command in conjunction with the `wc` and `find` commands to count
all files that end in ".txt" like so:


<img width="492" alt="image" src="https://user-images.githubusercontent.com/97120058/218364959-1875c851-4998-4279-943a-1d2fb67e4b98.png">


But there are other unique ways that the grep command can be used and modified!


## All Caps No Problems


Adding `-i` into your grep command will cause grep to search for files that match the pattern regardless of case
of both the input pattern and the files searched.


While this isn't a very flashy command, it has its uses when you need to find what is in a file
regardless of upper case or lower case.


For the purpose of simplifying later examples, assume that the file `find.txt` contains the results
returned by the command `find ./written_2/* > find.txt`

Usage Example 1:

<img width="498" alt="image" src="https://user-images.githubusercontent.com/97120058/218366471-abe1f63d-5443-4da0-8dc2-bf065f38a900.png">


Usage Example 2:

<img width="514" alt="image" src="https://user-images.githubusercontent.com/97120058/218366647-aa115c9b-b73c-4d26-a040-73a5ac7f46c3.png">


Source: grep manual provided using `man grep` command


## Give Me What I'm NOT Looking For

By using `-v` in your grep command, you can run the

