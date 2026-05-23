# Syscalls

A list of system calls supported by DIOS

## `0x40` Print

### `0x0040` Print character to serial port

This will print to the serial port the contents of the G0 register and block until the transmission has completed.

### `0x0140` Print string to serial port

This will print a null-terminated string pointed to by G0 to the serial port and block until the transmission has completed.
