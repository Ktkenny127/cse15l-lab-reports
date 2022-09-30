#How to install VScode to remote connecting

## Installing VScode
To start off you must got to [](https://code.visualstudio.com/) to download the VScode for mac and go throught the wizard! Once you are done with that you should open VSCode and it should look like the picture below

Once that is done you are going to got to the top of VScode and click on the **Terminal** and you are going to click on it and select **New Terminal**
 
## Remotely Connecting
Once a terminal is now open you will need to go into the terminal and type 
`ssh cs15lfa22jt@ieng6.ucsd.edu` but the *jt* will be your own personal code. One that happens you will need to type your password in. The keystokes are being monitored when you put your password in but it will not show. If it is your first time logging intoThe image below shows what text will come up if you are connected to the server.

## Trying Some Commands
 Now that you are in a server and are connected try running these commands on your computrer and the remote coimputer
-cd ~
-cd
-ls -lat
-ls -a
-ls <directory> where <directory> is /home/linux/ieng6/cs15lfa22/cs15lfa22abc, where the abc is one of the other group members’ username
-cp /home/linux/ieng6/cs15lfa22/public/hello.txt ~/
-cat /home/linux/ieng6/cs15lfa22/public/hello.txt

I should look similar to the picture above whether you have the commands in your personal computer or the server.

## Moving Files with scp
    Now you must creat a file called `WhereAmI.java` in VScode and then you have to put this into the file:
     # class WhereAmI {
        public static void main(String[] args) {
        System.out.println(System.getProperty("os.name"));
        System.out.println(System.getProperty("user.name"));
        System.out.println(System.getProperty("user.home"));
        System.out.println(System.getProperty("user.dir"));
    }
}

Complie and run this on your main computer with the commands below.
 
     # javac WhereAmI.java
     java WhereAmI

   Once you do that you are now going to use scp to transfer a file from your computer to the remote computer. Youre going to type `scp WhereAmI.java cs15lfa22jt@ieng6.ucsd.edu:~/` with your own letters. Now 

## Setting an SSH Key

## Optimizing Remote Running
