# Tutorial for Logging into a Course Specific Account for `ieng6`:

## Step 1: Installing VSCode

![Image](./Screenshot%20(345).png)

Go to the Visual Studio Code download page here: [VS Code Download](https://code.visualstudio.com/) and download the program specific to your system. 

## Step 2: Remotely Connecting

Open up the terminal in VS code and type in `ssh <username>@ieng6.ucsd.edu`. Then enter the password for your **course-specific** account. The terminal should look like this:

![Image](./Screenshot%20(352).png)

## Step 3: Trying Some Commands

Now, try running some commands. Some examples would include: 
* `ls` - *lists* all of the files + directories of the directory you are currently in
* `cat <filename>` - reads the *contents* of the file you put

## Step 4: Moving Files with scp

In the terminal, go to the directory that contains the file you want copied. Then enter the command `scp filenameofCopy <username>@ieng6.ucsd.edu`. This copies the file into the remote directory. It should look likes this: 

![Image](./Screenshot%20(500).png)

## Step 5: Setting an SSH key

Enter the command `ssh keygen`.

## Step 6: Optimizing Remote Running

