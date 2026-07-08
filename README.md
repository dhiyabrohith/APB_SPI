# APB_SPI
## Protocols Used

### [APB (Advanced Peripheral Bus)]

APB is part of ARM’s AMBA bus family and is used for connecting low-bandwidth peripherals like SPI, UART, GPIO, and timers.

### Key Features

- Simple request–response protocol
- Non-pipelined communication
- Low power and low area design
- Single transfer at a time

## Important APB Signals

| Signal | Direction | Description |
|---------|----------|-------------|
| PADDR | Master → Slave | Address bus |
| PWRITE | Master → Slave | Read/Write control |
| PSEL | Master → Slave | Peripheral select |
| PENABLE | Master → Slave | Access phase indicator |
| PWDATA | Master → Slave | Write data |
| PRDATA | Slave → Master | Read data |

## SPI (Serial Peripheral Interface)

SPI is a synchronous serial communication protocol used for high-speed data transfer between a master and one or more slave devices.

### Features

- Full duplex communication
- High-speed serial data transfer
- Master-slave architecture
- Configurable clock polarity (CPOL) and clock phase (CPHA)
- Multiple slave support using chip select signals

## Important SPI Signals

| Signal | Direction | Description |
|---------|----------|-------------|
| SCLK | Master → Slave | Serial Clock |
| MOSI | Master → Slave | Master Out Slave In |
| MISO | Slave → Master | Master In Slave Out |
| SS/CS | Master → Slave | Slave Select / Chip Select |

## SPI Registers

| Register | Function |
|-----------|----------|
| SPCR | SPI Control Register |
| SPSR | SPI Status Register |
| SPDR | SPI Data Register |
| SPER | SPI Extension Register |
| BAUD_REG | Baud Rate Configuration Register |
| INT_REG | Interrupt Control Register |

## Test Cases

- APB Write Transaction
- APB Read Transaction
- SPI Master Transmit
- SPI Master Receive
- Full Duplex Communication
- Loopback Mode
- CPOL/CPHA Mode Verification

## Conclusion

The APB-based SPI core was successfully verified using the UVM methodology by validating SPI communication, APB transactions, register functionality, clock generation, interrupt handling, and various protocol scenarios.

A comprehensive verification environment including driver, monitor, scoreboard, functional coverage, assertions, and RAL model was developed to ensure reliable verification of the DUT. Different test scenarios such as full duplex communication, loopback mode, CPOL/CPHA configurations, and APB read/write operations were thoroughly tested.

This project significantly enhanced understanding of:

- APB protocol and SPI architecture
- UVM-based verification flow
- Register Abstraction Layer (RAL)
- Functional coverage concepts
- Assertions and protocol checking
- Debugging and problem-solving methodologies

Overall, the project provided strong practical exposure to industry-standard verification techniques and improved confidence in protocol-level verification and UVM environment development.
