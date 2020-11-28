# Reverse Engineering of Rocket Chip ![](https://github.com/merledu/Reverse-Engineering-of-Rocket-Chip/blob/master/Different%20Modules%20Understanding%20Links%20of%20rocket%20chip/logo%20reverse%20engineering.png)
This repository contains the methodolgy of Reverse Engineering the Rocket Chip. For more information on Reverse engineering of Rocket Chip, please consult our MERL-UIT technical team  at <br/>
https://www.merledupk.org/ .

# Table of Content
* Rocket Chip Overview
* Rocket-Chip Micro-Architecture
* Rocket-Chip Code Complexity
* Rocket Core Scala Files
* Reverse Engineering of Rocket Chip
* Micro Architecture Specification (MAS) Document Rocket Chip
* Motivation And Scope of (MAS) Document Rocket Chip
* Methodology of MAS Document
* Aghaz(آغاز) SoC The Beginning
* Specifications of Aghaz(آغاز) SoC
* How did we do it?
* Blocks of Aghaz(آغاز) Core
* Blocks of Aghaz(آغاز) Tile
* References

# What is Rocket Chip
  * Rocket chip is a chip generator that is used for generating a multi-core system with Rocket scalar cores, Z-Scale control processors, and a coherent memory system
  * Rocket chip generator is coded in Scala that compiles using Chisel compiler to generate a SoC in descriptive RTL
  * The configuration of SOC are specified through Chisel parameters

