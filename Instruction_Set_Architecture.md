
# Instruction Set Architecture (ISA):

 **Instruction Set Architecture (ISA)** is part of the abstract model of a computer that defines how the CPU is controlled by the software. 
* The ISA acts as an interface between the hardware and the software, specifying both what the processor is capable of doing as well as how it gets done.

* The ISA defines the various **instructions**, **registers** and **memory addressing** modes that the processor would support, at a hardware level. Software created to run on an ISA would be designed to use the ISA's instructions, register and memory addressing modes.



## Complex Instruction Set Computer (CISC): 

 **Complex Instruction Set Computer (CISC)** is a type of microprocessor that is designed with a **large complex set of instructions**. 

* In a CISC processor, a single instruction has **‘several low-level operations’**, which makes the instructions relatively short but inherently complex.

* The primary goal of a CISC processor is to **reduce the number of instructions** in a program, thereby **minimizing overall program size**.

### Advantages and Disadvantages of CISC

<table style="width:100%; table-layout:fixed;">
  <tr>
    <th style="width:50%; text-align:left;">Advantages</th>
    <th style="width:50%; text-align:left;">Disadvantages</th>
  </tr>
  <tr>
    <td style="vertical-align:top;">
      • The code size is comparatively <b>shorter</b>, which <b>minimizes the memory requirement</b>. <br><br>
      • Execution of <b>a single instruction</b> accomplishes <b>several low-level tasks</b>. <br><br>
      • Complex addressing modes make memory access flexible. <br><br>
      • CISC instructions can <b>directly access memory locations</b>.
    </td>
    <td style="vertical-align:top;">
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

### Advantages and Disadvantages of RISC

<table style="width:100%; table-layout:fixed;">
  <tr>
    <th style="width:50%; text-align:left;">Advantages</th>
    <th style="width:50%; text-align:left;">Disadvantages</th>
  </tr>
  <tr>
    <td style="vertical-align:top;">
      • There are very few instructions in the RISC instruction set. <br><br>
      • RISC instructions have simple addressing modes. <br><br>
      • Each RISC instruction executes in a single clock cycle. <br><br>
      • RISC executes faster because most instructions operate on processor registers, avoiding frequent memory access. <br><br>
      • Pipelining is easier since all RISC instructions are of fixed size with opcode and operand in the same position. 
    </td>
    <td style="vertical-align:top;">
      • Although RISC instructions are smaller, more instructions are required to perform an operation compared with CISC. <br><br>
      • Machine instructions are hardwired in RISC, making modifications costly. <br><br>
      • It struggles with complex instructions and complex addressing modes. <br><br>
      • RISC does not allow direct memory-to-memory transfers; it requires separate Load and Store instructions.
    </td>
  </tr>
</table>



## Comparison of RISC and CISC

| **Criteria** | **CISC (Complex Instruction Set Computer)** | **RISC (Reduced Instruction Set Computer)** |
|--------------|---------------------------------------------|---------------------------------------------|
| **Instruction Set Architecture** | Large and complex instruction set; each instruction can perform multiple low-level operations. | Small and simple instruction set; each instruction performs a single, simple task. |
| **Execution Speed** | Slower execution, as one instruction may require multiple clock cycles. | Faster execution, as most instructions complete in a single clock cycle. |
| **Program Size** | Smaller program size, since fewer instructions are needed to perform a task. | Larger program size, as more instructions are required to accomplish the same task. |
| **Hardware Complexity** | More complex hardware design to support complex instructions and addressing modes. | Simpler hardware design, optimized for instruction pipelining and parallel execution. |
| **Practical Applications** | Widely used in traditional desktop and server processors (e.g., Intel x86, AMD). | Common in mobile devices, embedded systems, and modern processors (e.g., ARM, MIPS, RISC-V). |



# Personal thoughts:
I believe that in today’s world, RISC architectures are becoming increasingly suitable for embedded systems due to their high efficiency in power consumption and the simplicity of their hardware design. Since embedded devices often operate on limited battery resources, the low power requirements of RISC processors make them ideal for ensuring longer device lifespans. Moreover, the simpler hardware not only reduces manufacturing costs but also makes the processors more reliable and easier to integrate into compact systems.
