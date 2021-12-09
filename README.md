# OS-Practicals

Q.1
Round Robin is a cyclic CPU scheduling system that assigns each task a defined time slot. It's straightforward, quick to set up, and doesn't cause CPU exhaustion because each process gets an equal amount of CPU time. As a core, this is one of the most often used scheduling techniques. It is active because processes are only given CPU for a certain amount of time. The drawback is that context switching takes more time.

Create an array rem_bt[] to keep track of remaining burst time of processes. 
This array is initially a copy of bt[] (burst times array)
Create another array wt[] to store waiting times of processes. Initialize this array as 0.
Initialize time : t = 0
Keep traversing the all processes while all processes are not done. Do following for i'th process if it is not done yet.
a- If rem_bt[i] > quantum
       (i)  t = t + quantum
       (ii) rem_bt[i] -= quantum;
c- Else // Last cycle for this process
       (i)  t = t + rem_bt[i];
       (ii) wt[i] = t - bt[i]
       (ii) rem_bt[i] = 0;
      
Q.2.
fork()->
It accepts no input and returns an integer value. The values returned by fork() are listed below. 
Negative Value: The procedure of creating a child was unsuccessful. 
Zero: Return to the newly created child process
Positive: Return to parent or caller value. The value is the newly created child process's process ID.
