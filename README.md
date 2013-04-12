condorPythonShell
============

A set of Python scripts that allows python jobs to be submitted to a condor cluster via the command line. The script writes a submit file for each job and then runs condor_submit. It is currently limited to systems with a shared filesystem.

I also include a set of python classes which act as a wrapper around the submit scripts allowing python jobs to be submitted from a shell (e.g. iPython) and the results returned to said shell. The classes also manage the Condor Process in the background, i.e. if the job is still in a queue and is deleted from Python then the job is removed from the queue. 

The classes include condorList, a list of condor processes and condorDict a dictionary of condor processes.


Usage:

import condorSubmit as cs

result=cs.cmap(func1,argIter)

result[0]

If the job has finished it will display the result. If it has not finished then it will raise an 'UnfinishedCondorJob' exception.


I am currently cleaning up the code and will submit the version in a week or so.
