All Question of Tarteeb course.
# 1. What is .NET?
.NET is platform created by Microsoft. It provides comprehensive framework and runtime environment for building, deploying and running varios types of applications ranging from desktop and web app to mobile app and cloud services. .NET components: CLR,  Base Class Library. 
# 2. What is CLR? How CLR works?
CLR is the heart of the .NEt platform and provides memory management, garbage collection, exception handling and type safety, type system, Security, assembly loading and thread synchronization are available to any and all programming languages.
CLR contains Just In Time, Garbage Collector.

3. What does compiler do?
You use the co-responding compiler to check the syntax and analyses the source code. Regardless of which compiler you use, the result is a managed module.

4. What is Managed Code?
A managed module is a standard 32-bit Windows portable executable (PE 32) file or a standard 64-bit Windows portable executable (PE 32+) file that required the CLR to execute. In C# a managed module refers to a unit of compiled  code that confirm to the Common Language Infrastructure(CLI). Managed module are typically produced by compiling source code written in language such as C#, F#, etc.

5. What does Managed Code contain?
The Managed Module contains 4 things.  1) PE 32 / PE 32+:  32 or 64-bit, GUI, CUI, or dll.
2)CLR header: Location / Size, Flag, Other Metadata.
3)Metadata: Types & Members, Referenced Types.
4)IL.

What is Metadata?
Every managed module contains metadata tables. There are two main types of tables. 1)types & Members, Referenced Types. Unlike type Libraries  and IDL metadata is always associated with the file that contain the IL code. In fact, the metadata is always embedded in the same EXE/DLL as the code, making it impossible to separate the two. The metadata and the IL code it describes are never out of sync with one another.

6. What is IL?
IL is a platform, independent, high-level assembly language that can be executed by the Common
IL is stack-based, which means that all of its instructions push operands onto an execution stack and
pop results off the stack. Because IL offers no instructions to manipulate registers, it is easy for people
to create new languages and compilers that produce code targeting the CLR. IL instructions are also typeless. 
IL code is not directly executable by the computers hardware. Instead it's an intermediate representation that can be executed by the CLR. 

7. What is Assembly Language?
The CLR doesn’t actually work with modules, it works with assemblies. An assembly is an abstract
concept that can be difficult to grasp initially. First, an assembly is a logical grouping of one or more
modules or resource files. Second, an assembly is the smallest unit of reuse, security, and versioning.
Depending on the choices you make with your compilers or tools, you can produce a single-file or a
multi file assembly. In the CLR world, an assembly is what we would call a component.some managed modules
and resource (or data) files are being processed by a tool. This tool produces a single PE32(+) file that
represents the logical grouping of files. What happens is that this PE32(+) file contains a block of data called the manifest. The manifest is simply another set of metadata tables. These tables describe the
files that make up the assembly, the publicly exported types implemented by the files in the assembly,
and the resource or data files that are associated with the assembly.
An assembly’s modules also include information about referenced assemblies (including their
version numbers). This information makes an assembly self-describing. In other words, the CLR can
determine the assembly’s immediate dependencies in order for code in the assembly to execute.

Siz qanday assembly tuzgan paytiz bu assembly ishlayotgan boshqa assembly larni referencini o'zida ma'lumotini saqlaydi ya'ni qanaqa boshqa assemblylarga bog'liq ekanligi haqida ma'lumotni saqlaydi Ya'ni o'zini o'zi qayerda nimaga bog'liq bo'lganini tushuntira olishini ya'ni describe qila oladigan eng kichkina bo'lim

9. What is assembly?
As a step up from machine code, assembly uses abbreviations called mnemonics that represent the actual machine instructions. These mnemonics are easier for programmers to understand and work with. For example, instead of a long string of binary digits for "add," assembly might use the mnemonic "ADD."

10. What is a component in CLR world?
	It is intermediate Language because IL called component in the CLR world.

