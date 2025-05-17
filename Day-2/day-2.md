
---

## 🔧 Key Components Between Software and Hardware

### 1. System Software
- Software that runs the system and helps work with hardware.
- Examples: **Libraries**, **Drivers**, **Shell**

### 2. User Process
- A program started by the user.
- Examples: **Chrome**, **Python Script**, etc.

### 3. System Libraries
- Ready-made code that both apps and OS can use.
- System libraries are responsible for performing tasks like calculations, file handling, etc., so that applications don't have to write those from scratch.
- Examples: **Math functions**, **file access code**, etc.

### 4. Kernel
- **Core part** of the OS that talks to hardware.
- Manages and controls everything.

#### Kernel Responsibilities:
- **Device Management**
- **Memory Management**
- **Process Management**
- **Interrupt Handling**

### 5. Operating System (OS)
- Software that **manages hardware** and **lets applications run**.
- Examples: **Linux**, **Windows**, **macOS**

---

## 🔄 Flow of Communication

[User Process / App]
↓
[System Libraries]
↓
[Operating System]
├─ Shell / UI (User Interface)
├─ Kernel (Core Manager)
└─ Drivers (Device Communication)
↓
[Hardware (CPU, RAM, Disk, etc.)]
