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

Here, the grep command successfully finds all the text files in written_2 despite using `.TXT`.
This can be useful when the casing of file names is unconventional or unknown.


Usage Example 2:

<img width="514" alt="image" src="https://user-images.githubusercontent.com/97120058/218366647-aa115c9b-b73c-4d26-a040-73a5ac7f46c3.png">

Same as the first example, the grep command successfully operates despite strange casing.
This is useful as it shows that `-i` works even with a mix of upper and lowercase in the pattern.


Source: grep manual provided using `man grep` command


## Give Me What I'm NOT Looking For

By using `-v` in your grep command, you can run the inverse of the grep command, 
meaning that grep will return all lines that do NOT match the given pattern.

Usage Example 1:

<img width="507" alt="image" src="https://user-images.githubusercontent.com/97120058/218380163-ad014cb3-6960-4617-81bd-cfc3930a6c2d.png">

This shows every file in written_2 that is NOT a text file, which can be useful to know.

Usage Example 2:

<img width="507" alt="image" src="https://user-images.githubusercontent.com/97120058/218380424-1f47e339-bf24-4459-adbf-d137cb8b7dca.png">

This shows every file in written_2 that does not contain "Italy" in its name.
Just as it can be useful to prove what is in a list, it can be useful to prove what is not in a list.


Source: grep manual provided using `man grep` command


## Skip a Step

If you use `-c` in your grep command, the normal output of the grep command will print a count of matching lines for each input file.
This means that instead of using `wc` as we have done so far, we can simply read the file returned.

Usage Example 1:

<img width="503" alt="image" src="https://user-images.githubusercontent.com/97120058/218382483-e16da4fa-da71-469f-805d-3cde4aa83050.png">

Here the file produced by grep just contains the count of .txt files.
This is more organized than using `wc`.

Usage Example 2:

<img width="514" alt="image" src="https://user-images.githubusercontent.com/97120058/218382716-b0ee7c0e-87ea-4023-9ef7-494e158ff334.png">

This command could also be very useful if the count of files needed to be displayed or used in a bash script.


Source: grep manual provided using `man grep` command

## Exactly

By using `-x` in a grep command, grep will return only the lines in a file that exactly match the whole line.

Usage Example 1:

<img width="505" alt="image" src="https://user-images.githubusercontent.com/97120058/218383277-3f7ad500-e21c-4b4a-81df-0c3fc5db3aa7.png">

A fair warning, our normal method of finding text files will not work here.
This command is useful if you really know what you're looking for.

Usage Example 2: 

<img width="564" alt="image" src="https://user-images.githubusercontent.com/97120058/218383626-e141b168-5a41-4724-a64d-946fac12688e.png">

As seen here, this modification of grep is only useful if you really know what you're looking for. 

Source: grep manual provided using `man grep` command







