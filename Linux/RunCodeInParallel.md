In linux, to run python scripts in parallel, use:
```
python scriptA.py & python scriptB.py & python scriptC.py
```
To run code in back stage, use:
```
nohup /bin/sh Code.sh &
```
Which will return a code representing the process number

To check output log nohup.out, use:
```
tail -fn 50 nohup.out
```
