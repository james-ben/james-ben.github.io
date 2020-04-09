[//]: # (TODO: is there a way to make this more easily downloadable?)
[//]: # (TODO: Better project descriptions, including skills learned)

## Contact

[Email](mailto:bjames@byu.net)  
[LinkedIn](linkedin.com/in/benjamin-james-a83342121)  
[Github](https://github.com/james-ben)


# Skills

- Embedded programming (C)
- Python 3
- Bash scripting
- C++
- LLVM compiler framework
- Embedded Linux
- Detail-oriented
- Black belt in [Kishindo Martial Arts](https://www.facebook.com/BushiKaiKishindo/)


# Work Experience

### Research Assistant - BYU Configurable Computing Lab (May 2017 - Present)

- Primary developer for the Compiler-Assisted Software Fault Tolerance ([COAST](https://github.com/byuccl/coast)) tool
  - Tested performance of tool in radiation beam
  - Increased Mean Time Between Failure (MTBF) on code run with COAST
- Created fault injection simulation tool to test radiation tolerance of processors

### Teaching Assistant - (May - Dec 2018)

- Implemented Linux kernel drivers to interact with the HDMI and audio hardware on the [Xilinx PYNQ](https://www.xilinx.com/support/university/boards-portfolio/xup-boards/XUPPYNQ.html) embedded Linux platform
- Worked to update senior level engineering class to use the Xilinx PYNQ board, supervised by Professor Brad Hutchings


# Projects

### COAST (work)

**CO**mpiler-**A**ssisted **S**oftware fault **T**olerance

[Public Release](https://github.com/byuccl/coast)

An effort to add fault tolerance to Commercial Off-the-shelf (COTS) microcontrollers using software techniques.  

As the primary developer on this project since May 2018, I have accomplished a number of things on this project:

- Expanded support to multiple platforms/architectures
- Worked to support C++ front-end
- Created software test driver for use in a radiation beam
- Automated testsuite using [BuildBot](https://buildbot.net/)

Design challenges:

- LLVM C++ API has [spotty documentation](https://llvm.org/doxygen/index.html)
- Verifying that the protection flags are self-consitent (correct replication scope rules)
- Make sure changes to dataflow don't affect control flow, even when creating new basic blocks

Current/Future Work:

- Creating a fault injection platform on top of the [QEMU emulator](https://www.qemu.org/)
- Support for [FreeRTOS](https://www.freertos.org/)

Mean Work to Failure (MWTF) is a metric used to measure the increase in reliability in systems.  
For a more description, see [Section 7](https://liberty.princeton.edu/Publications/taco05_ft.pdf) or [page 274](https://books.google.com/books?id=gBEpCwAAQBAJ&lpg=PA274&ots=cLL0yFBcbv&dq=%22mean%20work%20to%20failure%22%20reliability&pg=PA274#v=onepage&q=%22mean%20work%20to%20failure%22&f=false)

MWTF increases shown in results of radiation tests:

- [HiFive1](https://www.sifive.com/boards/hifive1): 2.0x - 35.9x
- [PYNQ-Z1](https://store.digilentinc.com/pynq-z1-python-productivity-for-zynq-7000-arm-fpga-soc/):
  - MxM configurations: 1.2x - 10.0x
  - Various benchmarks: 2.5x - 53.9x

See the [Publications](#publications) below for more information.

### Qemu fork (work)

A fork of Qemu to do cache emulation.  _Currently under development_

[https://github.com/byuccl/qemu](https://github.com/byuccl/qemu)

### Self-driving cars (school)

Created a self-driving car platform from scratch for a graduate engineering course.  Used Nvidia Jetson Nano, Intel RealSense camera, OpenCV, and lots of Python.

[![BYU Self-driving cars](http://img.youtube.com/vi/KvFrLZTMihI/0.jpg)](http://www.youtube.com/watch?v=KvFrLZTMihI)

### Christmas Tree Lights (fun)

Code for controlling NeoPixel strands of lights, as well as a neat little web interface for setting up lighting routines.  An annual project.

[https://github.com/james-ben/christmas-lights](https://github.com/james-ben/christmas-lights)

### Miscellany

A collection of various scripts which are probably useful

[https://github.com/james-ben/miscellany](https://github.com/james-ben/miscellany)



# Education

### BS, Computer Engineering - Brigham Young University

- GPA: 3.83
- Computer Science Minor
- Graduated April 2019
- GRE Oct 2018:
  - Verbal Reasoning: 167
  - Quantitative Reasoning: 164
  - Analytical Writing: 5

### MS, Computer Engineering - Brigham Young University

- Expanding the coverage of [COAST](https://github.com/byuccl/coast) to include [FreeRTOS](https://www.freertos.org/), a common Real-Time Operating System.
- Expected Graduation: April 2021


# Publications

M. Bohman, B. James, M. J. Wirthlin, H. Quinn and J. Goeders, "[Microcontroller Compiler-Assisted Software Fault Tolerance](https://ieeexplore.ieee.org/document/8571250)," in IEEE Transactions on Nuclear Science, vol. 66, no. 1, pp. 223-232, Jan. 2019.  
[DOI: 10.1109/TNS.2018.2886094](https://doi.org/10.1109/TNS.2018.2886094)

Abstract:
> Commercial off-the-shelf microcontrollers can be useful for noncritical processing on spaceborne platforms. These microprocessors can be inexpensive and consume small amounts of power. However, the software running on these processors is vulnerable to radiation upsets. In this paper, we present a fully automated, configurable, software-based tool to increase the reliability of microprocessors in high-radiation environments. This tool consists of a set of open-source LLVM compiler passes to automatically implement software-based mitigation techniques. We duplicate or triplicate computations and insert voting mechanisms into software during the compilation process, allowing for runtime error correction. While the techniques we implement are not novel, previous work has typically been closed source, processor architecture dependent, not automated, and not tested in real high-radiation environments. In contrast, the compiler passes presented in this paper are publicly available, highly customizable, and are platform independent and language independent. We have tested our modified software using both fault injection and through neutron beam radiation on a Texas Instruments MSP430 microcontroller. When tested by a neutron beam, we were able to decrease the cross section of programs by 17-29x, increasing mean-work-to-failure by 4-7x.

B. James, H. Quinn, M. Wirthlin and J. Goeders, "[Applying Compiler-Automated Software Fault Tolerance to Multiple Processor Platforms](https://ieeexplore.ieee.org/document/8933038)," in IEEE Transactions on Nuclear Science, vol. 67, no. 1, pp. 321-327, Jan. 2020.  
[DOI: 10.1109/TNS.2019.2959975](https://doi.org/10.1109/TNS.2019.2959975)

Abstract:
> Several recent works have explored the feasibility of using commercial off-the-shelf (COTS) processing systems in radiation-prone environments, such as spacecraft. Typically, this approach requires some form of protection to ensure that the software can tolerate radiation upsets without compromising the system. Our recent work, COmpiler Assisted Software fault Tolerance (COAST), provides automated compiler modification of software programs to insert dualor triple-modular redundancy. In this article, we extend COAST to support several new processing platforms, including RISC-V and Xilinx, San Jose, CA, USA, SoC-based products. The automated software protection mechanisms are tested for a variety of configurations, altering the benchmark and cache configuration. Across the different configurations, the cross sections were improved by 4x to 106x. In addition, a hardware-mitigation technique is tested using dual-lock-step cores on the Texas Instruments, Dallas, TX, USA, Hercules platform, which is compared with the software only mitigation approach.


# References

**_Brigham Young University_**  
Professor Jeffrey Goeders  
Computer Engineering Department  
[jgoeders@byu.edu](mailto:jgoeders@byu.edu)

**_Other_**  
Tim Eversole  
Martial Arts Instructor  
[tdeversole@yahoo.com](mailto:tdeversole@yahoo.com)  
801-874-9794
