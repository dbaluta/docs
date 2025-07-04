# Day 3 – [Lab Title Here]

Slides: [day3_slides](./day3_slides)

## Description

_Provide a short description of what this lab session is about. Mention the scope and practical goals
for the day, what students are expected to understand or achieve by the end of this lab._

---

## Topics Covered

- _List bullet points summarizing key technical concepts introduced during this session._
- _These can include kernel mechanisms, APIs, interfaces, or subsystems discussed._
- _Use this as a quick reference or learning summary._

---

## Lab Exercises

> **Note**
>
> Before starting this lab, make sure your **exercises repository** is up to date. All lab exercises are
> located in subdirectories under `drivers/lkss/lab3`.
>
>
> ### If You Already Have the Repository
>
> If you are using the virtual machine described in [Infrastructure page](./infrastructure.md) the repo is already
cloned. 
>
> ```bash
> cd ~/linux  # or navigate to the location where you cloned the repo
> git pull origin main
> ```
>
> Make sure you are on the correct branch (that is `main` branch).
>
> ### If You Do Not Have the Repository Yet
>
> If you haven't cloned the repository yet, you can do so with the following commands:
>
> ```bash
> git clone https://github.com/Linux-Kernel-Summer-School/linux.git
> cd linux
> ```
>
> Navigate to `drivers/lkss/labs/lab3/` lab directory to begin your work.
>
> ---

### Exercise 1: Writing a Simple GPIO Button Driver

In this exercise, you'll explore a basic GPIO button driver that registers an interrupt handler
when the button is pressed. This example demonstrates how to use GPIO descriptors and platform
drivers in the Linux kernel.

1. **Understand the Driver Structure**
   Explore the code under `drivers/lkss/labs/lab3/gpio_button.c`. This driver requests a GPIO line,
   converts it to an IRQ, and sets up an interrupt handler triggered on a falling edge.
   Read through `gpio_button.c` and identify the following:
    - How the GPIO is retrieved using `devm_gpiod_get()`
    - How the GPIO is mapped to an IRQ using `gpiod_to_irq()`
    - How the interrupt is requested with `devm_request_irq()`
    - Where and how the interrupt handler is defined.
  Pay special attention to the `button_irq_handler()` function. You'll implement functionality in it.

---

### Exercise 2: [Exercise Title]

_Goal: Explain the purpose of the second exercise if applicable._

---

### Exercise 3: [Optional Exercise Title]

_Goal: Additional or challenge-level task to deepen understanding._

---

## Resources

- _Provide links to slides, Linux kernel documentation, relevant source files, headers, or external
  guides._
- _Add any notes about kernel versions, dependencies, or hardware setup._
