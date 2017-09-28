# Getting Started: .bashrc

## How to get PyRoot

So you’ve managed to get the first program cloned but the program you have isn’t running because you need something called *PyRoot*.  No need to fear with these step by step instruction you too will get a running version of the very first code for this project!

1. `ssh` into nero or whichever server you are using
```
$ ssh username@nero.stanford.edu
```

2. `$ ls -a` in your home directory.  (if you need to get back there simply use the `$ cd` command)
3. You should see a program called *.bashrc* open it with your prefered terminal text editor (this author prefers pico due to its simplicity) the command would be ````$ pico .bashrc````
4. Once opened go down below the second comment of `# User specific aliases and functions` and type in the following commands (you may copy and paste)
```
Export PATH=$PATH”:/soft/anaconda/bin”
Source activate IPyRoot
```

5. Save the file using the **WriteOut** command or **ctrl o** and exit out of the file **ctrl x** (note: these are the commands for pico)
6. Use command 
``` 
$ source .bashrc
``` 
and if you don’t get a syntax error then congrats! You just specified a path and you should try running your code.  If you did get a syntax error then try the command 
```
$ echo $shell
``` 
and if you get anything other than `bash` (such as `tcsh`) then we need to change your shell so the *.bashrc* file can be properly read

7. Use command 
```
chsh -s /bin/bash
``` 
it will prompt you for your password and voila your shell has been changed!

8. See bullet 6 again