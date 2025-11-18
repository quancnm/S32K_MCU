# Cortex Microcontroller Software Interface Standard (CMSIS)

---

## 1. Software Interface

### 1.1. Definition of Interface
In computing, an interface is a shared boundary across which two or more separate components of a computer system exchange information. The exchange can be between software, computer hardware, peripheral devices, humans, and combinations of these.

### 1.2. Definition of Software Interface
A software interface is used to allow either:
- two pieces of software to communicate with each other (**software–software interface**), or  
- software to communicate with a hardware device (**software–hardware interface**).

---

## 2. Common Microcontroller Software Interface Standard (CMSIS) Overview

### 2.1. Definition
- The CMSIS is a vendor-independent hardware abstraction layer for microcontrollers that are based on Arm® Cortex® processors.  
- The CMSIS defines generic tool interfaces and enables consistent device support.  
- It provides simple software interfaces to the processor and the peripherals, simplifying software re-use, reducing the learning curve for microcontroller developers, and reducing the time to market for new devices.

---

### 2.2. CMSIS Components

## **CMSIS Base Software Components**  
Provide software abstractions for basic level functionalities of a device. Maintained in the same GitHub repository and delivered as one CMSIS Software Pack (**Arm::CMSIS**).

- **CMSIS-Core**  
  Standardized access to Arm Cortex processor cores

- **CMSIS-Driver**  
  Generic peripheral driver interfaces for middleware

- **CMSIS-RTOS2**  
  Common API for real-time operating systems

---

## **CMSIS Extended Software Components**  
Implement specific functionalities optimized for execution on Arm processors. Delivered in standalone CMSIS-Packs.

- **CMSIS-DSP**  
  Optimized compute functions for embedded systems

- **CMSIS-NN**  
  Efficient and performant neural network kernels

- **CMSIS-View**  
  Event Recorder and Component Viewer technology

- **CMSIS-Compiler**  
  Retarget I/O functions of the standard C run-time library

---

## **CMSIS Tools**  
Provide utilities for software development workflows with CMSIS-based components.

- **CMSIS-Toolbox**  
  Command-line tools to work with software packs

- **CMSIS-Stream**  
  Tools and methods for optimizing DSP/ML block data streams

- **CMSIS-DAP**  
  Firmware for debug units interfacing to CoreSight Debug Access Port

- **CMSIS-Zone**  
  Defines methods to describe system resources and partition them

---

## **CMSIS Specifications**  
Define methodologies and workflows for embedded software development.

- **CMSIS-Pack**  
  Delivery mechanism for software components and device/board support

- **CMSIS-SVD**  
  Peripheral description of a device for debug view

---

### 2.3. Benefits of the CMSIS

- CMSIS reduces the learning curve, development costs, and time-to-market.  
- Consistent software interfaces improve software portability and re-usability.  
- Provides interfaces for debug connectivity, peripheral views, device support.  
- Compiler independent — compatible with common compilers.  
- Enhances debugging with peripheral info and ITM printf-style output.  
- CMSIS-Packs simplify delivery, updates, and tool integration.  
- CMSIS-Zone simplifies configuration of processors, memory, peripherals.  
- CMSIS-Toolbox supports IDE and CI workflows (CMake backend, VS Code integration).

---

### 2.4. Coding Rules

Essential CMSIS coding rules:

- Compliant with **ANSI C (C99)** and **C++ (C++03)**  
- Uses data types from `<stdint.h>`  
- Variables and parameters have complete data types  
- Expressions for `#define` constants use parentheses  
- Conforms to MISRA 2012 (violations documented)

Naming conventions:

- **CAPITAL** → core registers, peripheral registers, CPU instructions  
- **CamelCase** → function names and interrupt functions  
- **Namespace_Prefix** → avoid naming conflicts  

Doxygen example:

/**
 * @brief  Enable Interrupt in NVIC Interrupt Controller
 * @param  IRQn  interrupt number that specifies the interrupt
 * @return none.
 * Enable the specified interrupt in the NVIC Interrupt Controller.
 * Other settings of the interrupt such as priority are not affected.
 */

 
## 3. CMSIS-Core (Cortex-M)

### 3.1. Overview
CMSIS-Core (Cortex-M) implements the basic run-time system for a Cortex-M device and gives the user access to the processor core and the device peripherals.  
In detail it defines:

- Hardware Abstraction Layer (HAL) for Cortex-M processor registers with standardized definitions for the SysTick, NVIC, System Control Block registers, MPU registers, FPU registers, and core access functions.
- System exception names to interface to system exceptions without having compatibility issues.
- Methods to organize header files that make it easy to learn new Cortex-M microcontroller products and improve software portability. This includes naming conventions for device-specific interrupts.
- Methods for system initialization to be used by each MCU vendor. For example, the standardized `SystemInit()` function is essential for configuring the clock system of the device.
- Intrinsic functions used to generate CPU instructions that are not supported by standard C functions.
- A variable to determine the system clock frequency which simplifies the setup of the SysTick timer.

---

### 3.2. CMSIS in use
To use the CMSIS-Core (Cortex-M), the following files are added to the embedded application:

- **Startup File**  
  `startup_<device>.c`  
  (formerly `startup_<device>.s`, now deprecated)  
  Includes reset handler and exception vectors.

- **System Configuration Files**  
  `system_<device>.c` and `system_<device>.h`  
  Provide general device configuration (e.g., clock and BUS setup).

- **Device Header File**  
  `<device.h>`  
  Gives access to processor core and all peripherals.


