# Lab Report 3

## Streamlining SSH Configuration

Open the `.ssh/config` file

![Open](images/Week6/OpenConfig.jpg)

Add the SSH alias

![Add Alias](images/Week6/AddAlias.jpg)

Log into server using SSH alias

![Login](images/Week6/LoginAlias.jpg)

SCP Files using SSH alias

![SCP](images/Week6/SCPAlias.jpg)

Check SCP'd file on server

![SCPCheck](images/Week6/SCPAlias2.jpg)

## Setup Github Access from ieng6

Public Key on GitHub

![GitHubPublicKey](images/Week6/SSHKeyGithub.jpg)

Public Key and Private Key on ieng6
![ServerKeys](images/Week6/SSHKeyServer.jpg)

Running Git commands
![GitCommands](images/Week6/GitCommands.jpg)

[Link to Commit](https://github.com/Charlychee/cse15l-lab-reports/commit/8e04400d275072713fcff4b9a3f39013162c81e5)

## Copy whole directories with `scp -r`

Copying directory to server

![CopyServer](images/Week6/SCPServer.jpg)

Login and Compile and Run tests

![LoginCompile](images/Week6/LoginCompile.jpg)

Copy the whole directory and run the tests in one line.

![OneLine](images/Week6/OneLine.jpg)

`ssh ieng6 "mkdir -p ~/markdown-parser"; scp -r markdown-parser/lib markdown-parser/*.* ieng6:~/markdown-parser; ssh -t ieng6 "bash --login -c 'cd markdown-parser && javac -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar MarkdownParseTest.java && java -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar org.junit.runner.JUnitCore MarkdownParseTest'"`