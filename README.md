01_Git_and_Intro
================

Practice with basic git functions, and intro to study of Data Structures

Reading
=======

**Version Control with Git, 2nd Ed**. Loeliger and McCullough. 

http://proquest.safaribooksonline.com/book/databases/content-management-systems/9781449345037/version-control-with-git/id302681?uicode=ohlink (Free access through www.lib.miamioh.edu, but limited to 100 simultaneous users across all OhioLink. I recommend downloading/printing the required readings ahead of time, just in case.)

Read only the following:

1. Chapter 1
  * Background
  * The Birth of Git
2. Chapter 3: Getting Started
  * Intro
  * The Git Command Line
  * Quick Introduction to Using Git (read all sections)
  * Configuration files (Intro only, may skip part on aliases)
3. Chapter 4: Basic Git Concepts
  * Basic concepts (read all)
  * Object store pictures
  * Git concepts at work (read all)
4. Chapter 21: Git and Github
  * Repo for Public Code
  * Creating a GitHub Repository
  * Forks
  * Creating Pull Requests
  * Managing Pull Requests
  * Coding Models

**Open Data Structures in C++**. Morin, edition 0.1G-beta

http://opendatastructures.org/ (Free access. I recommend downloading the PDF version.)

Read the following:

1. Chapter 1 (pp. 1-21)

Homework
========

1. Create an account with github.com. You may select the free account. If you want to get some free private repos, you may apply at https://github.com/edu
2. Go to https://github.com/MiamiOH-CSE274/01_Git_and_Intro and fork the repo, which will create a copy of it in your github account.
3. Install git on your computer, if you do not already have it. I recommend installing http://windows.github.com/ if you use windows, or http://mac.github.com/ if you use Mac. **HOWEVER, I highly recommend using the command-line tools for everything, and ignoring the GUI. I will not be providing help with configuring/using the GUI.**
4. Clone your repo from github to your computer. When you are at the web page for your repo, `https://github.com/[your github id]/01_Git_and_Intro`, you will see info about how to clone it. The easiest way is to go to the command line terminal, and type `git clone git@github.com:[your github id]/01_Git_and_Intro.git`
6. Complete the exercises below by modifying this file.
7. After you complete each answer, be sure to create a new commit with the changes (using `git add README.md` and `git commit -m` as appropriate). Also, be sure to upload to github frequently by using `git push`
8. If I don't see at least 4-5 commits on this homework, I'm going to be unhappy.
9. Once complete, send me a pull request. This is your official "turn in" of the homework, which I will grade.
10. Double check that you did the right thing by going to https://github.com/MiamiOH-CSE274/01_Git_and_Intro/pulls and making sure that your pull request is there, and looks like you expect. Optimism is the root of all evil.

Exercises   ***Collaborated with Gage Laufenberg
=========

#### 1. Based on the reading in the Git book, is it okay to keep your local copy of your repo on a USB drive and just carry it around? Explain why or why not. What about keeping it on the M: drive?

It is alright to carry copies of your repo around on a USB drive or on your local M: drive.  You will have the most up to date repo, and you will be able to push it to your github account at your choosing provided you don’t lose the flash drive or the M: drive doesn’t crash.  The downside to having a repo on a USB drive is that group collaboration will be stalled until you push the repo to github.

#### 2. Imagine that you come into the lab on the weekend to work on homework with friends, but you forgot to bring your USB drive with your repo on it. What should you do?

As long as the most updated repo has been posted on github (as you should do every time you or your group finishes working), you can clone the most recent repo from github to whatever computer you are working on.

#### 3. Morin, Exercise 1.1 (p. 25). NOTE: You should not actually implement the solution with code. Instead, explain your solution using English. Pay special attention to explaining which data structure you ought to use, and why.

1.1.1 —> To read input one line at the time, and then print in reverse order, store the lines as strings, add them using the stack push(x) function, and then pull them in reverse order from the stack (as stack is ‘Last in First Out’) using the pop() function.

1.1.2 —> To read the first 50 lines in reverse order, followed by the next 50 in reverse order, use a stack, adding the first 50 lines only.  From there, pop each line off from that stack, putting them into reverse order.  Create a new stack, with the next 50 lines in order, and pop those off of that stack.  Continue this method until there is less than 50 lines, and then add the remainder to a stack of unspecified length.  Pop the data off from that stack and you are finished.

1.1.3 —> Add the data to a queue until the queue reaches a size of 42.  After the queue is greater than or equal to a size of 42, add elements to the end of the queue using add(x), and remove the first using remove().  If the element you add is read as blank, print the line that was removed from the queue.

1.1.4 —> First, use find(x) to see if the element is already in the USet.  If it is, print the element.  This will help save on memory usage.  If it is not, use add(x) to add the element to the USet.

1.1.5 —> Use a Uset.  Add the element to a Uset using add(x).

1.1.6 —> Add the elements to an SSet that is sorted by length using add(x).  An SSet will already have the elements sorted from shortest to tallest so you need only print each value in the SSet using remove(x).

1.1.7 —> Add the elements to an SSet that is sorted by length using add(x).  Keep track of the number of times each element is printed.  An SSet will already have the elements sorted from shortest to tallest so you need only print each value in the SSet using remove(x), but check to see if the element is printed more than once.  If it is, print it that number of times.

1.1.8 —> Have two queues.  Add the even numbered lines to the first queue, and the odd numbered lines to the second.  Create a third queue, adding the entire contents of the first queue, followed by the second queue.

1.1.9 —> Add the elements to a USet.  The elements will not be in any order, so you can remove the elements in an unordered, random order.

#### 4. Your choice: Morin, Exercise 1.2, 1.3, or 1.4 (pick one)

Note: You should not need to write any real computer code for any of these. Instead, explain how you would approach the problem using a combination of English and pseudocode. The goal is to write something that is understandable by any programmer, even if the two of you have never used the same computer language. (In other words, assume the other person does not know the syntax of Java or C/C++, but knows the basic programming constructs such as for loops, if statements, variables, and so on.)

1.1.2 —> If you add the elements to a stack by using pop(x), we can remove them in reverse order.  By popping, or using pop(), you remove the last element, leaving only the prefix of the Dyck word.  Add all the elements of the stack together using a for loop.  If the sum of the stack at that point is less than zero, the prefix sum is less than zero and the word is not a Dyck word by definition.  If the sum is greater than or equal to zero, pop() the last element off and add the sum of the stack again.  Do the same tests for the sum as before.  If you reach the first element again and the word has not been declared a non-Dyck word, we are able to say the word IS a Dyck word.

#### 5. Define/explain each of the following terms, as they relate to git.

1. blob - A blob is a binary file containing only the information relevant to building the project/the source files.
2. tree - "A tree object represents one level of directory information. It records blob identifiers, path names, 
and a bit of metadata for all the files in one directory. It can also recursively reference other (sub)tree objects
 and thus build a complete hierarchy of files and subdirectories." ("Version Control with Git")
3. commit - Adds all the files you’ve changed and added to your repo with a message before you push your new repo to github.
4. repo - A repository.  A place to store projects and files using git.
5. hash - A specified object ID.
