# Falcon-8 CPU

> **8-bit Single-Cycle Processor** designed from scratch in **Logisim Evolution**.

Falcon-8 is a custom educational CPU built to demonstrate the fundamentals of processor architecture at the digital-logic level, including instruction execution, datapath design, control logic, memory, registers, branching, and status flags.

## Architecture

- 8-bit data width
- 16-bit instruction width
- Single-cycle execution model
- 8 general-purpose registers
- Custom Instruction Set Architecture (ISA)
- Program Counter
- Instruction ROM
- Data RAM
- Control Unit
- Register File
- ALU
- Write-back logic
- Zero and Carry flags

## CPU Specifications

| Specification | Value |
|---|---|
| Data Width | 8-bit |
| Instruction Width | 16-bit |
| Registers | 8 general-purpose registers |
| Architecture | Single-Cycle |
| Instruction Memory | ROM 256 × 16 |
| Data Memory | RAM 256 × 8 |
| Implementation | Logisim Evolution |

## Instruction Format

```text
15          11 10      8 7      5 4       0
+-------------+---------+---------+---------+
|   Opcode    |   RD    |   RS    |Immediate|
+-------------+---------+---------+---------+
```

## Instruction Set

### Arithmetic & Logic

- `ADD`
- `SUB`
- `AND`
- `OR`
- `XOR`
- `NOT`

### Memory

- `LOAD`
- `STORE`

### Data Transfer

- `MOV`
- `LDI`

### Control Flow

- `JMP`
- `JZ`
- `JNZ`
- `JC`
- `HLT`

## Processor Architecture

```text
              ┌─────────────────┐
              │ Instruction ROM │
              └────────┬────────┘
                       ▼
                ┌──────────────┐
                │ Control Unit │
                └──────┬───────┘
                       │
        ┌──────────────┼──────────────┐
        ▼              ▼              ▼
  ┌──────────┐   ┌──────────┐   ┌─────────┐
  │ Register │──▶│   ALU    │──▶│  RAM    │
  │   File   │   └──────────┘   └─────────┘
  └──────────┘
        ▲
        │
  ┌─────┴─────┐
  │     PC    │
  └───────────┘
```

## Project Structure

```text
Falcon-8-CPU/
├── docs/
├── images/
├── logisim/
├── tests/
├── LICENSE
└── README.md
```

## Screenshots

### Main CPU
![Falcon-8 Main CPU](images/Main.png)

### ALU
![Falcon-8 ALU](images/ALU.png)

### Register File
![Falcon-8 Register File](images/Register.png)

### Program Counter
![Falcon-8 Program Counter](images/PC.png)

## Engineering Scope

Falcon-8 was developed as a hands-on computer architecture project to understand how a processor is assembled from digital building blocks and how a custom ISA maps to datapath and control signals.

## Future Improvements

- Pipeline architecture
- Stack pointer
- `CALL` / `RET` instructions
- Interrupt handling
- Cache memory
- Performance analysis and optimization

## Author

**Abdullah Almutairi**  
Electrical & Computer Engineering Student · King Abdulaziz University

## License

MIT License
