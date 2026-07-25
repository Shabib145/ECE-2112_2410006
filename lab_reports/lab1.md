# Lab 1: Digital Logic Basics

## Experiment 1: OR Gate from NOR Gates

### Aim
Build an OR gate using only NOR gates.

### Theory
A NOR gate gives the opposite of OR:

$$
A \downarrow B = \overline{A+B}
$$

If the NOR output is connected to both inputs of another NOR gate, it is inverted again:

\[
Y=(A \downarrow B)\downarrow(A \downarrow B)=A+B
\]

### NOR Gate Truth Table

| A | B | A NOR B |
|---|---|---------|
| 0 | 0 | 1 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 0 |

### Procedure
1. Connect `A` and `B` to the first NOR gate.
2. Connect its output to both inputs of the second NOR gate.
3. Take the second gate output as `Y`.
4. Test all input combinations.

![First NOR gate](image.png)

![NOR gate used as inverter](image-1.png)

### Result

| A | B | Y = A OR B |
|---|---|------------|
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 1 |

![Circuit test](image-2.png)

![Circuit output](image-3.png)

### Conclusion
An OR gate was created successfully using two NOR gates.

---

## Experiment 2: OR Gate from NAND Gates

### Aim
Build an OR gate using only NAND gates.

### Theory
A NAND gate can work as a NOT gate when both inputs are the same:

\[
\overline{A}=A \text{ NAND } A
\]

Using De Morgan’s law:

\[
A+B=\overline{\overline{A}\cdot\overline{B}}
\]

So, two NAND gates invert `A` and `B`, and a third NAND gate produces the OR output.

### NAND Gate Truth Table

| A | B | A NAND B |
|---|---|----------|
| 0 | 0 | 1 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 0 |

### Procedure
1. Use one NAND gate for `NOT A`.
2. Use another NAND gate for `NOT B`.
3. Connect both inverted outputs to a third NAND gate.
4. Check the output for every input pair.

![Input inversion](image-4.png)

![Final NAND connection](image-5.png)

### Result

| A | B | Y = A OR B |
|---|---|------------|
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 1 |

![Test result](image-6.png)

![Test result](image-7.png)

### Conclusion
The OR function was obtained using three NAND gates.

---

## Experiment 3: AND Gate from NOR Gates

### Aim
Build an AND gate using only NOR gates.

### Theory
First, invert both inputs using NOR gates:

\[
\overline{A}=A \downarrow A
\]

\[
\overline{B}=B \downarrow B
\]

Then apply NOR:

\[
Y=\overline{\overline{A}+\overline{B}}=A \cdot B
\]

### Procedure
1. Connect `A` to both inputs of the first NOR gate.
2. Connect `B` to both inputs of the second NOR gate.
3. Connect the two outputs to a third NOR gate.
4. Test the circuit.

![Input inversion using NOR](image-8.png)

![Final NOR connection](image-9.png)

### Result

| A | B | Y = A AND B |
|---|---|-------------|
| 0 | 0 | 0 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |

![Test result](image-10.png)

![Test result](image-11.png)

### Conclusion
An AND gate was implemented using three NOR gates.

---

## Experiment 4: AND Gate from NAND Gates

### Aim
Build an AND gate using only NAND gates.

### Theory
The first NAND gate gives:

\[
X=\overline{A \cdot B}
\]

A second NAND gate inverts `X`:

\[
Y=X \text{ NAND } X=A \cdot B
\]

### Procedure
1. Connect `A` and `B` to the first NAND gate.
2. Connect its output to both inputs of the second NAND gate.
3. Observe the final output.

![First NAND gate](image-12.png)

![NAND used as inverter](image-13.png)

### Result

| A | B | Y = A AND B |
|---|---|-------------|
| 0 | 0 | 0 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |

![Test result](image-14.png)

![Test result](image-15.png)

### Conclusion
Two NAND gates were enough to produce an AND gate.

---

## Experiment 5: NOT Gate from NOR Gates

### Aim
Create a NOT gate using a NOR gate.

### Theory
When the same signal is given to both inputs of a NOR gate:

