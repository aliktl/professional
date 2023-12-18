
4. **What is GIL and why is it important?**

    Answer №1: GIL is one of the most controversial and important features of the CPython-based implementation of Python. GIL, or Global Interpreter Lock, is a construct/tool that makes sure that only one thread at a time can execute a Python program. In other words, this lock belongs to the Python interpreter and it uses it to lock a thread.

    For example, thread T1 acquires GIL and does its job. While the Python interpreter is using GIL to lock T1, all other threads have to wait. After T1 finishes, it releases GIL and passes it to another thread T2 that needs it. The reason for the GIL presence is to make CPython thread-safe and not allow some threads to interfere with one another.
