# A process virtual machine for LC-3

[This](https://www.andreinc.net/2021/12/01/writing-a-simple-vm-in-less-than-125-lines-of-c)
fantastic blog post by Andrei Ciobanu directly inspired this project. Our humble
VM has 65535 (`UINT16_MAX`) words of 16 bits each. We also have ten 16-bit
registers. Our opcode is always the leading four bits of each instruction, which
gives us a maximum of `2^4=16` instructions. However, we only implemented 14
instructions because `RTI` did not make sense to implement, and `0xD` is a
reserved opcode.