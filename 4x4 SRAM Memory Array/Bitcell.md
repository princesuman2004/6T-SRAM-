

# SRAM Bitcell

## Overview

This document provides an overview of the SRAM bitcell, including its schematic design, read and write operations, and noise margin analysis. An SRAM bitcell is a fundamental building block of static random-access memory (SRAM), used to store a single bit of data.

## Schematic Design

The SRAM bitcell typically consists of six transistors (6T) arranged in a cross-coupled configuration. The basic components are:

- **Two PMOS Transistors** (for storage)
- **Four NMOS Transistors** (for access and cross-coupling)

### Schematic Representation

 ![image](https://github.com/user-attachments/assets/20a7c2d9-0a7a-4bbb-a8d6-86130ac6bc49)



## Read Operation

1. **Activate Read Access:**
   - The read access transistor (NMOS1) is turned on by applying a read signal to its gate.
   - The bitline (BL) is precharged to a high voltage.

2. **Read Out Data:**
   - The stored data is accessed through the bitline.
   - The voltage difference on the bitline is sensed and amplified by sense amplifiers connected to the bitline.

3. **Result:**
   - The voltage on the bitline changes based on the stored data (high or low).
  
     ![image](https://github.com/user-attachments/assets/456c862e-ac04-4c78-b8b2-21dfcd05c321)


## Write Operation

1. **Activate Write Access:**
   - The write access transistor (NMOS2) is turned on by applying a write signal to its gate.

2. **Apply Data:**
   - The bitline (BL) is driven to the desired logic level (high or low) to write data into the cell.

3. **Store Data:**
   - The data is stored in the SRAM cell as the voltage levels on the storage nodes are updated.

## Noise Margin Analysis

### Read Noise Margin

- **Definition:** The ability of the SRAM cell to withstand small disturbances during read operations.
- **Measurement:** Determine the minimum voltage difference required to reliably sense the stored data.
- **Typical Values:** Read noise margin is usually measured as the difference between the stable and unstable states of the cell.

### Write Noise Margin

- **Definition:** The ability of the SRAM cell to resist disturbances during write operations.
- **Measurement:** Determine the voltage margin required to reliably write a new value into the cell without causing a disturbance.
- **Typical Values:** Write noise margin is typically measured as the difference between the voltage levels required to overwrite the stored value.

## Results

- **Read Noise Margin:** Provides the reliability of data reading. A higher margin indicates better stability during read operations.
- **Write Noise Margin:** Ensures that the cell can be reliably written to without affecting the stored value. A higher margin indicates better resistance to write disturbances.

  ![image](https://github.com/user-attachments/assets/94576b10-1f29-4b1b-9d47-b776d86ccca9)


### Example Results

- **Read Noise Margin:** 0.2 V (indicating reliable read operations)
- **Write Noise Margin:** 0.3 V (indicating reliable write operations)


