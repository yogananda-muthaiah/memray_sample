# Memray Python Memory Profiler 

Instructions :

https://github.com/bloomberg/memray

```
python3 -m pip install memray
```

Step 1 : Install Python & Pip3 in Business Application Studio ( Ignore if its already installed)

Step 2 : Sample python is my git
https://github.com/yogananda-muthaiah/memray_sample.git

Step 3 : Test it once in your local SAP Business Application Studio

```
python3 app.py
```

Step 4 : run the memray which will throw a bin file in your folder

```
python3 -m memray run app.py


Writing profile results into memray-app.py.1580.bin
emray WARNING: Correcting symbol for malloc from 0x4215f0 to 0x7f98465713e0
Memray WARNING: Correcting symbol for free from 0x421a50 to 0x7f9846571a30
Memray WARNING: Correcting symbol for aligned_alloc from 0x7f984600b480 to 0x7f98465720f0
[########################################]
[memray] Successfully generated profile results.

You can now generate reports from the stored allocation records.
Some example commands to generate reports:

/usr/bin/python3 -m memray flamegraph memray-app.py.1580.bin
```

Step 5 : run the flamegraph using memray with downloaded bin file
```
python3 -m memray flamegraph memray-app.py.1580.bin

Wrote memray-flamegraph-app.py.1580.html
```
Step 6 : If you need live memory profile – run the below command
```
python3 -m memray run --live app.py
```
