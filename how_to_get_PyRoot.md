# How to get PyRoot

## Getting the correct python environment 

So you’ve managed to get the first program cloned but the program you have isn’t running because you need something called *PyRoot*.  No need to fear with these step by step instruction you too will get a running version of the very first code for this project!

1. `ssh` into nero or whichever server you are using
```
<Username@Laptop> $ ssh username@nero.stanford.edu
```
2. The first thing we need to check is to see if you are using the correct shell so we don't get a syntax error. Use the command 
```
<Username@nero> $ echo $shell
``` 
and if you get anything other than `bash` (such as `tcsh`) then we need to change your shell so the *.bashrc* file can be properly read. **NOTE** if you wish to use the `tcsh` shell then this document is not for you!!

3. Use command 
```
<Username@nero> $chsh -s /bin/bash
``` 
it will prompt you for your password and voila your shell has been changed!

4. `<Username@nero> $ ls -a` in your home directory.  (if you need to get back there simply use the `$ cd` command)
5. You should see a program called *.bashrc* open it with your prefered terminal text editor (this author prefers pico due to its simplicity) the command would be 
```
<Username@nero> $ pico .bashrc
````
6. Once opened go down below the second comment of `# User specific aliases and functions` and type in the following commands (you may copy and paste)
```
Export PATH=$PATH”:/soft/anaconda/bin”
Source activate IPyRoot
```

7. Save the file and exit out. (for pico use the **WriteOut** command to save and exit out of the file using **ctrl o** to save and **ctrl x** to exit) 
8. Use command 
``` 
<Username@nero> $ source .bashrc
``` 
and if you don’t get a error message then congrats! You just specified a path and you should try running your code.  To make sure that it works type in
```
<Username@nero> $ python
>>> import ROOT
```
This is to get a python shell running in the terminal and to get PyRoot imported so you can read `ROOT` files.  If you didn't get any error messages then congrats!! You just successfully imported `ROOT` and are ready to read in the data files!