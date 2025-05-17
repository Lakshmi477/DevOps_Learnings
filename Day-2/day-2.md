# 🖥️ Virtual Machine

There are a lot of servers we have created, but we haven't used 100% of CPU and RAM.  
Here, a lot of data is wasted, so this is called **inefficiency**.

With the concept of **virtualization**, we install a **hypervisor**.

- **Hypervisor** is a software that can be installed on a physical machine.
- Here we can do **logical isolation**.
- We add **efficiency** using the hypervisor by logically separating resources.
- There is **no dependency** between all VMs — every VM has its own CPU, RAM, and all other components.

---

# 🐧 LINUX OS

**Operating System** means it is the **bridge between software and hardware components**.

### Example:

When we use a program (browser or any app), it doesn't talk to hardware components like CPU, memory, or disk directly.  
Instead, it uses the **Operating System (OS)**.


---

## 🔧 Key components between software and hardware:

### ✅ System Software
- Software that runs the system and helps work with hardware (e.g., **libraries**, **drivers**)

### ✅ User Process
- A program started by the user (e.g., **Chrome**, **a Python script**, etc.)

### ✅ System Libraries

- Ready-made code that both apps and the OS can use (e.g., **math functions**, **file handling**)
- System libraries are responsible for performing tasks like calculations, file handling, etc., so that applications don't have to write those from scratch.


### ✅ Kernel
- This is the **main part of the OS** that talks to hardware and controls everything.
- Kernel is responsible for communication between software and hardware.

#### Kernel Responsibilities:
- Device Management  
- Memory Management  
- Process Management  
- Handling Management  

### ✅ OS
- Software that **manages hardware** and lets applications run.

---

## 🔄 System Architecture

[User Process / App]
↓
[System Libraries]
↓
[Operating System]
↳ Shell / UI (what you see)
↳ Kernel (core manager)
↳ Drivers (to talk to devices)
↓
[Hardware]
