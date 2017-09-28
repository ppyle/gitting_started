# Using Python on a Remote Computer

So you want to use an IPython notebook while using nero’s servers…  To do this we are going to need to do a special ssh into nero.  The command to do this is:
```
$ ssh -L 8888:localhost:8888 username@nero.stanford.edu
```
This will essentially create a direct pipe from **port 8888** on your computer to **port 8888** on nero!

When you do this you will see essentially the same screen as if you had just normally ssh’d into nero.  Now you’re gonna have to move into the repository for example your scratch folder 
```
$ cd /scratch/username/Example_Noise.
```
From here you’re going to start an IPython notebook 
```
$ ipython notebook
```
what should pop up in the terminal is an elinks ipython notebook use **q** to quit out of there and now the terminal should be completely blank.

Now for the last step!  Simply go to your favorite web browser and type in 
```
localhost:8888
```
and an IPython Notebook should pop up for you to use!
