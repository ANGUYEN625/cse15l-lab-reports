# Tutorial for Logging into a Course Specific Account for `ieng6`:

## Step 1: Installing VSCode

Go to the Visual Studio Code download page here: [VS Code Download](https://code.visualstudio.com/Download). Download the program specific to your system. 

![Image](./Screenshot%20(345).png)

## Step 2: Remotely Connecting

Open up the terminal in VS code and type in `ssh <username>@ieng6.ucsd.edu`. Then enter the password for your **course-specific** account. The terminal should look like this:

![Image](./Screenshot%20(352).png)

## Step 3: Trying Some Commands

Now, try running some commands. Some examples would include: 
* `cd` - moves you to a certain directory (stands for *change directory*)
* `ls` - *lists* all of the files + directories of the directory you are currently in
* `cat <filename>` - reads the *contents* of the file you put

## Step 4: Moving Files with scp

In the terminal, go to the directory that contains the file you want copied. Then enter the command `scp filenameofCopy <username>@ieng6.ucsd.edu:~/`. Enter your password. This copies the file into the remote directory. Now if you log back into the remote server and type in `ls`, the file should show up. 

![Image](./Screenshot%20(169).png)

## Step 5: Setting an SSH key

Enter the command `ssh-keygen`. This creates a public key (that goes on the remote server) and a private key (that goes on your personal device). The terminal should look like this: 

![Image](./Screenshot%20(509).png)

After doing so, your public and private keys will be created as files that are stored on your device. Now you have to copy the *public* key onto the `.ssh` directory on the server. Log into the remote server and then type in the command `mkdir .ssh`. Then log out and type in `scp <path of public key> <username>@ieng6.ucsd.edu:~/.ssh/authorized_keys`. Now it should automatically log you in without a password.

## Step 6: Optimizing Remote Running

There are some ways to optimize running commands on the remote server:
* Running remote commands or files surrounded by quotes on the same line as your login. This will automatically run the command and exit the server at the same time.

![Image](./Screenshot%20(588).png)

* Run multiple commands on the same line by dividing them with semicolons

* A combination of both running commands with quotes on the log in and running multiple commands separated by semicolons.

![Image](./Screenshot%20(589).png)
