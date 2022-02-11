# Group Option #3: Copy Whole Directories with `scp -r`

## Part 1: Copying Entire `markdown-parse` Director to `ieng6` Account

First, we need to show the files that are included in the `markdown-parse` repository before we copy everything to the remote server. The screenshot below includes all files that are in the repository in the local computer...

![markdown-parse repo picture](https://user-images.githubusercontent.com/81746604/153533655-b7c6fb2f-4fb2-4fbf-a14c-214c7cdf77b5.png)

Next, we use the `scp -r` to copy the directory to the remote server. I will be using my `cs15lwi22akd@ieng6.ucsd.edu` account in lieu of CSE 15L's demo remote server account to perform the copy. Additionally, since the resulting output of copying all files to the remote server is extremeley lengthy, two screenshots will be provided below, where the first picture will show the actual command on the command-line performing the copy along with some of the recursive copy functions being performed and the second picture will show some of the recursive copy functions being performed along with the last file being copies recursively. Thus, the two pictures below detail this process...

![markdown-parse repo picture](https://user-images.githubusercontent.com/81746604/153535172-224aa56b-07f5-4ecb-9ede-66fa0c02caa5.png)

![markdown-parse repo picture](https://user-images.githubusercontent.com/81746604/153535235-401d2d74-d57a-4dad-9592-72f3ec6c345c.png)


