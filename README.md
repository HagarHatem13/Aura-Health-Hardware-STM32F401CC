Aura Health — Embedded Hardware

This repository contains the **embedded firmware** for the Aura Health Monitoring System.

The firmware is responsible for reading data from the health-monitoring sensors, processing the measurements, and preparing the data for wireless transmission to the Aura Health web application.

🛠️ Development Environment

The embedded project is developed using:

* **Eclipse IDE**
* **C**
* **ARM Microcontroller**
* **GCC ARM Toolchain**
* Embedded peripheral drivers

 📁 Project Structure

The repository contains the main source and header files:

```text
Aura-Health-Hardware/
│
├── include/
│   ├── ...
│   └── ...
│
├── src/
│   ├── ...
│   └── ...
│
└── README.md
```

`include/`

Contains the project's header files (`.h`), including:

* Driver interfaces
* Configuration files
* Type definitions
* Peripheral definitions
* Module interfaces

 `src/`

Contains the C source files (`.c`) implementing:

* Drivers
* Hardware initialization
* Sensor communication
* Application logic
* Peripheral handling

---

 🚀 How to Open the Hardware Project

 1. Install Eclipse

Install an Eclipse version suitable for embedded C/C++ development and make sure the required ARM GCC toolchain is available.

 2. Create a New Eclipse Project

Open Eclipse.

Go to:

**File → New → C/C++ Project**

Create a new embedded C project using the appropriate toolchain and microcontroller configuration.

Give the project a name such as:

```text
Aura-Health-Hardware
```

Configure the project according to the target microcontroller used by the hardware.

---

 3. Add the `include` Folder

After creating the Eclipse project:

1. Copy the `include` folder from this repository.
2. Place it inside the Eclipse project directory.
3. In Eclipse, right-click the project.
4. Select:

**Refresh**

The `include` folder should now appear in the project.

Make sure Eclipse knows that this directory contains header files.

Go to:

**Project → Properties → C/C++ Build → Settings**

Then add the `include` directory to the compiler's **Include Paths**.

---

 4. Add the `src` Folder

Copy the `src` folder from this repository into the Eclipse project directory.

Then:

1. Refresh the Eclipse project.
2. Make sure all `.c` files appear under `src`.
3. Make sure Eclipse includes them in the build.

The project should now contain:

```text
Aura-Health-Hardware
│
├── include
│   ├── Driver1.h
│   ├── Driver2.h
│   └── ...
│
├── src
│   ├── Driver1.c
│   ├── Driver2.c
│   ├── main.c
│   └── ...
│
└── README.md
```

---

 ⚙️ Project Configuration

Before building the project, configure:

* Target microcontroller
* CPU frequency
* Compiler
* Linker
* Startup files
* Memory configuration
* Include paths
* Preprocessor definitions
* Debug configuration

The exact configuration depends on the microcontroller and development board being used.

---

🔨 Build the Project

After adding the `include` and `src` folders:

In Eclipse select:

**Project → Build Project**

or use:

```text
Ctrl + B
```

Make sure there are no compilation errors.

---

🔌 Hardware Connection

The embedded system is designed around the following architecture:

```text
Heart Rate Sensor
        ↓
Microcontroller
        ↓
Data Processing
        ↓
Wireless Communication
        ↓
Aura Health Website
```

The microcontroller collects the sensor data, processes it, and sends the required information through the wireless communication module.

---

 📡 Wireless Communication

The firmware is designed to support communication between the embedded device and the web application.

Depending on the final hardware implementation, communication can be performed using technologies such as:

* Bluetooth / BLE
* Wi-Fi
* UART-connected wireless module
* Other supported wireless communication modules

The communication layer should provide the web application with the required monitoring data.

---

 📊 Main Hardware Responsibilities

The firmware is responsible for:

* Initializing the microcontroller
* Initializing required peripherals
* Communicating with the heart-rate sensor
* Reading sensor measurements
* Processing measurements
* Determining the current monitoring zone
* Managing wireless communication
* Sending monitoring data
* Handling hardware errors

---

 🧩 Important

The `include` and `src` folders in this repository contain the project's source code.

When setting up the project in Eclipse, **do not modify the source files unnecessarily**.

Configure the Eclipse project around the provided source code and make sure the correct:

* Microcontroller
* Toolchain
* Include paths
* Startup files
* Linker configuration

are selected.

---

▶️ Quick Setup

For a quick setup:

```text
1. Open Eclipse
        ↓
2. Create a new embedded C project
        ↓
3. Select the correct microcontroller/toolchain
        ↓
4. Copy `include/` into the project
        ↓
5. Copy `src/` into the project
        ↓
6. Add `include/` to the compiler Include Paths
        ↓
7. Refresh Eclipse
        ↓
8. Build Project
        ↓
9. Flash the firmware to the microcontroller
```

---

 🔗 Complete Aura Health System

The complete project consists of:

```text
                 AURA HEALTH
                      │
        ┌─────────────┴─────────────┐
        │                           │
   HARDWARE                    WEB APPLICATION
        │                           │
Heart Rate Sensor              Dashboard
        ↓                       Analytics
Microcontroller                  History
        ↓                       Relaxation
Wireless Module                  Insights
        │                           │
        └──────── Wireless ─────────┘
```

The hardware repository contains the **embedded firmware**, while the web repository contains the **Aura Health monitoring interface**.
