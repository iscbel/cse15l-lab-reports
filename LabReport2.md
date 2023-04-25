# Lab Report 2
In this lab report, I will be writing a web server called `StringServer` and finding a solution to one of the bugs that we went over in lab three.

## Part 1
In order to complete the first part of this lab report, I will be basing the code off from the `wavelet` code from the lab. For the web server `StringServer`, I I want to be able to keep track of a single string that will keep being added to depending on the incoming requests.

![StringServer](StringServerPic.png)

Explaining the code above: The code takes in the URL and checks if it contains `/`, which will then go and obtain the query by using `.getQuery()`. After that, we want to check the location of `=` in the string so we will be able to successfully seperate the message using `.substring()` and add it to our `webstring` variable of type string that will keep adding on to it and using a `\n` to put each message on a new line. 

Anything that is on the other side of `=`, the code will take it in as a string and add it in to our `webString` variable. 
