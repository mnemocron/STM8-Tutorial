# STM8 Tutorial 000 - Intro

Embedded Software Programming on the STM8 Plattform

---

## Getting Started

In this first chapter I will give a brief introduction on how to get started with programming STM8 microcontrollers. I will point out sources of information and I will show how to use this information for your daily programming work.

---

### Development Environment

#### STM8CubeMX

Unlike the STM32CubeMX, the STM8CubeMX **does not generate initialization code** or a project folder. Its sole purpuse is to help you design a hardware board and choose the correct pinout.

- **[STM8CubeMX Download](https://www.st.com/en/development-tools/stm8cubemx.html)**
- User Manual STM8CubeMX **[UM2125](https://www.st.com/resource/en/user_manual/dm00336190.pdf)** (pdf)

#### ST Visual Develop (STVD)

STVD is STMicroelectronics recommended IDE. 
I do not recommend this IDE because the associated compiler option (Cosmic) is very old (C89 standard). However, the STVD comes with another program called ST Visual Program which is similar to the ST-Link Utility. It can be used to read/write the STM8 chips.

- **[STVD Download](https://www.st.com/en/development-tools/stvd-stm8.html)**
- User Manual ST Visual Develop **[UM0036](https://www.st.com/resource/en/user_manual/cd00004556-st-visual-develop-stvd--stmicroelectronics.pdf)** (pdf)

In order for the IDE to compile C-programs, you need a third party compiler.

- Register for the FREE stm8 Compiler: [cosmicsoftware.com](https://www.cosmicsoftware.com/download_stm8_free.php)

The Cosmic compiler requires a license for the free version. You have to request the license per e-mail (!?). (what a miracle that they don't also send you the license code on a postcard)

#### **IAR Embedded Workbench**

I recommend this IDE because it is state of the art and works very quickly out of the box. There are two evaluation license options available:

- full featured product for 30 days
- unlimmited license with `8kB` code size limitation

If you only plan to create small software for your STM8, the 2nd option is best.

- Download from [iar.com](https://www.iar.com/iar-embedded-workbench/#!?architecture=STM8)

During the installation you are prompted to enter your personal information. Enter your e-mail for the license key. Make something up for the other fields if you like (Name: Bruce Wayne / Address: Wayne Manor / City: Gotham ...)

---

### Hardware Documentation (Datasheet / User Manuals)

- **[PM0044](https://www.st.com/resource/en/programming_manual/cd00161709-stm8-cpu-programming-manual-stmicroelectronics.pdf)** STM8 CPU Programming Manual  (pdf) (162 pages)
- **[PM0047](https://d1.amobbs.com/bbs_upload782111/files_11/ourdev_439350.pdf)** STM8 Flash programming  (pdf)
- **[RM0016](https://www.st.com/resource/en/reference_manual/cd00190271-stm8s-series-and-stm8af-series-8bit-microcontrollers-stmicroelectronics.pdf)** STM8S / STM8AL Reference Manual (pdf) (467 pages)
- **[RM0031](https://www.st.com/resource/en/reference_manual/cd00218714-stm8l050j3-stm8l051f3-stm8l052c6-stm8l052r8-mcus-and-stm8l151l152-stm8l162-stm8al31-stm8al3l-lines-stmicroelectronics.pdf)** STM8L / STM8AL Reference Manual (pdf) (597 pages)
- MASTM8 Raisonance ST7/STM8 Assembler Manual (pdf) (87 pages) `ftp://raisonance.com/pub/Support/RKit-STM8/MASTM8.pdf` 

#### Reference Designs (Discovery Boards)

- [UM0817](https://www.st.com/resource/en/user_manual/cd00250600-stm8s-discovery-stmicroelectronics.pdf) STM8S-DISCOVERY
- [UM0970](https://www.st.com/resource/en/user_manual/cd00278045-stm8ldiscovery-stmicroelectronics.pdf) STM8L-DISCOVERY
- [UM2339](https://www.st.com/resource/en/user_manual/dm00462805-discovery-kit-with-stm8s001j3m3-stm8l001j3m3-and-stm8l050j3m3-mcus-stmicroelectronics.pdf) STM8-SO8-DISCO

---

### IDE and Tools Documentation

- **[UM0036](https://www.st.com/resource/en/user_manual/cd00004556-st-visual-develop-stvd--stmicroelectronics.pdf)** User Manual ST Visual Develop (pdf)
- **[User Guides](https://www.iar.com/support/user-guides/user-guides-iar-embedded-workbench-for-stmicroelectronics-stm8/)**: IAR Embedded Workbench for STM8

---

### Standard Peripheral Libraries (SPL) (HAL)

Because there is no code generator tool, you have to download and copy your own project. Luckily STMicroelectronics provides a peripheral library for the STM8 devices. It works similar to the hardware abstraction libraries (HAL) used in the STM32 ecosystem.

Unfortunately the coding style (upper/lower case) between the SPL packages differs sometimes, which makes the code not easily portable. (e.g. using `GPIO_PIN_5` in STM8S and `GPIO_Pin_5` in STM8L).

- Product Selector: [STM8 Embedded Software](https://www.st.com/en/embedded-software/stm8-embedded-software.html#products)
- **[STSW-STM8016](https://www.st.com/en/embedded-software/stsw-stm8016.html)** for STM8L15x/16x/05x/AL3Lx/AL31x
- **[STSW-STM8069](https://www.st.com/en/embedded-software/stsw-stm8069.html)** for STM8S/A

The SPL files also feature many many examples implementing every hardware function on the STM9 device. You can always look there and copy initialization code etc. from these example files.

---

### External Tutorials

- [embedded-lab.com](http://embedded-lab.com/blog/starting-stm8-microcontrollers/) (extensive introduction using STVD and Cosmic)





