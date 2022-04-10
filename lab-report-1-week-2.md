# Lab Report 1: Remote Access Tutorial
Welcome to this tutorial on how to remotely access the computers in the CSE labs.

This tutorial will walk you through from installing VScode on you machine to setting up
**ssh keys** and **optimizing remote running**.

## Instaling VScode
* Visit the Vscode website at https://code.visualstudio.com and download the correct version for your machine

* Next follow the instalation steps and open up the application, as well as the terminal using the menu at the top.

* Your window should look like this:

![Vscode_SS](https://github.com/peds24/cse15l-lab-reports/blob/971af39a369df603a1735834e6300f77ad8ecfd0/VScode_ss.png)

## Remotely Connecting
* The next step is loging into your lab account and connecting to a lab computer remotely.

* In the terminal type/copy the following address: **cs15lsp22xxx@ieng6.ucsd.edu**

> **Note:** this is not going to be your account, the **"xxx"** is just a place holder, your specific account should have different letters there, be sure to use your account

* You will be promted by a password and the screen will look like this:

![PassWord]()

> **Note:** When typing your account password there will apear to be nothing on the screen being typed. This is a security feature of the remote access, make sure you type it in correctly and hit enter, it should register.

* This is what you will see after a successful login:

![GoodLogin]()

## Running some commands
* Next its time to play around with the directory and termianl commands, here are some you can try out:
    * cd --> returns the current directory
    * ls --> lists all items in directory
    * cd perl15 --> travels to the directory **perl15**
    * cd ~ --> backtravels one step (directory)

* Here is what the screen looks like after running all four of these commands:

[CommandRunning]()

### Moving files using SCP
* Now onto moving and copying files to the server computer. Using the following code create a file named
**WhereAmI.java** in VScode.

* Paste the following code to the file and once finished compile it using the integrated terminal using **javac WhereAmI.java**.

```
class WhereAmI {
    public static void main(String[] args) {
        System.out.println(System.getProperty("os.name"));
        System.out.println(System.getProperty("user.name"));
        System.out.println(System.getProperty("user.home"));
        System.out.println(System.getProperty("user.dir"));
    }
}
```
* Now back on the VScode terminal type the following command and hit enter:
`scp WhereAmI.java cs15lsp22zz@ieng6.ucsd.edu:~/`

* Now try to log back into the server computer and in the main directory type **ls**, you should see the new file listed there.

![moveFile]()




