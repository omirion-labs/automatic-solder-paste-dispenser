# Overview

---

- [Overview](#overview)
  - [Software Architecture](#software-architecture)

<a name="overview"></a>
## [Software Architecture](#software-arch)

---

![image](../../../imgs/software_architecture.png)

* Hardware : the board that contains the microcontroller.
* HAL (Hardware Abstraction Layer) : control and drive low level registers (microcontroller level).
* BSP (Board Support Package) : manage peripheral components connected to the microcontroller.
* Third-Party : FreeRTOS in our case which is an embedded operating system.
* Application Layer : the application code.