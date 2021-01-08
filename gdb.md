GDB
===

## Catch events

### Catch syscalls (Linux)

```
(gdb) catch syscall SYSCALL_NAME
```

Examples

```
(gdb) catch syscall read
(gdb) catch syscall fork
```

If you have an old GDB and it doesn't support catch syscall by name or you know syscall number you can catch syscall by number.

Example: Catch fork()

```
(gdb) catch syscall 57
```

See

- [sourceware.org: Setting Catchpoints](https://sourceware.org/gdb/onlinedocs/gdb/Set-Catchpoints.html)
- [reverseengineering.stackexchange.com: Setting a breakpoint at system call](https://reverseengineering.stackexchange.com/questions/6835/setting-a-breakpoint-at-system-call)

### Catch a new thread event (Linux)

```
(gdb) catch syscall clone
```

or

```
(gdb) break __pthread_create_2_1
```

See

- [stackoverflow.com: gdb breakpoint on pthread_create](https://stackoverflow.com/questions/1440643/gdb-breakpoint-on-pthread-create)
- man 2 clone

## GDB initialization scripts

- /etc/gdbinit
- ~/.gdbinit
- ./.gdbinit

Source: [systutorials.com: gdbinit (5) - Linux Man Pages](https://www.systutorials.com/docs/linux/man/5-gdbinit/)

## Other

Set Intel syntax for assembly

```
set disassembly-flavor intel
```

## Command history

```
set history save on
```

**Hint:** Add command above to some of initialization scripts(e.g. ~/.gdbinit).

Default path for history is ./.gdb_history

Source: [sourceware.org: Debugging with GDB: 22.3 Command History](https://sourceware.org/gdb/current/onlinedocs/gdb/Command-History.html)

## TODO
 - Remote debugging


