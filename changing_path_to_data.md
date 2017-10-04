# Getting the Code to Work
So you’ve ssh’ed into nero, cloned the repository, changed the *.bashrc* and are finally ready to work on the code!  But wait! When you type 
```
<Username@Laptop> $ ssh username@nero.stanford.edu
<Username@nero> $ cd /scratch/username/Example_Noise
<Username@nero> $ python test_1.py
```

into the command shell you get an error. As long as the first thing you see after that command is `hello world` then you are on the right track.  Most likely what has happened is that you are not specifying the correct path to the data that your code reads in.  Type in 
```
<Username@nero> $ pico test_1.py 
```

to get a look at the code.  One of the first commands should be 
```
print(“hello world”)
```

and right below that command is where we need to specify exactly where the data is that the program will pull from.  Both the `merge` and `calib` lines should be identical.  Once you have finished specifying the path on both the `merge` and `calib` files you should be able to run your code and get a whole jumble of numbers and have created 15 pdf of graphs you can’t look at but hey! Its progress.
