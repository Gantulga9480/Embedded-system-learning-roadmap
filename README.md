# Roadmap for learning Embedded System (ES)

## 1. The Holy C (C programming language, from zero to hero)
[Motivation](https://www.youtube.com/shorts/u_eG4EaZ6uk)

 - C data types, variable, struct, type casting (char, unsigned, signed, long, double, …)
 - Bit wise operations (AND, OR, XOR, Bit shift)
 - Function
 - POINTER (Pointer arithmetic, Array)
 - Static and Dynamic memory allocation/deallocation (Heap Segmentation, Stuck Overflow)
 - Memory structure (Heap, Stuck, Text segment, ...)
 - Code design (Header files, Macros)
 - Algorithm and Data structure

Books are pretty good source for learning C/C++ from scratch. [C++](/files/Cpp%20All%20in%20One%20for%20Dummies%20-%20FreePdf-Books.com.pdf)

## 2. Embedded C (Nothing but C, except few things)
Depends on what microcontroller you're using
 - Build tools
 - Macros
 - Memory layout

I have no available source for these topics. You shoud go into source code or search on internet for that. Sorry :(

## 3. Basics of electronics
### You really need to be careful with electricity to avoid damaging your devices

**Look for "[*why short circuit is dangerous*](https://www.google.com/search?q=why+short+circuit+is+dangerous&sxsrf=AJOqlzV3q4jRhGcILuO6tQbPVyesB3xqsg%3A1674445829404&ei=BQTOY-eoGM-I4-EPwbms0Aw&oq=why+short+c&gs_lcp=Cgxnd3Mtd2l6LXNlcnAQAxgAMgUIABCRAjIFCAAQkQIyBQgAEIAEMgUIABCABDIFCAAQgAQyBQgAEIAEMgUIABCABDIFCAAQgAQyBQgAEIAEMgUIABCABDoKCAAQRxDWBBCwAzoHCCMQ6gIQJzoECCMQJzoECC4QQzoECAAQQzoICC4Q1AIQgAQ6CAguEIAEENQCOgUILhCABEoECEEYAEoECEYYAFDLBljYJWCCLWgDcAF4AYAB-gOIAYUQkgEKMS4xMS4xLjUtMZgBAKABAbABCsgBCMABAQ&sclient=gws-wiz-serp)"**

 - Voltage, Current, Ohms law
 - Usage of basic passive elements (Resistor, Capacitor, Inductor)
 - Usage of basic active elements (Transistors)

[YouTube](https://www.youtube.com/@EngineeringMindset) is a very good teacher.

## 4. Preparing your development environment
[AVR](https://en.wikipedia.org/wiki/AVR_microcontrollers) MCUs (microcontroller unit) are fairly simple and has affordable price.

[Microchip Studio](https://www.microchip.com/en-us/tools-resources/develop/microchip-studio) - IDE for writing, building and programming AVR MCUs

Here's my training combo for AVR Atmega32 MCU.
- USBasp programmer (also known as khazama) [elec.mn](https://elec.mn/category/9/product/61)
- Development board (makes life easier) [elec.mn](https://elec.mn/category/9/product/326)
- AVR Atmega32A - 8 bit MCU [Datasheet](https://ww1.microchip.com/downloads/en/DeviceDoc/Atmega32A-DataSheet-Complete-DS40002072A.pdf)

![mcu-combo](/imgs/mcu-combo.jpg)

#### Examples
I'm planning to add some basic example code for programming Atmega32 MCU. So stay tuned!

## 5. Dive deeper into MCUs
Almost all MCUs have these peripherals and features, but the implementation is different. So you need something like [this](https://ww1.microchip.com/downloads/en/DeviceDoc/Atmega32A-DataSheet-Complete-DS40002072A.pdf).
When it comes to programming embedded devices, the reference manual becomes our best friend.
There are already a plenty of learning resources on the internet. You just need to search for the specific topic.

 - CPU (Arithmetic logic unit, General purpose registers, SRAM, Program counter)
 - Memory (FLASH memory, EEPROM)
 - Registers
 - GPIO (General Purpose Input Output)
 - ADC (Analog to Digital Converter)
 - DAC (Digital to Analog Converter)
 - Timer (clock)
 - Interrupt

## 6. Communication
An embedded system really is a system of microchips or MCUs talking to each other and performing some action/computation. Especially the MCUs have a lot of these communication features built in. For example:
 - UART (Universal asynchronous receiver-transmitter)
 - SPI (Serial Peripheral Interface)
 - IIC (Inter-Integrated Circuit) also called I2C

## 7. Embedded OS (free-RTOS)
Yes. MCUs can have OS (Operating System) like free-RTOS. But unlike Windows or MacOS, the free-RTOS is a light weight open-source OS designed for Embedded devices. These are the topics you would face in learning Embedded OS.
 - Thread (Task)
 - Semaphore (Thread safe, Resource lock)
 - Scheduler (Kernel)

## 8. Memory management
Just don't use dynamic memory allocation. Joke!<br>
If I said this to some devs. They would k*ll me. Yes dynamic memory allocation is necessary.
But the main problem of memory management is **DYNAMIC** memory allocation. You need to be careful about your memory usage. Specially in embedded world. We have so much little space for storing the '\n' a.k.a the NULL character. So you need to collect your garbage by yourself. :)<br>

So that's it. This is my road map for learning Embedded system the HARD WAY.