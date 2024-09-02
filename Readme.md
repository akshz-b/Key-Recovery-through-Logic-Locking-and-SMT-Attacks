### Logic Locking

#### Problem Statement

**Oracle Information:**
- The executable file `a.out` functions as the Oracle in this context.
- The Oracle accepts 11 inputs: `i1`, `i2`, `i3`, `i4`, `i6`, `G1`, `G2`, `G3`, `G4`, `GG1`, `GG2`.
- The Oracle provides 4 outputs: `o1`, `o2`, `o3`, `o4`.

To run the Oracle, use the following command:
```
./a.out 1 2 3 4 5 6 7 8 9 10 11
```
Here, the input values are: `i1=1`, `i2=2`, `i3=3`, `i4=4`, `i6=5`, `G1=6`, `G2=7`, `G3=8`, `G4=9`, `GG1=10`, `GG2=11`.

**Obfuscated File Information:**
- The obfuscated file contains locked C code.
- This code is protected by keys `Key1` to `Key7`.
- The goal is to determine the correct values for these keys.

**Oracle:**
- `./a.out`

**Locked Code:**
- `obfuscated.c`
- Contains the obfuscated logic used by the Oracle.
- The function `arf` takes all inputs and the 7 keys as arguments.

#### SMT Attack

**Installing Dependencies:**
1. Update package list:
   ```
   sudo apt-get update
   ```
2. Install Python 3:
   ```
   sudo apt-get install python3
   ```
3. Install the Z3 solver:
   ```
   pip3 install z3-solver
   ```

**Running the Code:**
1. Execute the Oracle:
   ```
   ./a.out 1 2 3 4 5 6 7 8 9 10 11
   ```
   The Oracle requires 11 arguments at runtime.

2. Execute the Python solver script:
   ```
   python3 solver.py
   ```
   The script includes predefined Differential Input Patterns (DIPs), and running it will yield the values for the keys.

