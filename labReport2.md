# Servers and Symptoms and Bugs, Oh My!

In this tutorial I will be going through what I have learned through making and
deploying web servers, as well as troubleshooting bugs within programs.

## Creating and Deploying a Server

For this lab a substantial portion of the implementation for crreating a web server was provided to us
in the form of a `Server.java` file. The content of which is pictured below.

<img width="580" alt="Screenshot_20230127_010446" src="https://user-images.githubusercontent.com/97120058/215198490-669b352d-336b-43a9-9ae9-2d656f20829a.png">

We were instructed to treat this file as a blackbox, i.e. it is not necessary to know how the class works,
just assume that it does. 

Using this file I created a `StringServer.java` class that would append a message to a string each time a command like
`https://localhost:4000/add-message?s=hello` 

The implementation of `StringServer.java` is pictured below

<img width="611" alt="Screenshot_20230127_010959" src="https://user-images.githubusercontent.com/97120058/215200304-27a7a546-643c-4508-a2b4-75b20ee00ceb.png">

Here is a screenshot of the page visited after running `StringServer.java` and entering a message.

<img width="284" alt="Screenshot_20230127_125801" src="https://user-images.githubusercontent.com/97120058/215201243-142a7f0c-ed5e-46a2-ac56-4aba68e99229.png">

The following methods are called 
* Server.start() with the port number provided as a command argument and a new object of Handler()
* url.getPath()
* url.getQuery()

The relevant arguments for this class are the port number provided in the command prompt, the Url path that
is made in `Server.java`, and the command to add a string which is made in the url.

<img width="280" alt="Screenshot_20230127_010004" src="https://user-images.githubusercontent.com/97120058/215202679-712e69c9-fbda-4b94-9e71-163db7f86055.png">

The following methods are called 
* url.getPath()
* url.getQuery()

url.getPath() would return the path part of a url, in other words, the part of a url that does not contain the domain name.
url.getQuery would return the specific part of the path that contained the query denoted by `?`

Because the server is already started abd deployed, there is no need to call Server.start() again.
Other than that, the code that is called and procedure for adding an additional message is the same as adding the first.

## Troubleshooting Bugs with JUnit

Here I will provide a sample program that contains bugs along with another program that utilizes JUnit to pass failure-inducing input to the buggy program.

The program tested in this blog will be the `reverseInPlace()` method of the program `ArrayExamples.java` with the contents below

<img width="335" alt="Screenshot_20230127_060107" src="https://user-images.githubusercontent.com/97120058/215236368-aad0b51e-0503-4ea1-9dd6-f19c5ebb58c7.png">

The following test is a failure-inducing input for the program

```
@Test
public void testReverseInPlaceLong(){
  int[] input = {1, 2, 3, 4, 5}
  ArrayExamples.reverseInPlcae(input)
  assertArrayEquals(new int[]{5, 4, 3, 2, 1}, input);
}
```
This test does not induce a failure

```
@Test
public void testReverseInPlace(){
  int[] input1 = {3};
  ArrayExamples.reverseInPlace(input1)
  assertArrayEquals(new int[]{3}, input1);
}
```
After running both of these tests, the following is displayed on the console

<img width="594" alt="Screenshot_20230127_061512" src="https://user-images.githubusercontent.com/97120058/215236933-4b262eaf-fa76-4378-8036-29e74f296c61.png">

The issue with this program is that the array contents are being changed while the reversal is still taking place leading to error.
This is fixed by adding an array that stores the old contents of the original input array.

Before bug is resolved:

```
static void reverseInPlace(int[] arr) {
  for(int i = 0; i<arr.length; i += 1) {
    arr[i] = arr[arr.length - i - 1];
  }
}
```

After bug has been resolved:

```
static void reverseInPlace(int[] arr) {
  int[] template = new int[arr.length];
  for(int i = 0; i<template.length; i++)
  {
    template[i] = arr[i];
  }
  for(int i = 0; i<arr.length; i += 1) {
    arr[i] = template[arr.length - i - 1];
  }
}
```
Another approach that takes up less space:

```
static void reverseInPlace(int[] arr) {
  
  for(int i = 0; i<arr.length/2; i += 1) {
    int temp = arr[i];
    arr[i] = arr[arr.length - i - 1];
    arr[arr.length - i - 1] = temp;
  }
}
```
Proof that the bug has been fixed:

<img width="251" alt="Screenshot_20230127_062249" src="https://user-images.githubusercontent.com/97120058/215237328-ba405039-ae0c-4918-970a-e2828985af9d.png">

## Closing Thoughts

In the lab during week 2, it was really intriguing to learn about how to deploy a web server and how the code that handles url commands is made. 
It was fascinating to see the connections made between what's in a url and the program of a web page itself.

