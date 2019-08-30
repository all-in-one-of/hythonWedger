

![alt text](https://github.com/tricecold/hythonWedger/blob/master/wedger2.jpg)


# hythonWedger
Houdini Wedger 2.0
Author :   Timucin OZGER
Date   :   23.09.2018


This little code wedges a houdini file using multiprocessing.pool . Works especially best with single threaded tasks running in parralel.

I also added functionality to make flipbooks and MP4 out of it.

Initial development stage is to have a strong hython base, then to make an HDA out of it.
Some tests showed that around additional %30 optimized gains were made if POP simulations were run in parralel. I beleive the results will scale much better with non-mnultithreading friendly tasks, such as Solid Solver or Bullet Solver.

This HDA creates a txt file to be run with the main file.

Under the HIP File Folder It creates 
```
HIPFILE
------geo
      ---WedgerSOPNAME
         -------------v_0 (version of the cache)
                      ---cmd (this is the command that main python file processes)
                      ---videos
                      ---wedge_n
                         --------- _drafts
```
             
USAGE
Load the HDA in your scene
Use it instead of a file Cache
Play around batch size and max tasks to optimize performance based on your needs.

![alt text](https://github.com/tricecold/hythonWedger/blob/master/ProgressReport.jpg)

TO DO
1) Add fail safes for memory usage , if possible fail pools that go over a limit of memory use and retry once more pools are complete.
2) Autosave a copy of hip file to run instead of master file
3) Create some benchmarks.
4) Create proper versioning tools that is linked to scene file or project





