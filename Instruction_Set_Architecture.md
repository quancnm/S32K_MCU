
# Instruction Set Architecture (ISA):

 **Instruction Set Architecture (ISA)** is part of the abstract model of a computer that defines how the CPU is controlled by the software. 
* The ISA acts as an interface between the hardware and the software, specifying both what the processor is capable of doing as well as how it gets done.

* The ISA defines the various **instructions**, **registers** and **memory addressing** modes that the processor would support, at a hardware level. Software created to run on an ISA would be designed to use the ISA's instructions, register and memory addressing modes.



## Complex Instruction Set Computer (CISC): 

 **Complex Instruction Set Computer (CISC)** is a type of microprocessor that is designed with a **large complex set of instructions**. 

* In a CISC processor, a single instruction has **‘several low-level operations’**, which makes the instructions relatively short but inherently complex.

* The primary goal of a CISC processor is to **reduce the number of instructions** in a program, thereby **minimizing overall program size**.

<table>
  <tr>
    <th style="width:70%">Advantages</th>
    <th style="width:50%">Disadvantages</th>
  </tr>
  <tr>
    <td>
      • The code size is comparatively <b>shorter</b>, which <b>minimizes the memory requirement</b>. <br><br>
      • Execution of <b>a single instruction</b> accomplishes <b>several low-level tasks</b>. <br><br>
      • Complex addressing modes make memory access flexible. <br><br>
      • CISC instructions can <b>directly access memory locations</b>.
    </td>
    <td>
      • It requires <b>several clock cycles</b> to execute <b>a single instruction</b>, which reduces overall performance. <br><br>
      • Implementing pipelining for CISC instructions is more complicated. <br><br>
      • The hardware structure must be more complex to simplify software implementation. <br><br>
      • CISC was designed when memory was smaller and costlier; today, memory is inexpensive and abundant, making this design less efficient.
    </td>
  </tr>
</table>

## Reduced Instruction Set Computer (RISC):
 **Reduced Instruction Set Computer (RISC)** is a type of microprocessor that is designed with a **large complex set of instructions**. 

* The main objective of a CISC processor is to minimize the program size by reducing the number of instructions in a program.

### *Advantages*

* There are very fewer instructions in RISC instruction set.

* RISC instruction has simple addressing modes.

* RISC instructions execute one instruction per clock cycle.

* RISC instruction executes faster because most of instruction operates on processor register and there is no need to access memory for each instruction.

* It is easy to pipeline RISC instruction as all instruction is of fixed size and opcode and operand are located in the same position in the word.



### *Disadvantages*

* RISC instruction size is reduced but more instructions are required to perform an operation when compared with CISC

* The machine instructions are hardwired in RISC so, it would cost if any instruction needs modification.

* It finds is difficulty in processing complex instruction and complex addressing mode.

* RISC instructions do not allow direct memory to memory transfer, it requires Load and Store instructions to do so.


# Comparison of RISC and CISC:
## Cấu trúc tập lệnh
|| RISC | CISC |                                                            
|---|---|---|
| Similarity  | Acts as an interface between machine code (software and microarchitecture)
| Difference | RISC is a reduced instruction set| CISC is a complex instruction set                                |

## Tốc độ xử lý
|| RISC | CISC |                                                            
|---|---|---|
| Similarity  | Acts as an interface between machine code (software and microarchitecture)
| Difference | RISC is a reduced instruction set| CISC is a complex instruction set                                |

## Kích thước chương trình
|| RISC | CISC |                                                            
|---|---|---|
| Similarity  | Acts as an interface between machine code (software and microarchitecture)
| Difference | RISC is a reduced instruction set| CISC is a complex instruction set                                |

## Độ phức tạp phần cứng
|| RISC | CISC |                                                            
|---|---|---|
| Similarity  | Acts as an interface between machine code (software and microarchitecture)
| Difference | RISC is a reduced instruction set| CISC is a complex instruction set                                |

## Ứng dụng thực tế
|| RISC | CISC |                                                            
|---|---|---|
| Similarity  | Acts as an interface between machine code (software and microarchitecture)
| Difference | RISC is a reduced instruction set| CISC is a complex instruction set                                |



# Personal thoughts:
I believe that in today’s world, RISC architectures are becoming increasingly suitable for embedded systems due to their high efficiency in power consumption and the simplicity of their hardware design. Since embedded devices often operate on limited battery resources, the low power requirements of RISC processors make them ideal for ensuring longer device lifespans. Moreover, the simpler hardware not only reduces manufacturing costs but also makes the processors more reliable and easier to integrate into compact systems.
