# Digital Design & Verification Projects

![SystemVerilog](https://img.shields.io/badge/Language-SystemVerilog-blue)
![EDA Playground](https://img.shields.io/badge/Simulator-Xcelium-green)
![Verification](https://img.shields.io/badge/Focus-Functional%20Verification-orange)

A collection of **Digital Design Verification Projects** implemented using **SystemVerilog**, **Object-Oriented Testbench Architecture**, and **Constrained Random Verification**.

This repository contains verification environments for industry-standard protocols, memory systems, and sequential logic circuits.

---

# Repository Structure

```bash
.
├── APB/
├── I2C/
├── SPI/
├── UART/
├── Verification of DFF/
├── Verification of FIFO/
└── Wishbone Memory/
```

---

# Projects

<details>
<summary><b>1. Verification of FIFO</b></summary>

### Features
- Synchronous FIFO verification
- Generator-Driver-Monitor-Scoreboard architecture
- Mailbox communication
- Virtual Interface
- Randomized read/write operations

### Verified Parameters
- Full condition
- Empty condition
- Data integrity
- Pointer operations

</details>

---

<details>
<summary><b>2. Verification of DFF</b></summary>

### Features
- D Flip-Flop functional verification
- Reset behavior verification
- Clock edge verification

### Verified Parameters
- Setup of input data
- Positive edge triggering
- Reset functionality

</details>

---

<details>
<summary><b>3. UART</b></summary>

### Features
- UART protocol verification
- Serial transmission/reception
- Start/Stop bit validation

### Verified Parameters
- Baud synchronization
- Frame integrity
- TX/RX correctness

</details>

---

<details>
<summary><b>4. SPI</b></summary>

### Features
- SPI protocol verification
- Master-slave communication
- Clock polarity/phase testing

### Verified Parameters
- MOSI/MISO transfer
- Chip select functionality
- Clock synchronization

</details>

---

<details>
<summary><b>5. I2C</b></summary>

### Features
- I2C protocol verification
- Start/Stop condition checking
- ACK/NACK verification

### Verified Parameters
- SDA/SCL timing
- Address transmission
- Data transfer correctness

</details>

---

<details>
<summary><b>6. APB</b></summary>

### Features
- AMBA APB bus verification
- Read/write transaction checking
- Slave response validation

### Verified Parameters
- Address phase
- Enable phase
- Data integrity

</details>

---

<details>
<summary><b>7. Wishbone Memory</b></summary>

### Features
- Wishbone bus verification
- Memory read/write operations
- Bus handshake verification

### Verified Parameters
- ACK generation
- Address decoding
- Memory consistency

</details>

---

# Common Verification Architecture

All projects follow a layered verification architecture:

```text
Generator → Driver → DUT → Monitor → Scoreboard
```

---

# Common Generated Simulation Files

After running simulations in **EDA Playground (Cadence Xcelium)**, each project generates:

```bash
.simvision/                # Waveform database
xcelium.d/                 # Simulator working directory
work/                      # Compiled library

design.sv                  # DUT design file
testbench.sv               # Testbench file

dump.vcd                   # Waveform dump
dump.tcl                   # TCL script

run.sh                     # Simulation script
xrun                       # Xcelium executable output
xrun.history               # Simulation history

specman                    # Simulator support file
cds                        # Cadence support file

.bashrc
.bash_profile
.bash_logout
```

---

# Running Simulations

## On EDA Playground

1. Open EDA Playground
2. Select:

```text
Language: SystemVerilog
Simulator: Cadence Xcelium
```

3. Upload or paste:
- `design.sv`
- `testbench.sv`

4. Click **Run**

---

# Waveform Analysis

Simulation generates:

```bash
dump.vcd
```

This can be viewed using:

- GTKWave
- Cadence SimVision

---

# Verification Methodologies Used

This repository demonstrates:

✅ Object-Oriented Verification  
✅ Constrained Random Verification  
✅ Mailbox Communication  
✅ Event Synchronization  
✅ Transaction Modeling  
✅ Scoreboard-Based Checking  
✅ Self-Checking Testbench  

---

# Future Improvements

Planned upgrades:

- Functional Coverage
- Assertions (SVA)
- Coverage Driven Verification
- UVM Migration

---


