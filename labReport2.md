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

Because the server is already started abd deployed, there is no need to call Server.start() again.
Other than that, the code that is called and procedure for adding an additional message is the same as adding the first.


