# oisc_sim
## Registers
| Abbrev. Name | Full Name | Description | 
| ------------ | --------- | ----------- |
| IP | Instruction Pointer | Pointer to current instruction to be executed |
| SP | Stack Pointer | Pointer to current position in the stack |
| SST | Stack Start | The start of the stack segment |
| SSZ | Stack Size | The size of the stack in bytes, n/8 for number of positions |
| DST | Data Start | The start of the data segment |
| DSZ | Data Size | The size of the data segment |
| CST | Code Start | The start of the code segment |
| CSZ | Code Size | The size of the code segment |
| CTR | Counter | Counter used for loops and other operations |
| BST | Buffer Start | The start of a buffer |
| BSZ | Buffer Size | The size of a buffer in bytes |


## Endianness
- The system is little endian

## Integral types
- Maximum value-width is currently 64-bits
- types:
-- Char/Byte: 8 bits/1 byte
-- Word/Short: 16 bits / 2 bytes
-- Long: 32 bits / 4 bytes
-- Long Long: 64 bits / 8 bytes
-- Double: 64-bit double precision value
-- Float: 64-bit float value
- If an operation results in an overflow of the 64-bit value, the overflow flag will be set in the flags register, and the result register will be set to 0xFFFFFFFFFFFFFFFF (-1 signed/MAX_INT unsigned)
-- MAX_INT is: 0xFFFFFFFFFFFFFFFF or 1.844674407371E+19 or 2^64-1
-- for other minimum and maximum values see https://en.wikipedia.org/wiki/Integer_(computer_science)
## Stack
- The stack is 8-byte aligned