\[
Y=A \downarrow A=\overline{A}
\]

### Procedure
1. Connect input `A` to both NOR inputs.
2. Observe output `Y`.

![NOR inverter circuit](image-16.png)

### Result

| A | Y = NOT A |
|---|-----------|
| 0 | 1 |
| 1 | 0 |

![Test result](image-17.png)

### Conclusion
A NOR gate can act as a NOT gate by joining its two inputs.

---

## Experiment 6: NOT Gate from NAND Gates

### Aim
Create a NOT gate using a NAND gate.

### Theory
If both NAND inputs receive the same value:

\[
Y=A \text{ NAND } A=\overline{A}
\]

### Procedure
1. Connect input `A` to both NAND inputs.
2. Check the output.

![NAND inverter circuit](image-18.png)

### Result

| A | Y = NOT A |
|---|-----------|
| 0 | 1 |
| 1 | 0 |

![Test result](image-19.png)

### Conclusion
A NAND gate works as an inverter when both inputs are connected together.

---

## Experiment 7: Full Adder

### Aim
Design and test a one-bit full adder.

### Theory
A full adder adds three one-bit inputs:

- `A`: first input bit
- `B`: second input bit
- `Cin`: carry input

It gives two outputs:

- `Sum`
- `Cout`: carry output

The Boolean expressions are:

\[
Sum=A \oplus B \oplus Cin
\]

\[
Cout=AB+Cin(A \oplus B)
\]

A full adder can be built from two half adders and one OR gate.

### Procedure
1. Connect `A` and `B` to the first half adder.
2. Connect the first sum output and `Cin` to the second half adder.
3. Join the two carry outputs through an OR gate.
4. Test all eight input combinations.

![First half adder](image-20.png)

![Second half adder](image-21.png)

![Carry OR gate](image-22.png)

### Truth Table

| A | B | Cin | Sum | Cout |
|---|---|-----|-----|------|
| 0 | 0 | 0   | 0   | 0 |
| 0 | 0 | 1   | 1   | 0 |
| 0 | 1 | 0   | 1   | 0 |
| 0 | 1 | 1   | 0   | 1 |
| 1 | 0 | 0   | 1   | 0 |
| 1 | 0 | 1   | 0   | 1 |
| 1 | 1 | 0   | 0   | 1 |
| 1 | 1 | 1   | 1   | 1 |

![Test result](image-23.png)

![Test result](image-24.png)

![Test result](image-25.png)

![Test result](image-26.png)

### Conclusion
The full adder produced the correct sum and carry outputs for the tested input values.

---

## Experiment 8: Binary to BCD Conversion

### Aim
Convert a 4-bit binary number into Binary-Coded Decimal (BCD).

### Theory
BCD stores every decimal digit separately in 4-bit binary form. For example:

| Decimal Number | Binary Input | BCD Output |
|---|---|---|
| 5  | `0101` | `0101` |
| 9  | `1001` | `1001` |
| 10 | `1010` | `0001 0000` |
| 15 | `1111` | `0001 0101` |

For decimal values `0` to `9`, one BCD digit is sufficient. For values `10` to `15`, two BCD digits are needed: tens and ones.

### Procedure
1. Connect the four binary inputs to the converter circuit.
2. Connect the BCD outputs to the display or output indicators.
3. Test several binary values from `0000` to `1111`.
4. Compare the displayed decimal value with the expected result.

![Binary input circuit](image-27.png)

![BCD output circuit](image-28.png)

### Example Results

| Binary Input | Decimal Value | BCD Output |
|---|---:|---|
| `0000` | 0  | `0000` |
| `0011` | 3  | `0011` |
| `1001` | 9  | `1001` |
| `1010` | 10 | `0001 0000` |
| `1111` | 15 | `0001 0101` |

![Test result](image-29.png)

![Test result](image-30.png)

![Test result](image-31.png)

### Conclusion
The circuit converted binary input values to their BCD form. This type of conversion is useful in calculators, digital clocks, and seven-segment displays.

---

# End of Lab 1 Report
