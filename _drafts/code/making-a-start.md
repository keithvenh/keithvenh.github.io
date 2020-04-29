---
layout: post
date: 2020-04-29
author: Keith VenHuizen
tags: coding web-dev command-line
title: "Makning a Start in Programming"
subtitle: "Taking your first step into learning to write code."
permalink: /coding-nomad/making-a-start
---

## Outline

1. Introduction
    1. Getting started can be the most difficult part. Where to start can be one of the most overwhelming things to answer. Many people start in the middle, because it builds a feeling of success, but then get lost. I'm starting where I think it is logical to start. The beginning of any new program.
    2. Assumptions: linux (maybe mac), probably not windows. Google is your friend. 
2. Fire up your terminal
3. Learning some commands
    1. what are directories
    2. viewing your directory
    3. viewing files in your directory
    4. making a new directory
    5. changing directories
    6. creating a new file
4. Conclusion
    1. Where we started
    2. what we learned
    3. where we are headed next

# {{ page.title }}

{{ page.subtitle }}

## Introduction

### My Philosophy

Perhaps the hardest part about any undertaking is the first step. There is a Chinese proverb that reads: "A journey of a thousand miles begins with a single step." There are countless places and directions that your programming journey can take you, but you have to take the first step at some point. Many people don't take the first step on the journey to coding because they aren't sure what it is.

There are an unlimited number of tutorials to follow online, numerous books on the shelves of bookstores, dozens of different languages, and it all adds up to a sense of overwhelm that paralyzes us from taking that first step into programming. My hope is that this tutorial is a simple first step that will launch you into all the steps that follow.

To be honest, there are many different options when it comes to which first step to take. I've done a number of different tutorials and classes, and they all seem to start somewhere different. None of them are wrong, but none of them fit my learning profile very well, either.

I like structure. A beginning and an end. A template from which you can deviate as needed. I haven't really found a tutorial like that [LearnEnough](https://learnenough.com) by Micheal Hartl is probably the best I've encountered, especially when it was free, but even he gave me information well before I needed it.

I want to take a "just-in-time" approach to these tutorials. My goal is to walk you through the provess of developing a website and a program from beginning to end, and I want to give you the information you need "just-in-time." I don't want to give you a command line skill that you won't use until you become an expert. I want to give you the one or two commmands you need now, and when we get to the point that you need to ``` pipe ``` or ``` grep ```, then I will give them to you at that time. 

You will better learn and remember the things you have to use, and this will stem the tide of overwhelm. You will use and remember the things you're being taught, and never realize there are dozens of commands you won't need that you haven'y learned (yet).

So, let's get started!

### My Assumptions

I had to make a few assumptions when writing these tutorials. The first and most obvious is that you know how to use a computer, keyboard and the internet (especially Google). These are fairly safe assumptions considering your desire to to learn to code.

The assumption that will cause the most hang-ups is that you are using a Linux Operating System. If you're not, it is likely that you are using a Mac or a Windows. Mac users should be fine with this tutorial as it, too, uses Unix as its base. Most, if not all, of the information in these tutorials should work for a Mac user, but I can't make guarantees, because I am using Linux.

Windows users are at more of a disadvantage. I think that by using VS Code, which I will talk about soon, you too can use the built in terminal of that program and successfully complete all these tutorials, but I am less confident about the Window user than the Mac user.

It is my desire to write up some posts to ensure that all platforms can equally access the tutorial, but that isn't a reality yet, and so you can now consider yourself warned.

## Step 1: The Terminal

The image of a computer programmer or hacker pounding at his keyboard and the black and green screen doing unbelievable and magical things is a favorite of the movie and television industry. It makes software development or web development seem so mystical and alluring. The reality is less intimidating, but no less exciting. 

You have on your computer something known as a GUI, which stands for Graphical User Interface. It is how you interact with your programs, folders, files and almost anything else you want to do on your computer. But before GUIs existed there was the terminal. The terminal still exists, but, thanks to Hollywood, it is scary and dangerous and only for professional computer programmers.

The terminal is not as scary as it seems, and while you can do things that would not be good for your computer, it would be very difficult to do so by accident. The first thing I do when I want to start a new project is fire up my terminal. In fact, I've become so comfortable using my terminal that I have set my computer to open a terminal window on startup. (I know! I'm so cool now!)

It's your turn now. It's time to fire up that terminal. Go Ahead. Don't be afraid. I know you can do it! You've trained your whole life for this! Use your GUI to locate the program named "Terminal" and launch yourself into the great big world of being awesome!

WOW! You did it! Welcome to the exclusive club of terminal users! Now lets get down to business.

### Folders or Directories?

