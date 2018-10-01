# System Calls:

## fork()
- The calling process gets duplicated.
- The new one has the same content but a different memorie space.
- pid_t fork(void);
- fails when: you dont have enough space.

## stat()
- It gives back information about a file, in the buffer pointed to by statbuf.
- You dont need any permissions for the file, but you need per ission on all of the directories in pathname that lead to the file.
- int stat(const char *pathname, struct stat *statbuf)*;
- fails when: when you dont have the needed permissions.

## kill()
- It sends a specified signal to the specified processes or process groups.
- Normaly the signal terminates the process or groups.
- kill
- kill -l
- fails when: when the specified signal is invalid.

## mmap()
- creates a new mapping in the virtual address space of the calling process.
- void *mmap(void *addr, size_t length, int prot, int flags, int fd, off_t offset)*;
- fails when: too much memory has been locked.

## chmod()
- changes the mode of the file specified.
- int chmod(const char *pathname, mode_t mode)*;
- fails when: the named file does not exist

## waitpid()
-
- pid_t waitpid(pid_t pid, int *status, int options)*;

## exec()
- fais when: the total number of bytes in the environment and argument list is too large

## unlink()
- pathname points outside your accessible address space

## read()
- fd is not a valid file descriptor or is not open for reading

## mount()
- when the pointer points out of our adress space

# TRAP
- Trap is also known as exeption or fault, and it is a type of an synchronous interruption, by an sxceptional condition like a breakpoint or an error
