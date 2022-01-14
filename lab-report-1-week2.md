# Introduction

This blog contains a tutorial on how to log onto a course-sepcific account on `ieng6`. Each step be separated and will include a screenshot or multiple of them as well as a brief description of what to do in that particular step. Let's get started!




# Step 1: Intalling VSCode

VSCode is an IDE (integrated development environment) that allows for the writing, editing, and compiling of code for the purpose of software development. To install VSCode, we first go to [this website](https://code.visualstudio.com/), where we will see the page shown below.

![Image](https://user-images.githubusercontent.com/81746604/149571957-37288d90-520f-4f81-ba33-8dc61084df81.png)

Then, we install VSCode and then approach approach a fresh window such as the one below.

![Image](https://user-images.githubusercontent.com/81746604/149572411-15ebb83e-5a99-4935-8d82-d64fa28a5aed.png)

To create a new file, press the "command" and "N" keys together and select the programming language of your choice.




# Step 2: Remotely Connecting

To remotely connect, using course-specific account is required, which can be found using this [this link](https://sdacs.ucsd.edu/~icc/index.php) and finding your account in the format `cs15lwi22zz`, where `zz` is specific to your account. Once completed, open up VSCode and open up the terminal. Type `ssh`, add a space, type your account, and immediately follow it with `ieng6.ucsd.edu`. 

![Image](https://user-images.githubusercontent.com/81746604/149580207-324c9e6b-8367-4e24-b485-a85ed0c398b2.png)

The next steps are to type `yes` when a pop-up message notifying you that a new connection will be established to a server and then type your password, all of which are shown below.

![Image](https://user-images.githubusercontent.com/81746604/149580287-e80bb037-3923-41b2-99e2-4f0b01cc6e36.png)




# Step 3: Trying Some Commands

Some of the commands allow you to navigate through paths and folders is through commands such as `cd`, `ls`, `mkdir`, and `cp`. Below, a list of commands as well as their functions is provided. Also, for the sake of simplification, a picture of the commands being run on the computer as opposed to the remote computers in the CSE basement is provided.

* `cd ~` - sends you back to the base directory
* 'pwd` - prints the current directory (gives the absolute path)
* ls` - prints out the name of all files in the current directory
* `mkdir`- creates a folder in the current directory 
* `cp` - makes a copy of the file (sometimes does not work in server if the file can't be copied for security reasons)
* `scp` - moves files or directories between a local and a remote system or between two remote systems

![Image](https://user-images.githubusercontent.com/81746604/149590659-0da0019b-a150-4a03-add9-2384774568fd.png)


  
  
# Step 4: Moving Files with `scp`

One of the commands when dealing with files is `scp`, which takes a file and moves it from one location to another location. To move a file from your computer to another server, like the CSE building basement, use the syntax `scp`. The below picture includes a screenshot of a Java file that was created as well as the code that moves the file from the CSE server to the local computer. As we can see, after moving the file from the local computer to the CSE basement computers, we type `ls` and see that the file is in our home directory.

![Image](https://user-images.githubusercontent.com/81746604/149584082-12c6ebb4-6786-428f-a3cb-a716c43d1038.png)

![Image](https://user-images.githubusercontent.com/81746604/149584144-7e8cfb3e-0894-438b-bf7b-2cb8ceabdd38.png)



# Step 5: Setting an SSH Key

To look for time-saving ways to copy a remote server with `ssh` and `scp`, we can instead utilize `ssh` keys where we create pairs of files called "public key" and "private key," using the `ssh-keygen` syntax. By copying the public key onto the server and the private key onto the local computer, the `ssh` command then prevent you from having to constantly enter your password.

![Image](https://user-images.githubusercontent.com/81746604/149586196-e243d08e-16de-49b4-9bf8-1fc8336f7813.png)

After running `ssh-keygen`, we can now copy the public key to the `.ssh` directory according to our course-specific account and ultimately `scp` without entering our password.

![Image](https://user-images.githubusercontent.com/81746604/149586280-22482820-d161-4b03-a28b-12812e443dea.png)


# Step 6: Optimizng Remote Running

One of the ways to save time in remote running is to run multiple commands on the same line For instance, running the `WhereAmI.java` file can be done on the local computer as opposed to the CSE basement servers. The following picture includes how the file is able to be run on the servers as opposed to having to constantly login and out back and forth.

![Image](https://user-images.githubusercontent.com/81746604/149590378-71712d5f-73df-498f-8899-b95413eeba20.png)

The usage of semicolons allows us to pass multiple commands in at once and have the computer perform them in the order of which they are separated. By doing so we are able to run the actual file from our local computer and save time without having to constantly interact with the login portal of the servers.


