# Using Python on a Remote Computer

So you want to use an IPython notebook while using nero’s servers…  To do this we are going to need to do a special ssh into nero.  The command to do this is:
```
<Username@Laptop> $ ssh -L 8888:localhost:8888 username@nero.stanford.edu
```
This will essentially create a direct pipe from **port 8888** on your computer to **port 8888** on nero!

When you do this you will see essentially the same screen as if you had just normally ssh’d into nero.  Now you’re gonna have to move into the repository for example your scratch folder 
```
<Username@nero> $ cd /scratch/username/Example_Noise.
```
From here you’re going to start an IPython notebook 
```
<Username@nero> $ ipython notebook
```
what should pop up in the terminal is an elinks ipython notebook use **q** to quit out of there and now the terminal should be completely blank.

## NOTE

The default port for the `ipython notebook` command is port 8888 if you wish to use a different port on nero, like 8887, then the command is

```
<Username@Laptop> $ ssh -L 8888:localhost:8887 username@nero.stanford.edu
<Username@nero> $ cd /scratch/username/Example_Noise
<Username@nero> $ ipython notebook --port=8887

```

Now for the last step!  Simply go to your favorite web browser, like Google Chrome or Firefox on your laptop (not on nero) and type in 
```
localhost:8888
```
and an IPython Notebook should pop up for you to use!
