# 4-Bit Binary to Gray Code Converter – Verilog

## Description

A **4-bit Binary to Gray Code Converter** designed using Verilog HDL. The circuit converts a 4-bit binary number into its corresponding Gray Code using XOR logic.

## Features

* 4-bit binary input
* 4-bit Gray Code output
* Combinational logic design
* Simple XOR-based implementation
* Verilog testbench included
* Complete input verification from `0000` to `1111`

## Folder Structure

```text
Binary-to-Gray-Code-Verilog/
│
├── src/
│   └── binary_to_gray.v
│
├── tb/
│   └── binary_to_gray_tb.v
│
├── output/
│   └── output.txt
│
└── README.md
```

## Inputs

| Signal   | Width | Description  |
| -------- | ----: | ------------ |
| `binary` | 4-bit | Binary input |

## Output

| Signal | Width | Description      |
| ------ | ----: | ---------------- |
| `gray` | 4-bit | Gray Code output |

## Conversion Logic

For a 4-bit binary input:

```text
Gray[3] = Binary[3]
Gray[2] = Binary[3] XOR Binary[2]
Gray[1] = Binary[2] XOR Binary[1]
Gray[0] = Binary[1] XOR Binary[0]
```

## Truth Table

| Binary | Gray   |
| ------ | ------ |
| `0000` | `0000` |
| `0001` | `0001` |
| `0010` | `0011` |
| `0011` | `0010` |
| `0100` | `0110` |
| `0101` | `0111` |
| `0110` | `0101` |
| `0111` | `0100` |
| `1000` | `1100` |
| `1001` | `1101` |
| `1010` | `1111` |
| `1011` | `1110` |
| `1100` | `1010` |
| `1101` | `1011` |
| `1110` | `1001` |
| `1111` | `1000` |

## Working Principle

Gray Code is a binary numeral system in which two consecutive values differ by only one bit.

The converter uses XOR gates to generate the Gray Code from the binary input.

Example:

```text
Binary = 1011

Gray[3] = 1
Gray[2] = 1 XOR 0 = 1
Gray[1] = 0 XOR 1 = 1
Gray[0] = 1 XOR 1 = 0

Gray = 1110
```

## Simulation

This project can be simulated using **Icarus Verilog**.

### Compile

```bash
iverilog -o binary_gray_sim src/binary_to_gray.v tb/binary_to_gray_tb.v
```

### Run

```bash
vvp binary_gray_sim
```

### Save Output

```bash
vvp binary_gray_sim > output/output.txt
```

## Expected Output

The testbench verifies all 16 possible 4-bit binary inputs and displays their corresponding Gray Code values.

## Learning Outcomes

This project demonstrates:

* Combinational logic
* XOR gates
* Binary-to-Gray conversion
* Verilog continuous assignment
* Testbench development
* Truth-table verification
* Simulation using Icarus Verilog

## Future Improvements

The project can be extended to:

* 8-bit Binary to Gray converter
* Gray to Binary converter
* Parameterized Binary-to-Gray converter
* FPGA implementation
* Seven-segment display interface

## Author

**Nikhila**

## License

This project is created for educational and learning purposes.