Okay. It's a trick question. They're the same thing. A directory is just the original and technical name for a folder. Your GUI displays a folder icon, which is where folders got their most often used name, but a directory is the same thing. It's a folder that you can use to store multiple files and even other directories (or folders). Now, get ready for some terminal action! The first thing we need to learn how to do is figure out where in our computer we currently are in the terminal. We want to know what folder, or directory, we are currently in. This helps us to navigate to the folder we want to be in.

#### ```pwd```

In your terminal type ``` pwd ```, then hit ```enter``` or ```return```

```bash
$ pwd
/home/keithvenh
```

Let's talk about what we're seeing here. First, you likely see some form of username construct before a ```$``` in your terminal. It could be something like this ```username@username:~$```. This is simply called the pompt. When you see this, you know that your terminal is ready to accept a new command. Whenever I add code for you to add to the terminal, I'll just shoten it to the ```$``` for brevity and clarity. Your prompt is unique to you, so adding mine to every command in the terminal isn't helpful.

```pwd``` stands for "print working directory". In other words, tell me what folder I am currently in. The terminal is happy to ablige, and it spits out the result. For me, it is ```/home/keithvenh/```. For you, it is probably fairly similar. Following the pattern of ```/home/username/```. This is beacuse when you fire up a terminal for the first time, it starts you in your home directory. It is essentially your folder where everything else is stored, including your Desktop folder.

It is great to know which folder we are in, but we need to know at least two more things. What else is in this directory, and how to change to a different directory.

#### ```ls```

One of the most common things you will do in your terminal is list the contents of a directory. It's like perusing the list of folders and files on your computer. You have a folder named "Funny Memes", and inside you can see that you have a folder named "Cats", and a file named "dog.jpg". Your GUI makes it easy to see what is in your current folder, and so does the terminal. The cammond you need is ```ls```, which stands for list. In your terminal type ```ls``` and press ```return```

```bash
$ ls
// Your output will vary in length and content
```

Your terminal should have output a list of different files and directories. In this instance, you probably have a "Documents", "Downloads" and "Desktop" folders. Thesee are likely listed in a certain color or are bolded. You may also have files like "notes.txt" or "background.jpg". These are likely a different color or boldness than your folders.

The specifics of your output aren't as significant as recognizing the different between a directory and a file in the output, because next we are going to create our own new directory.

#### ```mkdir```

Now we know how to view what directory we are in, and view the contents of that directory. The next step is to create our own directory for our programming course. For this, we need the ```mkdir``` command. The ```mkdir``` command, however, needs an argument to tell it what to name the new directory. In our case, lets name it "projects." In your terminal run the command ```mkdir projects```.

```bash
$ mkdir projects
// this command has no output
```

Because this command has no output, we need to run ```ls``` again to check that it created our new directory.

```bash
$ ls
// should include our new directory
```

After running ```ls```, scan through the output and make sure you have a directory titled "projects". Having the new directory for our project is great, but how do we change into the new directory? In your GUI, after creating a new folder, you would double click on it. In the terminal, the equivalent is the ```cd``` command.

#### ```cd```

```cd``` stands for "change directory", and like the ```mkdir``` command, it requires an argument. We need to tell ```cd``` what directory we want to change to, in this case "projects."

```bash
$ cd projects
// this command has no output
```

While the ```cd``` command has no output, you likely did notice a change in your terminal. It is likely that your prompt changed from ```username@username:~$``` to ```username@username:~projects$```. Whether or not your prompt changes isn't important, though. what is important is that we did in fact change to our new directory. If you'll remember back to the start of this lesson, you can check this witht he ```pwd``` command.

```bash
$ pwd
/home/keithvenh/projects
```

If you're in the new directory your output should be similar to the above. Our new directory should be empty, that is, we shouldn't have any files or folders in this directory yet, because it is new. to check this, we can use the ```ls``` command.

```bash
$ ls
// usually outputs a list of directories and folders, but should output nothing since our directory is empty.
```
## Conclusion

Well, we started knowing nothing about the terminal, and now we know more than most people will ever know in their lives. Most people will never run a single command in a terminal. You've learned four of the most basic and important. ```pwd```, ```ls```, ```mkdir [directory name]```, and ```cd [directory name]```.

At the beginning of any project, we will almost always start by creating a new directory to hold our project and changing to it. As you become familiar with the layout of your directories, you are likely to use ```pwd``` and ```ls``` less and less, not because they aren't important, because your brain is smart like a computer and can remember what directory you are in and what directoreis and files are there with you. The good news is that you will always have ```pwd``` and ```ls``` in your back pocket to help you if you ever get lost.

Now that we know how to get around our file system, the next step is to create our first file, and connect it to a versioning software.

Until next time, brag to all your friends about your new-found terminal expertise!