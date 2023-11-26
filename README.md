# Interview-Questions

## Node JS Interview Questions

1.  What is npm?

**Answer:**

npm stands for Node Package Manager. npm provides following two main functionalities:

Online repositories for node.js packages/modules which are searchable on search.nodejs.org
Command line utility to install packages, do version management and dependency management of Node.js packages.

#

2. What is Node.js?

**Answer:**

Node.js is a web application framework built on Google Chrome's JavaScript Engine (V8 Engine).

Node.js comes with runtime environment on which a Javascript based script can be interpreted and executed (It is analogus to JVM to JAVA byte code). This runtime allows to execute a JavaScript code on any machine outside a browser. Because of this runtime of Node.js, JavaScript is now can be executed on server as well.

Node.js = Runtime Environment + JavaScript Library

#

3. What is an error-first callback?

**Answer:**

Error-first callbacks are used to pass errors and data. The first argument is always an error object that the programmer has to check if something went wrong. Additional arguments are used to pass data.

        fs.readFile(filePath, function(err, data) {
            if (err) {
                //handle the error
            }
            // use the data object
        });

#

4. What is Callback Hell?

**Answer:**

The asynchronous function requires callbacks as a return parameter. When multiple asynchronous functions are chained together then callback hell situation comes up.

#

5. What is control flow function?

**Answer:**

It is a generic piece of code which runs in between several asynchronous function calls is known as control flow function.

#

6. What are Event Listeners?

**Answer:**

Event Listeners are similar to call back functions but are associated with some event. For example when a server listens to http request on a given port a event will be generated and to specify http server has received and will invoke corresponding event listener. Basically, Event listener's are also call backs for a corresponding event.

Node.js has built in event's and built in event listeners. Node.js also provides functionality to create Custom events and Custom Event listeners.

#

7. If Node.js is single threaded then how it handles concurrency?

**Answer:**

Node provides a single thread to programmers so that code can be written easily and without bottleneck. Node internally uses multiple POSIX threads for various I/O operations such as File, DNS, Network calls etc.

When Node gets I/O request it creates or uses a thread to perform that I/O operation and once the operation is done, it pushes the result to the event queue. On each such event, event loop runs and checks the queue and if the execution stack of Node is empty then it adds the queue result to execution stack.

This is how Node manages concurrency.

#

8. Could we run an external process with Node.js?

**Answer:**

Yes. Child process module enables us to access operating system functionaries or other apps. Scalability is baked into Node and child processes are the key factors to scale our application. You can use child process to run system commands, read large files without blocking event loop, decompose the application into various “nodes” (That’s why it’s called Node).

Child process module has following three major ways to create child processes –

* spawn - child_process.spawn launches a new process with a given command.
* exec - child_process.exec method runs a command in a shell/console and buffers the output.
* fork - The child_process.fork method is a special case of the spawn() to create child processes.

#

