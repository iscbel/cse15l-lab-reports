# Lab Report 3
This lab report will be focusing on researching `find` command online. I will be finding 4 interesting command-line options or alternative ways to use the command `find`. 

## What is `find`?
Before researching different/ alternative ways of using the command. I do want to review, (mainly for my sake), the purpose of using `find` and how it can be useful. In general, the `find` command allows us to be able to search for files and directories. For example if I open up a terminal in `Visual Studios` and run the find command just by itself with nothing else attached, it will start searching through ALL of the files since I did not specify what I was trying to find. 

![Going through files](/pictures/openfile.png)

This is just a small part of what bash was doing, I had to stop it from going through all the files because it was too much. 

So now lets try using `find` with a word attached to it to make it try finding more specific files/directories. 

![find desktop](/pictures/findesktop.png)

Here we can see there is significantly less files/directories that were found when we added a word next to `find`. It just filters what we're trying to look for. 

Now that I've explained a little basics on what `find` is used for, I will be showing my research on command-line options/ alternative ways to use the command and show 2 examples for each.

## 1: Using `-not`
**Source**: [Using not with find](https://adamtheautomator.com/bash-find/#Filtering_out_Files_with_the_-not_Operator)

In the write-up for lab report 3, we are told to use the files and directories from `./technical` so that is where I will be pulling the examples from. 

Using `-not` combined with `find` will be able to filter out anything we know we are NOT looking for. Or just remove certain files/directories in general to make it easier to find what we are looking for.

### Example 1

![Before -not](/pictures/fullgov.png)

Here are all the files that are within `docsearch/technical/government/Media`
