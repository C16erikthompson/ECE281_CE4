ECE281_CE4
==========
#Prism Summary
Programmable Reconfigurable Informational Simple Microcomputer (PRISM) is a small-scale
version of a typical digital computer that operates using numbers in hexadecimal.
To program in PRISM, a specific set of sommands are used that allow the programmer
to manipulate memory to include RAM, an accumlator, an input, and an output.  These
commands use three types of addressing: inherent, immediate, and direct.  
Inherent addressing uses data that is already preent in the datapath, while immediate 
addressing uses additional data saved immediately after the opcode in memory.  Direct addressing
requires the program to access a specific point in memory.
Inherent addressing includes the following commands:

•	NOP (016) No Operation

•	NEG (116) Negate the value in the accumulator (generate the 2's complement)

•	NOT (216) Complement the value in the accumulator (generate the 1's complement)

•	ROR (316) Rotate each bit in the accumulator right by one position (and ‘wrap’ 
  the  least-significant bit around to the most-significant bit’s position)
  
Immediate addressing includes the following commands:

•	ADDI (616) Add “immediately” the value of the second word to the value in the accumulator; 
•	LDAI (716) Load (copy) “immediately” the second word to the accumulator

Direct addressing includes the following commands:

•	OUT (416) Output (copy) the value in the accumulator to the addressed I/O port; Second word is the port address
•	IN (516) Input (copy) the value at the addressed I/O port to the accumulator; Second word is the port address
•	AND (816) AND the value located at the memory address (formed by the second and third words
  of the instruction) with the value in the accumulator
•	JMP (916) Unconditional jump (transfer program execution) to the instruction located at the
  memory address (formed by the second and third words of the instruction)
•	JZ  (A16) Jump (transfer program execution) to the instruction located at the memory address
  (formed by the second and third words of the instruction) if the value in the accumulator = 0
•	JN  (B16) Jump (transfer program execution) to the instruction located at the memory address 
  (formed by the second and third words of the instruction) if the most significant bit of the
  accumulator = 1 (indicating the value in the accumulator represents a negative number)
•	OR  (C16) OR the value located at the memory address (formed by the second and third words of
  the instruction) with the value in the accumulator
•	STA (D16) Store (copy) the value in the accumulator at the memory address (formed by the second
  and third words of the instruction)
•	ADDD (E16) Add “directly” the value located at the memory address (formed by the second and third
  words of the instruction) to the value in the accumulator
•	LDAD (F16) Load (copy) “directly” into the accumulator the value at the memory address (formed by
  the second and third words of the instruction)

#Summary of PRISM Architecture

•	PRISM contains four major subsystems
•	Controller
•	Datapath
•	Memory Subsystem
•	Input/Output (I/O) Subsystem
	
•	PRISM is a bus-structured computer with three major busses
•	Bi-directional Data Bus
•	Address Bus
•	Control Bus
•	Datapath Control Lines
•	Datapath Status Lines
•	I/O and Memory Control Lines
