# Logging into Course Account

## Installing VS Code
1. Download VS Code from [here](https://code.visualstudio.com/).
![VS Code Page](images/Week2/InstallVSCode.jpg)
2. After going through the installation process, open VS Code. You should see this:
![VS Code Startup](images/Week2/VSCodeStartup.jpg)

## Remotely Connecting
1. If you are using a Windows OS, then [install OpenSSH](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse)
2. Open your terminal (Command Prompt for Windows users)
![Terminal](images/Week2/Terminal.jpg)
3. Enter in the command `ssh $(YOUR_ACCOUNT)@ieng6.ucsd.edu`
   1. e.g. `ssh cs15lacz@ieng6.ucsd.edu`

   ![SSH](images/Week2/SSH.jpg)

## Trying Some Commands
1. You can now type commands into the terminal and press enter to run them
2. Here's a list of commands you can use:
   1. Change directory to home `cd ~`
   2. Change directory to given directory `cd $DIRECTORY`
   3. Show contents of current directory, listing all files and properties and ordering them by time `ls -lat`
   4. Show contents of current directory, showing all files `ls -a`
   5. Show contents of given directory `ls $DIRECTORY`
   6. Copy a source file to a destination `cp $SOURCE_PATH $DESTINATION_PATH`
   7. Display the contents of given file `cat $FILE_NAME`
   
Here's an example command run
   ![Commands](images/Week2/CommandsLS.jpg)
`
## Moving Files with SCP
1. SCP allows users to move files from one system to another. We will practice moving a file from our local computer to the remote server.
2. If you have been following this tutorial from top to bottom, then use the `exit` command to leave the remote server and return to your local computer on the terminal.

![Exit](images/Week2/Exit.jpg)
4. Create a file in your current directory
   1. I will be using `WhereAmI.java` for this example

   ![Files](images/Week2/Files.jpg)
5. To copy this file onto the remote server, enter this command `scp $FILE_NAME $(SERVER_URL):$(SERVER_PATH`
   1. e.g. `scp WhereAmI.java cs15lsp22acz@ieng6.ucsd.edu:~/`

   ![SCP](images/Week2/SCP.jpg)
6. Now you can log into the remote server and see your file there.
![Remote SCP](images/Week2/RemoteSCP.jpg)

## Setting SSH Key
1. If you have been following this tutorial from top to bottom, then use the `exit` command to leave the remote server and return to your local computer on the terminal.
2. Enter this command to create the SSH Key `ssh-keygen`
3. Enter the directory and file name you would like to save your ssh key
4. Do not add a passphrase
![SSHKey](images/Week2/CreateSSHKey.jpg)
5. SSH onto the remote server and create a .ssh directory on your home directory
![SSHDir](images/Week2/CreateSSHDir.jpg)
6. Return to your local computer and scp the PUBLIC ssh key to your remote server's .ssh directory
![Exit](images/Week2/Exit.jpg)
![SCPKey](images/Week2/SCPSSHKey.jpg)

## Optimize Remote Running
1. Multiple commands on the terminal can be run on one line using the semicolon (;)
   1. e.g. ![Multiple Commands](images/Week2/MultiCommands.jpg)
2. We can also run commands on a remote server from our local computer by providing a command after the ssh command.
   1. e.g. ![Remote Commands](images/Week2/RemoteCommand.jpg)
3. Combining these 2 ideas, we can copy a Java program from our local computer to the remote server and compile and run that Java program.

![Optimized Workflow](images/Week2/OptimizedWorkflow.jpg)