# Lab Report 3
This lab report will be focusing on researching `find` command online. I will be finding 4 interesting command-line options or alternative ways to use the command `find`. 

**Note that for some of the examples, I will be combining the usage of more than one command line options used with `find` in order to explore different combinations of how to use `find`**

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

### Example 1: Using -not by itself with find

Here are all the files that are within `docsearch/technical/government/Media`. Those are a lot of files that we might not even need all of them. Say for example we don't need any of the ones containing the letter `F`. 

![Before not](pictures/fullgovpic.png)

![Not f](pictures/findnotf.png)

In the picture we can see it filters out all the files within `docsearch/technical/government/Media` that start with capital F. It is case sensitive and goes through each file inside of the directory we are in. 

## 2: Using `-and`
**Source**: [Using and with find](https://adamtheautomator.com/bash-find/#Combining_Two_Conditions_with_the_-and_Operator)

Now that we know how to filter out words we are not looking for, what if we have more than one keyword of the file we are looking for? That's where `-and` comes into use and can be useful when trying to find files that contain more than one key word of what you are looking for. 

### Example 2: Using -and by itself with find

![biomed full list](pictures/biomedfulllist.png)

Here we can see there are a ton of txt files within biomed! Let's try filtering out the ones we are looking for using keywords such as `gb` and `12` in order to just get the files containing that. 

![filtered biomed](pictures/findgb12.png)

We can see that using `-and` filtered out everything inside of the biomed directory and left us with anything containing `gb` and `12`! 

### Example 3: Combining the usage of `-and` and `-not`
What if we want to filter out words depending on what keywords we know NOT to look for. (Notice I said keywordS meaning multiple ones!) We can use `-not` and `-and` in a combination to filter out multiple key words on what we are NOT looking for. 

![Not and And](pictures/notand.png)

I kinda went a little crazy typing up the words I wanted to filter out from `biomed` (mainly because I want it to fit on a screenshot but that's beside the point!). Aside from showing the possibility of combining `-not` and `-and` I also demonstrated the fact that you can format it like a run-on sentence, allowing multiple keywords of words you are either trying to look for or NOT trying to look for! Pretty cool :D

## 3: Using find and `-delete` to remove files
**Source**: [Using delete and find together]([https://www.geeksforgeeks.org/find-command-in-linux-with-examples/](https://www.cyberciti.biz/faq/linux-unix-how-to-find-and-remove-files/))

We know by now that all the files that are within `technical/` are A LOT and at times it might be a hassle to find the one you want to remove. We can easily use `-delete` to remove a file if we know the general name of that file. Let's try removing a file from `government/Media`.

### Example 4: Using `-find` and `-delete`

![Deleting Philly](pictures/deletephilly.png)

The first part of the screenshot shows `government/Media` and in the fourth column we see a .txt file named `Philly_lawyers.txt`, say we do not know the full name of the file and can only remember that it starts with the word "Philly". We can see I run a line using `-find` and `-delete` with the only keyword i'm using is `Philly`. Once I run it we can see in the bottom fourth column that it no longer exists and was deleted based off of what I typed!.

### Example 5: Deleting Multiple files of the same name

![before](pictures/before.png)

We can see that we have multiple files within biomed that contain the keyword `research`. What if we want to delete all of those files and only keep the ones that have nothing to do with research. 

![after](pictures/after.png)

Here we can see that by using a combination of `-find` and `-delete` we are able to take away all of the txt files that had any mention of research in the name and are left with the ones that do not have it in the name.

## 4: Using `grep` along with `find`
**Sources** [Using `grep`](https://stackoverflow.com/questions/16956810/how-can-i-find-all-files-containing-specific-text-string-on-linux)

We have so far only been looking for files with certain names but what if we also want to look at keywords that are within said files. 

### Example 6: Using `grep` along with `find`
Let's say that we are withing `technical/911reports` and we are trying to find any .txt file that has a mention of `school` in it. There's not that many files inside of `/911reports` however each one contains a lot of text that it would just be inconvenient to go through each one individually and skim through until we find it. 

![School find](pictures/schoolfind.png)
Here we can see the command that I ran using `grep` in order to filter out which txt files did not contain the mention of the word `school`.

