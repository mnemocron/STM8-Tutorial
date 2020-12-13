# STM8-Tutorial
Getting started with the STM8 HAL development environment. Tutorial documents in Markdown. 

---

### 000 - Resources

Here you find links and hints to important documents like datasheets and user manuals for the STM8 series as well as the available compilers.


### 001 - Project Template

Start a project in the IAR Emebdded Workbench. Copy the necessary files and change the necessary settings.

---

After these two tutorials, you should know, how to build your own project from the templates and resource files provided by the manufacturers.

---

### 8-Bit is not dead!

Why use an 8 bit MCU anyways, if there are powerful STM32 microtontrollers available?

> Sometimes they simply are the more cost efficient solution.

Example:

> I worked on a project which used an analog comparator circuit to toggle an LED with a threshold and hysteresis (charging status LED).
> It turns out that the comparator and the 1% resistors (~ $0.10/pc.) necessary for the voltage threshold cost more than a single STM8S MCU (< $0.40).
> The STM8S offers internal ADCs which solves the problem of the voltage threshold and hysteresis. And you save on a couple of resistors.











