# nand2tetris -- 虛擬機

## Node.js 執行

```
$ node vmh Class1
[
  "// This file is part of www.nand2tetris.org",
  "// and the book \"The Elements of Computing Systems\"",
  "// by Nisan and Schocken, MIT Press.",
  "// File name: projects/08/FunctionCalls/StaticsTest/Class1.vm",
  "",
  "// Stores two supplied arguments in static[0] and static[1].",
  "function Class1.set 0",
  "push argument 0",
  "pop static 0",
  "push argument 1",
  "pop static 1",
  "push constant 0",
  "return",
  "",
  "// Returns static[0] - static[1].",
  "function Class1.get 0",
  "push static 0",
  "push static 1",
  "sub",
  "return",
  ""
]
============== pass1 ================
// init
@256
D=A
@RSP
M=D
@LABEL1
D=A
@SP
A=M
M=D
@R1
D=M
@SP
A=M
M=D
@R2
D=M
@SP
A=M
M=D
@R3
D=M
@SP
A=M
M=D
@R4
D=M
@SP
A=M
M=D
@5
D=A
@R0
AD=A-D
@R2
M=D
@R0
D=M
@R1
M=D
@Sys.init
0; JMP
label LABEL1
// function Class1.set 0
label Class1.set
// push argument 0
@0
D=A
@argument
A=M
AD=D+A
D=M
@SP
A=M
M=D
// pop static 0
@SP
A=M
D=M
@Class1.0
M=D
// push argument 1
@1
D=A
@argument
A=M
AD=D+A
D=M
@SP
A=M
M=D
// pop static 1
@SP
A=M
D=M
@Class1.1
M=D
// push constant 0
@0
D=A
@SP
A=M
M=D
// return
@R1
D=M
@R13
M=D
@5
A=D-A
D=M
@R14
M=D
@argument
AD=M
@R15
M=D
@SP
A=M
D=M
@R15
A=M
M=D
@R2
D=M
@R0
M=D+1
@R13
D=M
D=D-1
@R13
M=D
A=D
D=M
@R4
M=D
@R13
D=M
D=D-1
@R13
M=D
A=D
D=M
@R3
M=D
@R13
D=M
D=D-1
@R13
M=D
A=D
D=M
@R2
M=D
@R13
D=M
D=D-1
@R13
M=D
A=D
D=M
@R1
M=D
@R13
D=M
D=D-1
@R13
M=D
A=D
D=M
@R14
M=D
0; JMP
// function Class1.get 0
label Class1.get
// push static 0
@Class1.0
D=M
@SP
A=M
M=D
// push static 1
@Class1.1
D=M
@SP
A=M
M=D
// sub
@SP
M=M-1
@SP
A=M
D=M
@SP
M=M-1
@SP
A=M
A=M
D=A-D
@SP
A=M
M=D
@SP
M=M+1
// return
@R1
D=M
@R13
M=D
@5
A=D-A
D=M
@R14
M=D
@argument
AD=M
@R15
M=D
@SP
A=M
D=M
@R15
A=M
M=D
@R2
D=M
@R0
M=D+1
@R13
D=M
D=D-1
@R13
M=D
A=D
D=M
@R4
M=D
@R13
D=M
D=D-1
@R13
M=D
A=D
D=M
@R3
M=D
@R13
D=M
D=D-1
@R13
M=D
A=D
D=M
@R2
M=D
@R13
D=M
D=D-1
@R13
M=D
A=D
D=M
@R1
M=D
@R13
D=M
D=D-1
@R13
M=D
A=D
D=M
@R14
M=D
0; JMP
```