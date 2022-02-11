# Group Option #3: Copy Whole Directories with `scp -r`

## Part 1: Copying Entire `markdown-parse` Director to `ieng6` Account

First, we need to show the files that are included in the `markdown-parse` repository before we copy everything to the remote server. The screenshot below includes all files that are in the repository in the local computer...

![markdown-parse repo picture](https://user-images.githubusercontent.com/81746604/153533655-b7c6fb2f-4fb2-4fbf-a14c-214c7cdf77b5.png)

Next, we use the `scp -r` to copy the directory to the remote server. I will be using my `cs15lwi22akd@ieng6.ucsd.edu` account in lieu of CSE 15L's demo remote server account to perform the copy. Additionally, since the resulting output of copying all files to the remote server is extremeley lengthy, two screenshots will be provided below, where the first picture will show the actual command on the command-line performing the copy along with some of the recursive copy functions being performed and the second picture will show some of the recursive copy functions being performed along with the last file being copies recursively. Thus, the two pictures below detail this process (the three dots represent the separation of the two screenshots)...

![markdown-parse repo picture](https://user-images.githubusercontent.com/81746604/153535172-224aa56b-07f5-4ecb-9ede-66fa0c02caa5.png)

**...**

![markdown-parse repo picture](https://user-images.githubusercontent.com/81746604/153535235-401d2d74-d57a-4dad-9592-72f3ec6c345c.png)


## Part 2: Logging into `ieng6` Account and Compiling/Running Tests

Now that we have the file copies, I can log into my `ieng6` account and try to find the `markdown-parse` directory using the `ls` command. The process of logging in and finding the directory is shown below...

![markdown-parse repo picture](https://user-images.githubusercontent.com/81746604/153535854-91e1d556-945f-4f33-ae68-d1f076a107f8.png)

We can compile and run all of the files on the command line through our remote server account. The screenshot below illustrates how we use the compiling and running commands to test our files. We compile both `MarkdownParse.java` and `MarkdownParseTest.java` files before running the `MarkdownParseTest.java` file. Thus, the screenshot below displays our tests...

![markdown-parse repo picture](https://user-images.githubusercontent.com/81746604/153539047-0f859ef2-4205-45c1-b71e-a4844bfe7257.png)


## Part 3: Combining `scp`, `;`, and `ssh` to Copy Directory and Run Tests

We will now try to save keystrokes by trying to combine the `scp`, `;`, and `ssh` commands from our local computer. Similar to Part 1, since the resulting output of copying all files to the remote server is extremeley lengthy, two screenshots will be provided below, where the first picture will show the actual command on the command-line performing the copy along with some of the recursive copy functions being performed and the second picture will show some of the recursive copy functions being performed along with the last file being copies recursively. Thus, the two pictures below detail this process (the three dots represent the separation of the two screenshots)...

![markdown-parse repo picture](https://user-images.githubusercontent.com/81746604/153541343-c18898ed-5412-40c0-8a58-5e6034bd325e.png)

**...**

![markdown-parse repo picture](https://user-images.githubusercontent.com/81746604/153541625-713ee372-c923-42d5-a17a-70df3391fdee.png)