12. What is JIT Compilation?
Just In Time Compilation : When you run your C# program, the CLR loads the assembly containing the IL code
- [ ] The CLR's JIT compiler translates the IL the code into native machine code that is specific to the computer's hardware architecture(This dynamic translation ensures optimal performance by adapting the code to the execution environment. 
13. What is Stack vs Queue?
stack is a linear data structure where elements are inserted and removed from one end only, known as the top. It follows the LIFO (Last In First Out) principle, meaning that the last element added is the first one to be removed. 
* A queue is another linear data structure.
* Elements are inserted at one end (called the rear) and removed from the other end (called the front).
* It follows the FIFO (First In First Out) principle, where the first element added is the first one to be removed.

14. What is Base Class Library (BCL)?
* The BCL is the foundational part of the .NET Framework. It contains essential, fundamental types and functionality that are available to all .NET applications.
* Some key points about the BCL:
    * It includes basic data types (e.g., System.String, System.DateTime), file access, collections, custom attributes, formatting, security attributes, I/O streams, and string manipulation.
    * These core types are closely integrated with the Common Language Runtime (CLR), which manages memory, execution, and other runtime services for .NET applications.
    * BCL is a comprehensive collection of reusable classes, interfaces and value types that provide fundamental building blocks for .NET applications.

15. What is Framework Class Library (FCL)?
* The FCL is a broader library that encompasses the entire .NET Framework. It extends beyond the BCL and provides additional functionality for specific application domains.
* Key points about the FCL:
    * It includes libraries for various purposes, such as:
        * ASP.NET: For building web applications.
        * WinForms: For creating Windows desktop applications.
        * ADO.NET: For database access.
        * XML stack: For working with XML data.
        * And more…
    * Developers can use FCL classes to make their lives easier when building different types of applications.

18. What is IL Verification? 
The biggest benefit IL provides is application robustness and security. While compiling IL into native CPU instructions, the CLR performs a process called verification. Verification examines the high-level IL code and ensures that everything the code does is safe. For example, verification checks that every method is
called with the correct number of parameters, that each parameter passed to every method is of the
correct type, that every method’s return value is used properly, that every method has a return statement, and so on. The managed module’s metadata includes all of the method and type information
used by the verification process.

19. What is safe vs unsafe code?
By default, Microsoft’s C# compiler produces safe code. Safe code is code that is verifiably safe. However, Microsoft’s C# compiler allows developers to write unsafe code. Unsafe code is allowed to work directly with memory addresses and can manipulate bytes at these addresses. This is a very powerful feature and is typically useful when interoperating with unmanaged code or when you want to improve the performance of a time-critical algorithm. However, using unsafe code introduces a significant risk: unsafe code can corrupt data structuresand exploit or even open up security vulnerabilities. For this reason, the C# compiler requires that all methods that contain unsafe code be marked with the unsafe keyword. In addition, the C# compiler requires you to compile the source code by using the /unsafe compiler switch.

1. What is System.Object? 
System.Object is the ultimate base class for all types. All types are derived from System.Object. This means that the following two type definitions are identical.
1. //Implicitly derived from object: class Employee{}
2. //Explicitly derived from Object: class Employee : System.Object{} 
2. What methods does it have? Explain? 
The System.Object class offers the public instance methods. In addition, types that derive from System.Object have access to the protected methods.
1. Public: Equals, GetHashCode, ToString, GetType;
2. Protected: MemberwiseClone, Finalize 
3. What is new operator? How does it work? done
The CLR requires all objects to be created using the new operator. The following line shows how to
create an Employee object.
Employee e = new Employee("ConstructorParam1");
Here’s what the new operator does:
1. It calculates the number of bytes required by all instance fields defined in the type and all of
its base types up to and including System.Object (which defines no instance fields of its
own). Every object on the heap requires some additional members—called the type object
pointer and the sync block index—used by the CLR to manage the object. The bytes for these
additional members are added to the size of the object.
2. It allocates memory for the object by allocating the number of bytes required for the specified
type from the managed heap; all of these bytes are then set to zero (0).
3. It initializes the object’s type object pointer and sync block index members.
4. The type’s instance constructor is called, passing it any arguments (the string "ConstructorParam1"
in the preceding example) specified in the call to new. Most compilers automatically
emit code in a constructor to call a base class’s constructor. Each constructor is responsible for
initializing the instance fields defined by the type whose constructor is being called. Eventually, System.Object’s constructor is called, and this constructor method does nothing but return.
After new has performed all of these operations, it returns a reference (or pointer) to the newly
created object. In the preceding code example, this reference is saved in the variable e, which is of
type Employee.
By the way, the new operator has no complementary delete operator; that is, there is no way to
explicitly free the memory allocated for an object. The CLR uses a garbage-collected environment
(described in Chapter 21) that automatically detects when objects are no longer being used or accessed and frees the object’s memory automatically. the C# new operator returns the memory address of the object—the memory address refers to the object’s bits. 
Me: 
1."New" operator qancha bayt joy olishini hisoblaydi ya'ni type qancha joy oladigan bo'lsa shunga qarab.
2. Va u xotiralarni ajratadi object uchun, nimaga qarab ajartadi deganda byte-ga qarab misil uchun 1 byte ga 8 ta sell(xotira katakchasi) ajratadi va bu xodisa heap xotirada bo'ladi va bu hamma bytelar  0 yoki null bilan to'ldiriladi. Xuddi array ga o'xshab.
3. Va objectni type va indexini  initialize qiladi.
4. Va usha instance constructor chaqiriladi(like Employee()) va bironta argument qabul qiladi, Har bir constructor field ni intialize qilishga ma'sul dir va shu ketma ketlikda System.Object ning ham constructori chaqiriladi bu constructor method hechnima qilmaydi shunchaki return qiladi. Va "new" keywordi hamma shu ishlarni qilgandan keyin bu reference qaytaradi yangi yaratilgan objectni va bu reference variable ga saqlanadi qaysiki type Employee employee; ga  Aytgancha "new" operatorida delete operatori yo'q, ya'ni create qilgandan keyin xotiradan delete qila olmaydi .Buning uchun CLR garbage-collectorni ishlatadi.

4. What does sealed keyword mean? 
When you declare a class as sealed, it means that no other class can inherit from it. When a method is sealed, it cannot be overridden by any derived class.

5. Tell me about GetType() method? Can I override it? 
One of the most important features of the CLR is type safety. At run time, the CLR always knows what type an object is. You can always discover an object’s exact type by calling the GetType method. Because this method is non-virtual, it is impossible for a type to change another type. For example, the Employee type can’t override the GetType method and have it return a type of SuperHero.

6. Tell me about "is" keyword?  
The "is" operator checks whether an object is compatible with a given type, and the result of the evaluation is a Boolean: true or false.The is operator will never throw an exception.
The "is" operator is used to check the type of an object.

7. Tell me about "as" keyword? done
"as" operator is used to Perform conversion between compatible reference type.
"as" operatorini biz ikki compatible reference type-larni cast qilish uchun foydalanamiz. Misol uchun object va string, lekin int va string bo'lsa bolmaydi.

8. What to do if two types from different namespaces have same name? 
Problem: Two companies might both offer a type called Widget - Microsoft's Widget does one thing and Wintellect's Widget does something entirely different.  Solution: //Define WintellectWidget symbol as an alias to Wintellect.Widget using WintellectWidget = Wintellect.Widget; using MicrosoftWidget = Microsoft.Widget; :)

9. What is process? 
A windows process refers to a running instance of a program on the windows operating system. Each process has  own memory space, system resources, and execution environment. Here are some keys points about windows process. A Windows process refers to a running instance of a program on the Windows operating system. Each process has its own memory space, system resources, and execution environment. Here are some key points about Windows processes:
1. Execution Environment: A process provides an execution environment for a program. It includes resources such as memory, CPU time, files, and input/output devices.
2. Isolation: Processes are isolated from each other, meaning that the memory space of one process is separate from that of another. This isolation helps prevent one process from accessing or modifying the memory of another process without proper authorization.
3. Process Lifecycle: Processes go through different states during their lifecycle, including creation, execution, suspension, and termination. The Windows operating system manages the lifecycle of processes, allocating resources as needed and reclaiming them when the process terminates.
4. Identification: Each process is identified by a unique process identifier (PID), which is a numerical value assigned by the operating system. PIDs are used to manage and track processes, allowing the operating system to perform operations such as process creation, termination, and resource allocation. 
10. What is thread? done 
Thread bu processni ichida yaratiladigan eng kichik qism bo'lib, 1mb stack xotiraga ega.

11. What is stack? done Certainly! Let’s dive into the concept of stack memory in C# in a way that’s easy to understand.
When we write code in C# (or any other programming language), our programs need to allocate memory to store variables, objects, and other data. This memory can be categorized into two main types: stack memory and heap memory. Let’s break down what each of these means:
    * Allocation Purpose: Stack memory is primarily used for static memory allocation and local variables.
    * Managed by CPU: The stack memory is managed directly by the CPU, which makes it faster and more efficient.
    * How It Works:
        * When a method is called, a stack frame (a block of memory) is allocated on the stack.
        * This stack frame contains space for local variables and method parameters.
        * As the method executes, it uses this allocated memory for its operations.
        * When the method call returns, the stack frame is automatically deallocated.
    * Analogy: Imagine a stack of plates or dishes placed on top of each other. Each plate represents a method call, and the stack grows and shrinks as methods are called and return.
    * LIFO Principle: Stack memory follows the Last In, First Out (LIFO) principle. This means that memory allocation and deallocation happen only at one end of the stack (the top).
    * 
12. What is heap? done
	Heap memory is used for dynamic memory allocation, especially for objects with varying lifetimes. Unlike stack memory, heap memory is not managed by the CPU directly.
    * How It Works:
        * When you create an object (e.g., an instance of a class), the object itself is stored in a different memory location called the heap.
        * The stack memory contains a pointer to this object in the heap.
        * The heap doesn’t track running memory; it’s used for more complex and long-lived data structures.
    * Usage Example: When you create an instance of a class (like SomeClass in your code), the object’s data resides in the heap, while the stack holds a reference to it.
In summary, stack memory is like a quick-access scratchpad for method calls and local variables, while heap memory is a larger storage area for more complex data structures. Understanding these memory types helps us write efficient and reliable C# code.

13. What is garbage-collection? done
Garbage collection is a crucial memory management technique used in the .NET Framework (which includes C#) and many other programming languages. Its primary purpose is to automatically manage memory by freeing up memory that is no longer needed by the application. Here are the key points about garbage collection in C#.

1. Checked/Unchecked operator & statement done 
Byte b = 200;  b = (Byte) (b + 100);  // b now contains 44(or 2C in Hex)
In this example b and 200 are first converted to 32-bit values and are then added together; the result is 300  then 300 is converted to byte due to the explicit cast this generated the overflow Exception if the Byte were cast outside the checked operator, the exception would not occur.
=> checked keyword helps to check if the destination data type is overflow in arithmetic calculation.
=> unchecked keyword behaves almost the same way as default but is useful to by pass the constant data type checks
Checked / unchecked statement: this statements cause all expressions within a block to be checked or unchecked.
checked
{ //start of checked block  Byte b = 100;
b += 200; // This expression is checked for overflow 
}  // End of checked block.

2. What are primitive types?
Primitive types deganda bizaga FCL tomonidan oldin yozilgan type nazarda to'tiladi bunga System.Int32, System.Single, System.Float va hokazolar kiradi. va bular uchun C# tili tomonidan kalit so'zlar hozirlab qo'ygan va shuning uchun biz FCL da yozilgan shakldagi typlarni emas uni o'rniga C# oddiy kalit so'zlarini ishlatib foydalanishimiz mumkin.

3. What is Reference type? 
The CLR supports two kinds of types: reference types and value types. Reference types are always allocated from the managed heap, and the C# new operator returns the memory address of
the object—the memory address refers to the object’s bits. 
■ The memory must be allocated from the managed heap.
■ Each object allocated on the heap has some additional overhead members associated with it
that must be initialized.
■ The other bytes in the object (for the fields) are always set to zero.
■ Allocating an object from the managed heap could force a garbage collection to occur.

4. What is Value type? 
Value types are lighter then reference types because they are no allocated as objects in the managed heap, not garbage collected, and not referenced to by pointers, However, in many cases, you must get reference to an instance of a value type. For example, let's say that you wanted to create an ArrayList object.

5. What does copy-by-value vs copy-by-reference means in those contexts? done
In reference type when we copy types value it reference to memory address not create another memory clot
In value type when we copy types value it copy and create new slot  from memory, second type will be independent.

1. What does partial keyword mean? done
The partial keyword tells the C# compiler that the source code for a single class, structure, or interface definition may span one or more source code files. Each file contains a portion of the class definition and when the program is compiled, the compiler combines all the partial class definition into a single class definition.

2. What does static keyword mean? done
A static keyword in C# is a special type of a class taht cannot be instantiated and can only contain static members, such as static fields, static methods, static properties and static events. 1.Cannot be instantiated: Since static classes can only contain static members, are cannot have instance members they cannot be instantiated using the "new" keyword like regular classes. 2. Static members only: All members of a static class must be declared as static.

1. What is Task?
In C#, a Task is a higher-level abstraction for running code asynchronously. A Task denotes a unit of work that needs to be executed asynchronously, and it may or may not return a value. A Task is usually created with the help of the Task Factory class, which provides several methods for creating and executing Tasks.
Tasks use a Thread pool to execute their work, which means that the Tasks are executed on one of the Threads in the Thread pool. When a Task is created, it is added to the Thread pool's queue, and one of the Threads in the pool is used to execute the Task. Once the Task is completed, the Thread returns to the pool, ready to be used for another Task.
* Tasks are more lightweight than Threads. Tasks use fewer system resources, such as memory and CPU time, compared to Threads.
* Tasks are easier to manage than Threads. Tasks provide a higher-level abstraction for asynchronous programming, which makes it easier to write and maintain code.
* Tasks can also provide better performance than Threads in certain situations. This is because Tasks use a Thread pool, which can manage Threads more efficiently than creating and destroying Threads for each unit of work.
Tasks are recommended when you want to perform a unit of work asynchronously, and you don't need fine-grained control over the execution. Tasks are perfect for executing small and short-lived units of work, such as I/O operations or simple computations.
Tasks are also recommended when you want to leverage the benefits of a Thread pool. A Thread pool can manage Threads more efficiently than creating and destroying Threads for each unit of work. This can result in better performance, especially when there are many units of work to execute.
Tasks are also useful when you want to chain asynchronous operations. Tasks can be combined using the await operator to create a chain of asynchronous operations that execute one after the other. This can be important when you want to perform a series of dependent asynchronous operations.
When to Use Threads:
Threads in C# should be used when you need fine-grained control over the execution and when you have specific requirements that cannot be met with the higher-level abstractions provided by Tasks. Here are some situations where Threads may be the better choice:
Long-lived Units of Work:
Threads are better suited for long-lived units of work, such as background services or complex computations that require more control over the execution. In such cases, it is often necessary to control the execution of the code in a more fine-grained manner than what Tasks provide.
Fine-grained Control Over Thread Execution:
Threads allow you to set Thread priorities, Thread synchronization, and Thread aborts. If you need to customize how your code is executed, Threads provide a low-level interface that allows you to do so.
Low-level Programming:
Threads require more low-level programming and synchronization, which can be useful if you have specialized requirements that cannot be met with the higher-level abstractions provided by Tasks.

2. What is Threadpool?
In C#, a ThreadPool is a managed thread pool provided by the .NET Framework to efficiently manage and reuse threads. It allows you to perform asynchronous and parallel operations without explicitly creating and managing threads on your own. ThreadPool is commonly used for executing short-lived tasks or actions in a multithreaded environment to improve performance and resource utilization.
The ThreadPool class is available in the System.Threading namespace and provides a static API for interacting with the thread pool. 
It’s important to note that the ThreadPool is designed for short-lived tasks and not suitable for long-running operations. If you have long-running tasks, consider using dedicated threads (e.g., via Task with TaskCreationOptions.LongRunning or explicit thread creation) to avoid blocking ThreadPool threads that could be used for other short tasks.
Keep in mind that starting from .NET Core 3.0, the default thread pool implementation changed to “CompletionPortThreadPool” from “DefaultThreadPool.” This change enhances the performance and scalability of the ThreadPool in modern applications.


3. What is task.Start() and task.Wait()? What is the alternative to it?
1. Task.Start() and Task.Wait():
    * Task.Start(): This method is used to explicitly start a new task. It creates and schedules a new task for execution. However, it doesn’t make the calling method asynchronous by itself.
    * Task.Wait(): This method blocks the current thread until the specified task completes. It’s a synchronous operation, meaning it waits for the task to finish before proceeding further.
2. async/await:
    * The async and await keywords provide an alternative approach to handling asynchronous operations in C#.
    * When you mark a method as async, it allows you to use the await keyword within that method.
    * Here’s how it works:  
4. What is async/await?
1. Concurrency vs. Parallelism:
    * Concurrency is the ability of an application to be composed of multiple asynchronous processes that may execute independently but may not necessarily run at the same time. async/await facilitates concurrency by allowing the program to continue executing other tasks while waiting for asynchronous operations to complete.
    * Parallelism, on the other hand, involves executing multiple tasks simultaneously, usually on multiple threads or processors. While async/await can lead to parallelism in certain scenarios (like in ASP.NET Core applications), it primarily focuses on simplifying concurrency rather than enabling parallelism directly.
2. Asynchronous Programming Model (APM):
    * Before async/await, asynchronous programming in .NET was typically done using the Asynchronous Programming Model (APM), which involved methods with names ending in Begin and End, such as BeginRead and EndRead. APM was powerful but often complex and error-prone.
    * async/await simplifies asynchronous programming by providing a more intuitive and readable syntax compared to APM. It abstracts away much of the complexity involved in managing asynchronous operations, making code easier to write and understand.
3. Continuation Passing Style (CPS):
    * async/await can be understood in terms of Continuation Passing Style (CPS), which is a programming style used in functional programming and asynchronous programming.
    * In CPS, instead of waiting for the result of an asynchronous operation directly, the program specifies what should happen next after the operation completes. This is akin to providing a continuation or a callback.
    * With async/await, the await keyword effectively captures the continuation of an asynchronous operation. When the awaited operation completes, the rest of the method after the await is scheduled to run as a continuation. This allows for more sequential and intuitive code flow.
4. Compiler Transformations:
    * Under the hood, the C# compiler transforms async methods into state machines. It breaks the method into multiple parts and creates a state machine to track the progress of the asynchronous operation.
    * When encountering an await keyword, the compiler splits the method into two parts: the part before the await, which runs synchronously, and the part after the await, which becomes the continuation to be executed asynchronously when the awaited operation completes.
5. Error Handling:
    * Error handling with async/await is simpler compared to APM. Exceptions thrown within an async method are propagated back to the caller's context as if it were a synchronous method. You can use try/catch blocks around await expressions to handle exceptions.
    * Additionally, you can use the Task object returned by an asynchronous method to handle errors, check for completion status, or cancel the operation if needed.
Understanding these theoretical aspects helps in grasping the underlying principles of async/await and enables you to write more effective and efficient asynchronous code.

5. What is ContinueWith()?
ContinueWith() is a method in the .NET framework used to chain asynchronous operations together. It allows you to specify a continuation, which is an action to be performed after the asynchronous operation completes. This method is commonly used in scenarios where you want to execute additional logic once an asynchronous operation finishes, such as error handling, logging, or triggering another asynchronous operation.
* We start an asynchronous operation using Task.Run() to simulate an asynchronous task (SomeAsyncMethod()).
* We then use ContinueWith() to specify what should happen after the asynchronous operation completes. In this case, we print the result of the asynchronous operation.
* Finally, we await the continuation task to ensure that the program doesn't exit before the continuation finishes.
It's important to note that while ContinueWith() provides a way to chain asynchronous operations, it's often recommended to use async/await syntax instead, as it provides clearer and more concise code for handling asynchronous operations. However, ContinueWith() can still be useful in certain advanced scenarios where you need fine-grained control over task continuation.
The ContinueWith function is a method available on the task that allows executing code after the task has finished execution. In simple words it allows continuation.

6. When I can't use 'await'? ref, out, catch, finally, unsafe? 	1	Ref Parameters (ref): When you use ref to pass a variable to a method, you're essentially saying, "Hey, this method can directly change the original variable I'm passing." This is useful in situations where you want a method to modify the original variable rather than just working with a copy of it. However, await is specifically designed for asynchronous operations, like waiting for a file to download or waiting for a database query to finish. It's not meant for directly modifying variables, so you can't use await with ref.
1. Out Parameters (out): Similar to ref, out is used for passing variables to methods, but with out, the method is required to assign a value to the variable before it returns. This is often used when you want a method to output multiple values. Again, await is for waiting on asynchronous tasks to finish, not for directly modifying variables, so it doesn't work with out parameters.
2. Catch Blocks (catch): In C#, catch blocks are used for handling exceptions that occur during the execution of your code. When something unexpected goes wrong, like trying to divide by zero or accessing a file that doesn't exist, you use a catch block to deal with that error gracefully. await, on the other hand, is for waiting on asynchronous tasks to complete. It doesn't have anything to do with handling errors, so you can't use await inside a catch block.
3. Finally Blocks (finally): finally blocks are used to ensure that certain code runs regardless of whether an exception was thrown or not. This is helpful for things like cleaning up resources or releasing locks. await is for asynchronous programming and has nothing to do with ensuring certain code always runs, so it's not allowed inside finally blocks.
4. Unsafe Code (unsafe): In C#, most code runs in a safe, managed environment, meaning the language and runtime take measures to prevent certain types of bugs and security vulnerabilities. However, there are times when you might need to do something that's not allowed in this safe environment, like directly manipulating memory addresses. That's where unsafe code comes in. However, await is all about safely managing asynchronous tasks, so it doesn't make sense to use it in unsafe code.
In essence, await is a tool specifically designed for asynchronous programming, and it doesn't play well with situations that involve directly modifying variables, handling errors, ensuring code always runs, or doing low-level memory operations.

7. Can I make my Main method async?
In C#, starting with version 7.1, you can make the Main method asynchronous by changing its signature to return a Task or Task<int> (if you want to return an exit code). Then you can mark it with the async keyword and await asynchronous operations inside it.
You can make your Main method async in C#. Let’s explore how and why you might want to do that.
1. What is an async Method?
    * An async method is a method that can asynchronously execute code without blocking the calling thread.
    * It’s commonly used for tasks that involve I/O operations (such as reading/writing files, making network requests, or querying databases) or other asynchronous operations.
    * The async keyword allows you to use the await keyword inside the method.
2. Making Main Method async:
    * By default, the Main method in a C# console application is synchronous (blocking).
	◦	However, you can make it async by adding the async modifier to the Main method signature.
1. What is thread?
In C#, a Thread is a lower-level abstraction for running code asynchronously. A Thread represents an operating system-level construct that is used to execute code asynchronously. A Thread may or may not return a value, and it is usually created with the help of the Thread class.
Threads use their own resources, such as memory and CPU time, and they are usually created and destroyed explicitly by the developer. When a Thread is created, it starts executing immediately, and it continues to execute until it is explicitly stopped or it completes its work.
Threads have several disadvantages compared to Tasks:
* Threads are heavier than Tasks. Threads use more system resources, such as memory and CPU time, compared to Tasks.
* Threads are harder to manage than Tasks. Threads require more low-level programming and synchronization, which makes it harder to write and maintain code.
* Threads can also provide worse performance than Tasks in certain situations. This is because creating and destroying Threads for each unit of work can be inefficient, especially when there are many units of work to execute.

2. What is foreground thread vs background
1. Foreground Threads:
    * Foreground threads are considered important threads by the runtime, and they keep the application alive as long as they are running.
    * If there are any foreground threads still running, the runtime won't shut down the application, even if all foreground threads are blocked (e.g., waiting for I/O operations to complete).
    * Foreground threads are typically used for executing critical tasks that must complete before the application can gracefully exit or for long-running tasks that are integral to the application's functionality.
    * By default, the main thread (the one that executes the Main method) is a foreground thread.
    * You can mark a thread as foreground explicitly by setting its IsBackground property to false, although it's not common to do so because foreground is the default behavior.
2. Background Threads:
    * Background threads, also known as daemon threads in other programming languages, are considered expendable threads by the runtime.
    * If all foreground threads complete their execution or are terminated, the runtime will abruptly terminate any remaining background threads, regardless of their state or progress.
    * Background threads are typically used for executing non-critical tasks that can be safely terminated if the application needs to exit, such as periodic background tasks, monitoring tasks, or tasks that can run in parallel with the main application logic.
    * You can mark a thread as background by setting its IsBackground property to true.

4. How to create thread using C#? 
using the Thread class from the System.Threading namespace. Here's a basic example of how to create and start a new thread:

using System;
using System.Threading;

class Program
{
    static void Main(string[] args)
    {
        // Create a new thread and pass a method to execute
        Thread thread = new Thread(DoWork);

        // Start the thread
        thread.Start();

        // Main thread continues here while the new thread executes in parallel
        Console.WriteLine("Main thread continues...");

        // Wait for the new thread to finish before exiting the program
        thread.Join();
        Console.WriteLine("New thread finished. Exiting the program.");
    }

    static void DoWork()
    {
        // Simulate some work
        for (int i = 0; i < 5; i++)
        {
            Console.WriteLine($"Thread is running... {i}");
            Thread.Sleep(1000); // Sleep for 1 second
        }
    }
}

5. What are thread priorities? Why used?
Thread priorities are a mechanism provided by operating systems to control the scheduling of threads in a multi-threaded application. Each thread is assigned a priority value, which determines its importance relative to other threads. The operating system scheduler uses these priorities to decide which thread to execute when multiple threads are ready to run.
Thread priorities are typically represented by integer values, often ranging from 0 to 31 or 1 to 10, with higher values indicating higher priority. However, the exact range and mapping to system priorities can vary between different operating systems and runtime environments.
Thread priorities are used for the following reasons:
1. Priority Scheduling: Thread priorities allow the operating system to schedule threads in a way that gives preference to higher-priority threads over lower-priority ones. This can be useful for ensuring that critical tasks, such as real-time processing or user interface responsiveness, receive preferential treatment over less critical background tasks.
2. Resource Allocation: Thread priorities can influence the allocation of CPU resources among threads. Higher-priority threads are typically given more CPU time than lower-priority threads, allowing them to make progress more quickly. This can be important for ensuring that time-critical tasks meet their deadlines and that system resources are used efficiently.
3. Responsiveness: By assigning higher priorities to threads responsible for user interaction or time-sensitive operations, applications can maintain responsiveness even under heavy load. For example, a user interface thread might be given a higher priority to ensure that user input is processed promptly and smoothly.
4. Deadlock Avoidance: In some cases, adjusting thread priorities can help avoid potential deadlocks or livelocks by ensuring that certain threads are scheduled to run before others. For example, a lower-priority background thread might yield the CPU to a higher-priority thread when accessing shared resources, reducing the risk of contention and deadlock.
It's important to use thread priorities judiciously and with an understanding of their implications. Setting thread priorities too high can lead to starvation of lower-priority threads and potentially degrade overall system performance. Additionally, thread priorities should not be relied upon as the sole means of ensuring timely execution or resource allocation, as they are subject to the scheduling policies and limitations of the underlying operating system.

6. What is multi-threaded application?
A multi-threaded application is like a busy worker who can do many things at once. Instead of doing one task at a time, it can handle multiple tasks simultaneously. This makes the program faster and more efficient because it can use the computer's resources better. However, it also needs careful planning to avoid problems like tasks bumping into each other or fighting over resources. So, while multi-threaded applications are great for getting things done quickly, they need to be handled with care to work smoothly.

7. What is asyncronous operation? 
 In computer programming, an asynchronous operation refers to a computational task that operates independently of the main program flow. Instead of blocking the program execution until completion, asynchronous operations are initiated and allowed to proceed concurrently with other tasks. This non-blocking behavior enables the program to execute additional operations while waiting for the asynchronous task to complete. Asynchronous programming is commonly used in scenarios where certain tasks, such as I/O operations or network requests, may introduce latency or unpredictable delays. By utilizing asynchronous operations, programs can maintain responsiveness and optimize resource utilization by efficiently managing the execution of concurrent tasks.

8. What are difficulties with building multi-threaded applications?
Creating multi-threaded applications is tough because you have to handle shared resources carefully to prevent conflicts between threads. Ensuring that data remains safe across threads adds complexity, and managing synchronization between threads introduces overhead. Debugging becomes challenging due to timing-related issues, and optimizing performance without slowing down the program is tricky. Additionally, designing for scalability across multiple cores or distributed systems requires careful planning. Overall, building multi-threaded applications demands a good grasp of concurrency concepts and thoughtful design to overcome these difficulties.

9. How to setup periodic operation? Timer, CronJobs, etc.
Setting up periodic operations can be accomplished using various techniques such as timers, cron jobs, or scheduling libraries depending on the programming environment and requirements:
1. Timers: In programming languages like JavaScript, you can use timers such as setTimeout() or setInterval() to execute functions periodically. These functions allow you to schedule code to run after a specified delay or at regular intervals.
2. Cron Jobs: Cron is a time-based job scheduler in Unix-like operating systems. You can create cron jobs by editing the crontab file to specify the schedule and the command or script to execute at the specified times. Cron provides a flexible way to schedule periodic tasks with fine-grained control over timing.
3. Scheduling Libraries: Many programming languages offer scheduling libraries or frameworks that provide higher-level abstractions for setting up periodic operations. These libraries often offer features like task scheduling, interval-based execution, and error handling. Examples include APScheduler in Python or Quartz Scheduler in Java.
4. Operating System Services: Some operating systems provide built-in scheduling services for managing periodic tasks. For instance, Windows Task Scheduler allows users to schedule tasks to run at specified times or intervals.
5. Cloud Services: In cloud environments, you can often utilize platform-specific services for scheduling periodic tasks. For example, AWS Lambda allows you to schedule functions to run at regular intervals using CloudWatch Events.
Each approach has its advantages and is suitable for different scenarios. It's essential to consider factors such as ease of use, platform compatibility, and the level of control required when choosing the appropriate method for setting up periodic operations in your application.

5. What languages support CLR? 
CLR primarily supports languages that adhere to the Common Language Infrastructure (CLI) specifications. Languages like C#, VB.NET, F#, Managed C++, IronPython, IronRuby, and Windows PowerShell have direct support for CLR. While other languages can also work with .NET Framework through extensions or interoperability mechanisms, these languages seamlessly integrate with CLR, making them popular choices for .NET development.

6. What is namespace?  Namespace allows for the logical grouping of related and developers typically use them to make it easier to locate a particular type.
The CLR doesn’t know anything about namespaces. When you access a type, the CLR needs to know the full name of the type (which can be a really long name containing periods) and which assembly contains the definition of the type so that the runtime can load the proper assembly, find the type, and manipulate it.

7. What is unmanaged code? 
What language offers ability to write such code? 
What are benefits/problems compared to managed code?
Unmanaged code refers to programming code that is directly executed by the operating system without the need for a runtime environment or managed execution environment. In unmanaged code, developers have direct control over memory management, resource allocation, and other low-level system interactions. This type of code is typically written in languages like C or C++.
Languages like C and C++ offer the ability to write unmanaged code. These languages provide direct access to system resources and hardware, allowing developers to write code that interacts closely with the underlying operating system without the overhead of a managed runtime environment.
Benefits:
* Performance: Unmanaged code often offers better performance compared to managed code since it directly interacts with system resources without the overhead of a runtime environment.
* Control: Developers have fine-grained control over memory management and system resources, allowing for optimizations tailored to specific hardware or performance requirements.
* Access to system-level functionality: Unmanaged code allows developers to access low-level system functionality and hardware features that may not be available or easily accessible in managed environments.
Problems:
* Memory management: With great power comes great responsibility. Unmanaged code requires manual memory management, which can lead to memory leaks, buffer overflows, and other security vulnerabilities if not handled carefully.
* Portability: Unmanaged code may be less portable across different platforms compared to managed code, as it often relies on platform-specific features and system calls.
* Safety and stability: Due to the lack of automatic memory management and runtime checks, unmanaged code is more prone to bugs, crashes, and security vulnerabilities if not carefully written and tested.

8. What is managed module? 
A managed module is a compiled unit of code that targets a runtime environment with built-in memory management, such as the Common Language Runtime (CLR) in the .NET framework. In managed modules, the runtime environment is responsible for various tasks including memory allocation, garbage collection, exception handling, and security enforcement.
Managed modules typically contain code written in high-level languages like C#, Visual Basic .NET, or F#, and are compiled into an intermediate language (IL) format. This IL code is then executed by the CLR at runtime, allowing for platform independence and runtime optimizations.
Managed modules offer several benefits:
* Automatic memory management: The runtime environment automatically handles memory allocation and deallocation, reducing the risk of memory leaks and buffer overflows.
* Security: The runtime environment enforces security policies such as code access security, ensuring that code cannot perform unauthorized actions.
* Interoperability: Managed modules can easily interact with other managed code and components, regardless of the language they were written in.
* Portability: Since managed code is executed by a runtime environment, it can run on any platform that supports the runtime, facilitating cross-platform development.
managed modules provide a higher level of abstraction and developer productivity compared to unmanaged code, as they offload many low-level tasks to the runtime environment.

9. What is friend assemblies? 
Friend assemblies" is a concept in the .NET framework that allows one assembly to access the internal types and members of another assembly, as if they were declared as public. In .NET, assemblies are the building blocks of applications, containing compiled code, resources, and metadata.
When an assembly is marked as a friend assembly of another assembly, it gains privileged access to the internal implementation details of the other assembly. This access is typically restricted to types and members that are marked as internal or protected internal in the target assembly.
Friend assemblies are useful in scenarios where multiple assemblies need to work closely together or share implementation details while maintaining encapsulation and abstraction boundaries. However, they should be used with caution, as they can potentially lead to tight coupling between components and make it harder to maintain or evolve the codebase.
[assembly: InternalsVisibleTo("FriendAssemblyName")]

11. What properties does System.Object has and why they are used?
The System.Object class in C# is the ultimate base class for all other classes in the .NET framework. It provides a set of fundamental properties and methods that are inherited by all other types in C#. Some of the key properties of System.Object include:
1. ToString(): Returns a string representation of the current object. This method is often overridden in derived classes to provide a meaningful string representation of the object's state.
2. Equals(Object): Determines whether the current object is equal to another object. By default, this method performs a reference equality check, but it can be overridden in derived classes to provide custom equality comparison logic.
3. GetHashCode(): Returns a hash code for the current object. This method is used in hash-based collections such as dictionaries and hash sets to efficiently store and retrieve objects.
4. GetType(): Returns the runtime type of the current instance as a Type object. This method is commonly used for reflection and type-based operations.
5. ReferenceEquals(Object, Object): Determines whether two object references refer to the same object instance. This method performs a reference equality check similar to the == operator.
These properties and methods are essential for working with objects in C# and are used in various scenarios such as string formatting, equality comparisons, hash code generation, and runtime type introspection. By providing a common set of behavior for all types, System.Object forms the foundation of object-oriented programming in C# and enables polymorphism, inheritance, and other core concepts of the language.

13. How do you build your own types in C#?  Create Person model?
To build your own types in C#, you typically use classes. Here's how you can create a Person model:
// Define the Person class
public class Person
{
    // Properties
    public string FirstName { get; set; }
    public string LastName { get; set; }
    public int Age { get; set; }
    public Person(string firstName, string lastName, int age)
    {
        FirstName = firstName;
        LastName = lastName;
        Age = age;
    }
    public void Introduce()
    {
        Console.WriteLine($"Hello, my name is {FirstName} {LastName} and I am {Age} years old.");
    }
}
This Person class has three properties (FirstName, LastName, and Age) to represent attributes of a person. It also has a constructor to initialize these properties when creating a new Person object, and a method Introduce() to introduce the person by printing their name and age.

14. Reference vs Value types?  done

15. Is string reference or value type?
String is reference type.

16. What is string immutability?
17. How to build complex string in C#?
18. Explain the following types:
  18.1 class
  18.2 object
  18.3 interface
  
19. Describe and explain each of the following keywords:
  19.2 abstract (both in class and method level) done
  19.3 new (both operator and keyword used before methods? done
  19.6 instance constructors vs static constructors. done
  19.7 constants - how they are treated under the hood done
  19.8 instance constructors in reference vs value types d

21. Overload vs  override done
22. What is explicit vs implicit casting?  done
23. How to convert from one type to another? done
24. What is auto-property? Why not use fields directly? done 
25. What are static classes? How they are treated by CLR? done
27. What is var? done  
28. What is dynamic? dynamic vs var done 
29. What props does Exception type has?
30. ReferenceEquals vs Equals? 
20. What are Design Principles? Why we need them?

21. What Design Principles you know?

22. Explain the following:
	22.1 Program to an Interface, not an Implementation
	22.2 Encapsulate What Varies (application-, class- and method-level)
	22.3 Favor Composition Over Inheritance
23. How practically you used above-mentioned principles in your projects?
24.What is Dependency Inversion?
25.What is Inversion of Control?
26.What is Dependency Injection?
27.What is IoC Container?
16. What is NGen.exe?
17. Why to translate into IL? Can't we make CLR understand C# directly?
8. Describe CLRs execution model?

6. Wrap those operations in stored procedures (use print())
7. Call stored procedured 
8. Create clustered index for firstname + lastname of student
9. Find and show exection plan?
10. Use SQL Profiler
1. What is SQL?
Structured query language (SQL) is a programming language for storing and processing information in a relational database. A relational database stores information in tabular form, with rows and columns representing different data attributes and the various relationships between the data values. You can use SQL statements to store, update, remove, search, and retrieve information from the database. You can also use SQL to maintain and optimize database performance.
Structured query language (SQL) is a popular query language that is frequently used in all types of applications. Data analysts and developers learn and use SQL because it integrates well with different programming languages. For example, they can embed SQL queries with the Java programming language to build high-performing data processing applications with major SQL database systems such as Oracle or MS SQL Server. SQL is also fairly easy to learn as it uses common English keywords in its statements
SQL was invented in the 1970s based on the relational data model. It was initially known as the structured English query language (SEQUEL). The term was later shortened to SQL. Oracle, formerly known as Relational Software, became the first vendor to offer a commercial SQL relational database management system.

How does SQL work?
Structured query language (SQL) implementation involves a server machine that processes the database queries and returns the results. The SQL process goes through several software components, including the following. 
Parser
The parser starts by tokenizing, or replacing, some of the words in the SQL statement with special symbols. It then checks the statement for the following:
Correctness
The parser verifies that the SQL statement conforms to SQL semantics, or rules, that ensure the correctness of the query statement. For example, the parser checks if the SQL command ends with a semi-colon. If the semi-colon is missing, the parser returns an error.
Authorization
The parser also validates that the user running the query has the necessary authorization to manipulate the respective data. For example, only admin users might have the right to delete data. 
Relational engine
The relational engine, or query processor, creates a plan for retrieving, writing, or updating the corresponding data in the most effective manner. For example, it checks for similar queries, reuses previous data manipulation methods, or creates a new one. It writes the plan in an intermediate-level representation of the SQL statement called byte code. Relational databases use byte code to efficiently perform database searches and modifications. 
Storage engine
The storage engine, or database engine, is the software component that processes the byte code and runs the intended SQL statement. It reads and stores the data in the database files on physical disk storage. Upon completion, the storage engine returns the result to the requesting application.

2. What is DBMS?
3. What is Key?
4. What is Composite Key?
5. What is index?
6. What types of indexes do you know?
7. What is clustered index? Non-clustered?
8. What is database integrity?
9. What is transaction?
10. What is Function and Stored Procedure?
A stored procedure is a prepared SQL code that you can save, so the code can be reused over and over again.
So if you have an SQL query that you write over and over again, save it as a stored procedure, and then just call it to execute it.
You can also pass parameters to a stored procedure, so that the stored procedure can act based on the parameter value(s) that is passed.

what is view?
https://www.datacamp.com/tutorial/views-in-sql?utm_source=google&utm_medium=paid_search&utm_campaignid=19589720824&utm_adgroupid=157156376591&utm_device=c&utm_keyword=&utm_matchtype=&utm_network=g&utm_adpostion=&utm_creative=698229374839&utm_targetid=dsa-2218886984820&utm_loc_interest_ms=&utm_loc_physical_ms=1028523&utm_content=&utm_campaign=230119_1-sea~dsa~tofu_2-b2c_3-row-p2_4-prc_5-na_6-na_7-le_8-pdsh-go_9-na_10-na_11-na-may24&gad_source=1&gclid=CjwKCAjwi_exBhA8EiwA_kU1MgUR2LKM9yv8BN5hHvDZLUDSd2qQVf-Lmp_so-f3rWMkCAMVOnf3gRoC7vIQAvD_BwE

11. What are normal forms? 1NF?
The First Normal Form – 1NF
For a table to be in the first normal form, it must meet the following criteria:
* a single cell must not hold more than one value (atomicity)
* there must be a primary key for identification
* no duplicated rows or columns
* each column must have only one value for each row in the table
The Second Normal Form – 2NF
The 1NF only eliminates repeating groups, not redundancy. That’s why there is 2NF.
A table is said to be in 2NF if it meets the following criteria:
* it’s already in 1NF
* has no partial dependency. That is, all non-key attributes are fully dependent on a primary key.
The Third Normal Form – 3NF
When a table is in 2NF, it eliminates repeating groups and redundancy, but it does not eliminate transitive partial dependency.
This means a non-prime attribute (an attribute that is not part of the candidate’s key) is dependent on another non-prime attribute. This is what the third normal form (3NF) eliminates.
So, for a table to be in 3NF, it must:
* be in 2NF
* have no transitive partial dependency.
12. What is execution plan?
13. What is SQL Profiler?
1. What is ERD?
2. What is Foreign Key?
3. What is Primary Key?
4. What is Self-Referencing Foreign Key?
5. What are primary vs secondary models?
6. What relationships do you know among SQL Tables?
7. What is ORM?
8. What is SQLite?
9. How to use SQLite in .NET apps?
10. What is CRUD? How to do in using EF core?

3. Hassan Habib ko'rsatganlaridek API loyihasi, Unit Test loyihasi yaratilsin
4. VideoMetadata classi yaratilsin. LoyihaNomi/Models/VideoMetadatas/VideoMetadata.cs 
5 3ta PR bo'lsin:
	5.1 INFRA: Initialize API Project (MERGED)
	5.2 INFRA: Initialize Unit Test Project (MERGED)
	5.3 DATA: Add VideoMetadata (OPEN)

question for teacher when we create repo on terminal should we create on github or something..l
