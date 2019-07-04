# 

A thread has a beginning, an execution sequence, and a conclusion. It has an instruction pointer that keeps track of where within its context it is currently running.

To spawn another thread, you need to call following method available in thread module −
thread.start_new_thread ( function, args[, kwargs] )
This method call enables a fast and efficient way to create new threads in both Linux and Windows.
The method call returns immediately and the child thread starts and calls function with the passed list of args. When function returns, the thread terminates.
Here, args is a tuple of arguments; use an empty tuple to call function without passing any arguments. kwargs is an optional dictionary of keyword arguments.

The newer threading module included with Python 2.4 provides much more powerful, high-level support for threads than the thread module discussed in the previous section.
The threading module exposes all the methods of the thread module and provides some additional methods −
threading.activeCount() − Returns the number of thread objects that are active.
threading.currentThread() − Returns the number of thread objects in the caller's thread control.
threading.enumerate() − Returns a list of all thread objects that are currently active.
In addition to the methods, the threading module has the Thread class that implements threading. The methods provided by the Thread class are as follows −
run() − The run() method is the entry point for a thread.
start() − The start() method starts a thread by calling the run method.
join([time]) − The join() waits for threads to terminate.
isAlive() − The isAlive() method checks whether a thread is still executing.
getName() − The getName() method returns the name of a thread.
setName() − The setName() method sets the name of a thread.
Creating Thread Using Threading Module
To implement a new thread using the threading module, you have to do the following −
Define a new subclass of the Thread class.
Override the __init__(self [,args]) method to add additional arguments.
Then, override the run(self [,args]) method to implement what the thread should do when started.
Once you have created the new Thread subclass, you can create an instance of it and then start a new thread by invoking the start(), which in turn calls run() method.
