# Syscalls

A list of system calls supported by DIOS

## `0x40` Print

### `0x0040` Print character to serial port

This will print to the serial port the contents of the G0 register and block until the transmission has completed.

### `0x0140` Print string to serial port

This will print a null-terminated string pointed to by G0 to the serial port and block until the transmission has completed.

## `0x41` Char in

### `0x0041` Char in from serial port

This will return the next key in the serial port input buffer to G0. If the buffer is empty, 0 is returned.

### `0x0141` Char in from keyboard

This will return the next key in the keyboard input buffer to G0. If the buffer is empty, 0 is returned.

NOTE: only regular characters and their shifted versions are currently implemented.

## `0x42` Sleep

NOTE: Sleeping may result in corrupted keyboard/serial input. To be fixed

### `0x0042` Microsecond sleep

This will block for the number of microseconds provided in G0.
