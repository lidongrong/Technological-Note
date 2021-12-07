## A Short Memo on How to Run Python Script on Group Server

#### Log in Group Server

To log in to the server, use MobaXTerm->Session->SSH, with hostname 

```
stapc051.sta.cuhk.edu.hk
```

accountname+password see corresponding email.

#### Basic Linux Commands

After logging into the server, there is some linux commands are of vital use:

```
# construct a directory
mkdir filename

# move into a directory
cd directory

# move to another directory
cd /home/directory name

```

#### Run Python in Linux Server Using Conda

Python with multiple versions could be installed via conda. 

First, move to /home directory and call

```
$ source /opt/share/etc/miniconda3-py39.sh
```

Then create the python environment:

```
$ conda create -n environment-name python=3.9 
```

The version could be whatever, 3.5, 3.7, etc.

After creating the environment, the environment shall be activated to run Python scripts or pip install packages. To do this, use command:

```
$ conda activate environment-name
```

**Example3.1**
```
# Create an environment named py39
$ conda create -n py39 python=3.9
$ conda activate py39
```

After activating the environment, a Python script can be runned using:

```
python ScriptName.py
```

Or can just type in

```
python
```

to enter interactive environment.

#### Keep Tasks Running by Tmux

By adopting tmux, our tasks can be run remotely even if we've lost our connection.

We can create multiple sessions using tmux (so that perhaps we can run multiple tasks in parallel?)

We can start a new session by the command:

```
tmux new -s <session-name>
```

This will lead us into a new session. To temporarily leave this session, use:

```
tmux detach
```

List all existing session:

```
tmux ls

```

Go into a specific session:

```
tmux attach -t <session-name>
```

To kill a session, use:

```
tmux kill-session -t <session-name>
```

#### Conclusion

This is some basic operations in the linux server. Operations on Slurm will later be added (Or presented in another note).



