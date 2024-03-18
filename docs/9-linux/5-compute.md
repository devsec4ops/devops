# Compute

## **What** is a Linux Process?

A process is basically a running program on your computer. When you open an app or run a command, Linux starts a new process for it. Each process has a unique number called a Process ID (PID).

### **Types** of Processes

-   Foreground processes: When you run a command or program, and it takes control of your terminal until it's done, it's running in the foreground. You have to wait for it to finish to do something else.
-   Background processes: These are the opposite. You can start a process and keep using your terminal without waiting for it to finish. You add `&` at the end of a command to do this. For example:
-   
    `sleep 30 &`

### **Viewing and Managing Processes**

-   `ps`: Shows you what processes are running. `ps aux` is a common way to see all running processes with details.
-   `top`: Gives you a live look at running processes and how much computer resources they're using.
-   `kill`: Lets you stop a process. If a process won't stop normally, you can force it to stop with `kill -9 PID`, replacing `PID` with the process's unique number.

##  **What** is a Job?

A job is like a task you've told your Linux shell (like Bash) to do. You can have many jobs running at the same time.

### **Job Control Commands**

-   `bg`: Moves a paused job to the background so it keeps running. For example, if you've stopped a job, you can continue it in the background with `bg %1`, where `1` is the job number.
-   `fg`: Brings a background job to the foreground. If you used `bg` to send a job to the background, use `fg %1` to bring it back.
-   `jobs`: Lists all your current jobs with their numbers and states, like running or stopped.


## **Real-life Uses and Commands**

-   Checking what's running: Use `ps aux` to see all active processes. It's helpful if your computer is slow, and you want to find out what's using all the resources.
-   Stopping a frozen program: If a program isn't responding, find its PID with `ps aux | grep program_name`, then stop it with `kill PID`.
-   Running tasks in the background: Start a long-running command like a file backup in the background with `command &` so you can keep using your terminal.
-   Bringing a background task to the foreground: If you started a task like editing a document in the background but now want to interact with it, use `fg %job_number` to bring it back.

##**Interview question** 

1.  Can a zombie process consume CPU resources?
    - No, a zombie process cannot consume CPU resources. It's a process that has completed execution but still remains in the process table waiting for its parent to retrieve its exit status.
2.  Is it possible to kill a zombie process using the `kill` command?
    - No, you cannot kill a zombie process using the `kill` command because the process has already finished execution. The proper way to remove a zombie process from the process table is for its parent process to read its exit status, or by terminating the parent process, after which the init process will adopt and clean it up.
3.  Can you run a command in the background without using the `&` at the end of the command? How?
    - Yes, you can use the `nohup` command or `disown` shell builtin with a running process. `nohup` allows a command to continue running in the background even after you log out. With `disown`, you can remove a job from the shell's job table, making it immune to hangups even without `&`.
4.  How can you list only the child processes of a specific process?
    - A common misconception is that commands like `ps` directly support filtering by parent process ID (PPID). While `ps` does show PPID, to list only the child processes of a specific process, you might use a combination of `ps` and `grep` or the `pstree -p [parent_pid]` command, where `[parent_pid]` is the PID of the parent process, to get a tree representation.
5.  If `kill -9` cannot kill a process, what could be the reason?
    - If `kill -9` (which sends the SIGKILL signal) does not terminate a process, it is likely because the process is in an uninterruptible sleep state (D state), usually waiting on I/O. Processes in this state cannot be killed until they resume, as the kernel is handling the process directly.
6.  What happens if you execute the command `:(){ :|:& };:` in a Linux shell?
    - This command is a fork bomb. It defines a function named `:` that, when called, starts two instances of itself in the background, each of which does the same. It rapidly exhausts the system's process limit, potentially leading to a system crash. **It's a dangerous command and should not be executed**.
7.  Can you have more than one PID 1 process in a system?
    - Under normal circumstances, there is only one PID 1 process, which is the init process (like systemd or SysVinit) responsible for bootstrapping the user space and managing system processes. However, in namespaces (particularly with containers like Docker), each namespace can have its own PID 1, isolated from the host system.
8.  Is it possible for a child process to continue running after its parent process has been terminated?
    - Yes, when a parent process is terminated, its child processes are not automatically killed. Instead, they are re-parented to the init process (or another appropriate process), which then becomes responsible for them.