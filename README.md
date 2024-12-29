## Introduction
The Pressure Detection System is an embedded application designed to detect pressure levels and trigger an alarm if the pressure exceeds a predefined threshold. This project focuses on:
- Building an embedded system process using the ARM `arm-none-eabi` toolchain directly through the terminal.
- Utilizing binary utilities for ELF file analysis.
- Exploring system architecture, from requirements to design and implementation.
- Leveraging UML diagrams for system visualization and alignment among stakeholders.

The system's primary purpose is simplicity to serve as a learning platform for embedded systems concepts, toolchain usage, and system design.

## Table of Contents
1. [Introduction](#introduction)
2. [Features](#features)
3. [System Design](#system-design)
   - [UML Diagrams](#uml-diagrams)
4. [Source files](#source-files)
5. [Installation](#installation)
   - [Prerequisites](#prerequisites)
   - [Steps](#steps)
6. [Examples](#examples)
   - [Sample Scenario](#sample-scenario)
7. [Troubleshooting](#troubleshooting)
8. [Contributors](#contributors)
9. [License](#license)

## Features
- Real-time pressure monitoring.
- Alarm signaling when pressure exceeds the threshold.
- Modular system architecture:
  - State machine-based logic.
  - Interfaces for easy integration.
- Embedded C implementation for STM32 microcontrollers.
- Build process including:
  - Custom startup code.
  - Linker script and Makefile integration.
  - ELF file analysis and binary utilities.

## System Design
The system development followed a structured approach:
1. **Requirement Analysis**:
   - Defined through a Requirement Diagram.
2. **System Analysis**:
   - Captured using Use Case, Activity, and Sequence Diagrams.
3. **System Design**:
   - Block Diagram detailing the modular structure.
   - State Machines for each block.

### UML Diagrams
The project utilized UML diagrams to align team understanding and streamline development:
- **Requirement Diagram**: Defines high-level goals. ![RequirementsDiagram](https://github.com/user-attachments/assets/cb6d0e8b-46ba-420c-9863-c709d354072c)

- **Use Case Diagram**: Illustrates actor interactions. ![UseCaseDiagram](https://github.com/user-attachments/assets/9aa87f1c-7d12-42e2-9026-6c285fccd81b)

- **Activity Diagram**: Maps process flow. ![ActivityDiagram](https://github.com/user-attachments/assets/cdd942e0-ec73-472e-8aeb-95ed63caa745)

- **Sequence Diagram**: Describes interactions among components. ![SequanceDiagram](https://github.com/user-attachments/assets/81e1bf6b-ba28-48ec-8268-79986e39c40f)

- **Block Diagram and State Machines**: Detail architectural design and component behavior.
  ![BlockDiagram](https://github.com/user-attachments/assets/574cea5d-35a5-47a4-afec-9bf05f43c5e9)
  ![HighPressureDetectionSM](https://github.com/user-attachments/assets/d81ff5c1-0375-41d3-97b8-b32d39dfaca5)
  ![AlarmMechanismSM](https://github.com/user-attachments/assets/e2bb94c1-8252-484a-81be-e5c92cc11b59) 

## Source Files
- `main.c`: Entry point of the application.
- `HighPressureDetection.c`: Contain the states of the high pressure detection module.
- `AlarmMechanism.c`: Contain the states of the alarm signaling logic module.
- `StateMachine.h`: Header file for declaring and defining state machines and transitions.
- `startup.s`: Custom startup code for STM32.
- `linker_script.ld`: Custom linker script defines memory layout for the application.
- `Makefile`: Custom Make file Automates build and cleaning process.

## Installation

### Prerequisites
- ARM `arm-none-eabi` toolchain.
- STM32 development board or Proteus simulator.

### Steps

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Mohamed-Hamdy-MA/Pressure-Detection-System.git
   ```

2. **Navigate to the project directory:**
   ```bash
   cd Pressure-Detection-System
   ```

3. **Build the project using the provided Makefile:**
   ```bash
   make build
   ```

## Examples

### Sample Scenario
1. Set pressure input in Proteus (PA0:PA7).
2. Observe alarm activation when pressure exceeds the threshold (PA13).
3. Verify state transitions using debug GPIO LEDs.

## Troubleshooting

- **Issue:** Alarm not triggering.  
  **Solution:** Verify pressure value acquisition (`getPressureVal`).

- **Issue:** Build failure.  
  **Solution:** Ensure `arm-none-eabi-gcc` is correctly installed.

## Contributors

- **Mohamed Hamdy** - Auther and Developer.
- **Learn In Depth** - Provider of driver.c, driver.h and Protues project.

## License

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.