# Rocket Chip Overview
Detailed diagram of Rocket Chip is shown below
 
 ![1](https://github.com/merledu/Reverse-Engineering-of-Rocket-Chip/blob/master/Different%20Modules%20Understanding%20Links%20of%20rocket%20chip/Rocket%20Chip%20SOC%20Block%20Diagram.PNG)

 

# Rocket Chip Micro Architecture
![](https://github.com/merledu/Reverse-Engineering-of-Rocket-Chip/blob/master/Different%20Modules%20Understanding%20Links%20of%20rocket%20chip/rocket%20chip%20micro%20architecture.JPG)

# Rocket Chip Code Complexity
* The complexity of code of Rocket-chip is high, because it contains 328 source files of scala in 23 directories, and 33,427 total lines of scala code.
* Another issue faced was that Rocket-chip contains several meaningless variable names and non-elaborated comments which further leads to uncertainty in methods, increases the complexity to decode it and makes it tough to understand the hardware inputs/outputs.
* Lack of understandability and comprehension concludes to difficulty in modifying Rocket-core or its component as for customized requirements. 

# Rocket Core Scala Files
This table will gives the complete detail of total number of scala files and their length of code in Rocket Core.

![](https://github.com/merledu/Reverse-Engineering-of-Rocket-Chip/blob/master/Different%20Modules%20Understanding%20Links%20of%20rocket%20chip/core%20level%20lines%20of%20code%20table.PNG)
# Reverse Engineering of Rocket Chip

| Rocket chip is a chip generator that allows you to set up different configurations and these configurations are specified through Chisel parameters. Reverse Engineering of Rocket Chip journey starts from (Micro Electronic Research Lab) MERL which is working in the field of RISC V Processor development and Research. The purpose of Reverse Engineering of Rocket Chip is to get aware of the modules used in rocket chip and make Micro Architecture Specification (MAS) documentation as Rocket chip doesn’t have any MAS documentation available yet. Another main purpose is to increase Rocket chip code reusability so every programmer can easily understand its code and manipulate it according to its desired configuration by changing Chisel Parameters. We decode basic modules of rocket chip by taking an understanding of its code line by line with the help of Scala and Chisel expertise. We convert these modules code understanding into flow charts and start making Micro Architecture Specification (MAS) documentation. We make flow charts for different modules of Rocket Chip. After completion of flow charts, we make block diagrams of Rocket Chip modules according to its configuration pin in and out.  |
| :--- |

# Micro Architecture Specification (MAS) Document Rocket Chip
![](https://github.com/merledu/Reverse-Engineering-of-Rocket-Chip/blob/master/Different%20Modules%20Understanding%20Links%20of%20rocket%20chip/MAS%20Document%20of%20Rocket%20Chip.PNG)</br>
* This MAS Document provides in depth understanding of Modules of Rocket-Chip SoC.
* Explanation of Modules is achieved by means of Block Diagrams, Class Diagrams, Flowcharts, and explanation of all the keywords found in the code.
*  This MAS Document is essential for those who have basic knowledge of Scala, CHISEL and SoC hardware.In explanation only the name of keywords is used but their definition is mentioned in the Appendix – Scala & CHISEL keywords.


## Motivation And Scope of (MAS) Document Rocket Chip
* To explain the workflow to a beginner seeking to understand and use Rocket-core for generating a customized System on chip (SoC) or modifying a module based on their general requirements.
* Provide a hardware  view by  mapping it to blocks of code which highlights the wiring and back tracing of input/output by means of variables. The hardware mapping creates a linkage between software and hardware in entire workflow.
* The Microarchitecture Specification (MAS) Documentation designed by MERL-UIT aims to achieve an elaboration of Rocket-chip at core level and its components in a detailed manner, it furthermore features additional representations such as block diagrams and flowcharts.


## Methodology of MAS Document

* We decode basic modules of rocket chip by taking understanding of its code line by line with the help of Scala and Chisel expertise.
* We convert these modules code understanding into flow charts and start making Micro Architecture Specification (MAS) documentation.
* We make flow charts for different modules of Rocket Chip. After completion of flow charts, we make block diagrams of Rocket Chip modules according to its configuration pin in and out
# Aghaz(آغاز) SoC The Beginning
![](https://github.com/merledu/Reverse-Engineering-of-Rocket-Chip/blob/master/Different%20Modules%20Understanding%20Links%20of%20rocket%20chip/Aghaz%20SOC.PNG)

# Specifications of Aghaz(آغاز) SoC
| Specs of Aghaz(آغاز) |
| :-----: |
| RV-32 (32-bit) |
| I, M & C extensions |
| 64-KB Instruction and Data Cache |
|  CLINT |
| PLIC |
| Privileged( Machine) |
# How did we do it?
|  With the help of MAS Document, which contains in-depth knowledge of all the Modules of Rocket-Chip generated by Rocket-Chip SoC Generator |
| :----- |
# Blocks of Aghaz(آغاز) Core
![](https://github.com/merledu/Reverse-Engineering-of-Rocket-Chip/blob/master/Different%20Modules%20Understanding%20Links%20of%20rocket%20chip/Aghaz%20Core.PNG)

# Blocks of Aghaz(آغاز) Tile
_Rocket-Tile of Aghaz SoC contains_
* Aghaz Core
* Branch Target Buffer 
* L1 Icache
* DCache of 64-KB </br></br>
![](https://github.com/merledu/Reverse-Engineering-of-Rocket-Chip/blob/master/Different%20Modules%20Understanding%20Links%20of%20rocket%20chip/Aghaz%20Tile.PNG)
![]()

## References
### Rocket Chip Module Understanding Table

|  Module Name | Link Description |
| --------------- | --------------- |
| TLB (Target Look aside Buffer) | https://www.youtube.com/watch?v=Z2T2vnyZl0o  <br/> https://www.geeksforgeeks.org/translation-lookaside-buffer-tlb-in-paging/ |
| Priority Encoder | https://www.youtube.com/watch?v=kEj-m3YuGa4&feature=youtu.be |
| BTB(Branch Target Buffer) | https://www.sciencedirect.com/topics/computer-science/branch-target-buffer |
| BHT (Branch History Table) | https://www.youtube.com/watch?v=yk-U6qqeGE0 |
| NPC | https://www.embecosm.com/appnotes/ean7/html/ch04s06s01.html |
| CSR (Control and State Register) | https://people.cs.pitt.edu/~don/coe1502/current/Unit4a/Unit4a.html |
| Cache | https://www.student-circuit.com/learning/year3/embedded-systems/what-are-three-types-of-cache-memory/ |
| Scratchpad memory (SPRAM) | https://www.sciencedirect.com/topics/computer-science/scratchpad-memory |
| Control Flow Integrity (CFI) | https://www.youtube.com/watch?v=LKK7U_gF744 |
| AMBA | https://www.allaboutcircuits.com/technical-articles/introduction-to-the-advanced-microcontroller-bus-architecture/ |
| AXI | https://www.allaboutcircuits.com/technical-articles/introduction-to-the-advanced-extensible-interface-axi/ |
| Aborts and Pre-fetch Aborts | https://developer.arm.com/documentation/ddi0344/c/programmer-s-model/exceptions/aborts |
| CLINT | https://chromitem-soc.readthedocs.io/en/latest/clint.html |
| Coherent Memory | https://whatis.techtarget.com/definition/memory-coherence |
| SISD and SIMD | https://www.quora.com/What-is-the-difference-between-SISD-and-SIMD |
| Superscalar processor | https://www.slideshare.net/ManashKumarMondal/superscalar-processor |
| Position Independent Code (PIC) | https://docs.oracle.com/cd/E26505_01/html/E26506/glmqp.html |
| Adding GPIOS with rocket chip | https://github.com/sifive/sifive-blocks/tree/master/src/main/scala/devices |

