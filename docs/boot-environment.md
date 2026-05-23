# Boot Environment

## Reserved memory

Addresses 0x00008000 to 0x00009FFF are reserved for usage by DIOS for as long as it is required, and all memory at 0x0000A000 and beyond are useable. Once DIOS is no longer required, addresses 0x00008000 to 0x00009FFF may be reclaimed.

## Interrupt table

All interrupts not specified by `syscalls.md` (including all hardware interrupts) are useable by a program. By default, all interrupts unused by DIOS are handled by a stub handler which immediately returns from the interrupt. To add program handling of the interrupt, simply change the entry in the interrupt table to wherever it should be handled, as the interrupt table is stored in RAM. When DIOS is no longer required, the interrupt table must be completely redifined so that DIOS syscalls may not be accidentally invoked in a broken state.
