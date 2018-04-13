## Multiple Choice and Short Answer Questions

1. List all of the main states a process may be in at any point in time on a
   standard Unix system. Briefly explain what each of these states mean.

    Created- When the process is first created, waiting to be ready as approved by the scheduler.

    Ready- Process loaded into main memory system and awaiting CPU execution; waiting in the run        queue.

    Running- When it is first in the queue and executed.

    Blocked- Running but cannot continue until an external event occurs allowing it to continue.

    Terminated- Either killed or completed execution, waiting to be exited in the process table.

2. What is a Zombie Process? How does it get created? How does it get destroyed?

    A zombie process is a terminated process that is still in the process table, waiting for another process to read its exit status and be removed from the table. It gets created between the points in time of a process finishing and waiting for its exit status to be executed, and it is usually destroyed by the parent process that reads its exit status and reaps it from the process table.

3. Describe the job of the Scheduler in the OS in general.

    The scheduler decides which order to run processes for the CPU, managing the ready and run queues. It also pushes new processes into memory to be ready for execution.

4. Describe the benefits of the MLFQ over a plain Round-Robin scheduler.

    MLFQ allows for priority scheduling, and adjusting priority during its execution, whereas Round-Robin treats all processes the same and executes one-by-one in whatever order they are input. MLFQ is much more efficient in this regard, new processes have top priority, then are adjusted depending if they finish their quantum or not. Because of the prioritization system it allows for preemptive sorting of shorter processes to finish quickly and reduce CPU burden.