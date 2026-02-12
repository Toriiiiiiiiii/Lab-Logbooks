# Computer Systems I Logbook - Lab S3
## 12/11/2025

### 2
* The return code from `asm1` is `0`. Based on the source code, I expected a return code of `256`. This means that return codes are only one byte in size.

### 3
* The biggest number that can be returned is `255`, and therefore there are `8` bits in the return code.

### 4
* The code returns `0` as I would expect, as the value of `r1` is `0`, which is not greater than `13`.
* By changing the value of `r1` to `14`, the output changes to `42`.
* By changing the branch instruction to `bge`, the output changes to `42`.

### 5
* The code returns `15` instead of `5` which does not match up with the original description of the program, which should print out `5`.
* The return code of the program is not zero.
* Adding in another call to `printf` causes a segmentation fault as no format string was provided.
* `printf` returns the number of bytes written to the output.

### 6.
* The maximum value that can be factorialed with this is 12, as 13! results in an overflow.
* As such, the first value of factorial that breaks is 13!, which gives 1932053504 instead of the expected 479001600.
* If zero! is done with my implementation, the program hangs.

### 7. 
* The stack pointer is jumping around randomly on the stack as values are pushed/popped by other processes and the OS.
* Running `stack` several times gives the same output.
* The output of `stack`, 8, shows that, after pushing 2 values onto the stack, `sp` decreases by 8.
* This means that the width of the stack is 4 bytes (32 bits), and that the stack is growing downwards.
