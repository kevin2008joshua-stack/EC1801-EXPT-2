# EXPT 2 - Verification of Logic Gates
### SIMULATION AND VERIFICATION OF AND, OR, AND NOT GATES
## Aim
To design, implement, and verify the functionality of basic AND, OR, and NOT logic gates using Verilog HDL, and verify the functionality using Synopsys VCS and DVE.
# Software Required
•	Synopsys VCS
•	Synopsys DVE
•	Linux Terminal
•	Verilog HDL
# Boolean Function
The basic logic gates realize the following Boolean functions:

•	AND: Y_AND = A . B
•	OR: Y_OR = A + B
•	NOT: Y_NOT = A'

# Theory / Synopsis
Logic gates are the basic building blocks of digital systems. NAND and NOR are universal gates. XOR produces 1 when its inputs differ, while XNOR produces 1 when its inputs are equal.
# Files to be Created
File name	Purpose
logic_gates.v	Logic-gate RTL
logic_gates_tb.v	All input combinations and VCD generation
 # Verilog  Program
<img width="1917" height="488" alt="exp2 (2)" src="https://github.com/user-attachments/assets/7c0ad400-e48e-455a-9269-b467b0f69a5b" />

# **Test Bench Program**
<img width="1917" height="873" alt="exp2 (3)" src="https://github.com/user-attachments/assets/263fb14f-2507-4f86-a6a8-19617b139d68" />
# Truth Table
<img width="940" height="318" alt="image" src="https://github.com/user-attachments/assets/8a343bdb-ffb4-4aac-8b88-cf59eca374a8" />
# Simulation Procedure
STEP 1 – Open Terminal
Open a terminal in the experiment folder.
bash

STEP 2 – Load Synopsys Environment
source /synopsys/start.sh

STEP 3 – Compile Using VCS
vcs logic_gates.v logic_gates_tb.v -full64
If compilation is successful, VCS generates the simulation executable:
simv

STEP 4 – Run Simulation
./simv
The terminal displays the input combinations and corresponding output F.
A VCD waveform file is also generated:
exp1_boolean_min.vcd

STEP 5 – Open DVE
dve -full64
Other option
dve -full64 &
A DVE environment will open.

DVE Waveform Verification
In DVE:
Open the testbench hierarchy.
Locate the signals: 
a
b
y_and
y_or
y_not
Add the signals to the waveform window.
Run/inspect the waveform.
Verify that y_and = 1 only when a=1 AND b=1 — the single combination where both inputs are high.
Verify that y_or = 1 whenever a=1 OR b=1 (any input high forces the output high).
Verify that y_not is always the exact complement of a, regardless of b.
The waveform should agree with the truth table.
# Expected Result
The basic logic gates — AND, OR, and NOT — were realized using Verilog HDL:
Y_AND = A.B
Y_OR = A+B
Y_NOT = A'
The design was compiled and simulated using Synopsys VCS, and the functionality was verified using DVE waveform analysis, matching the expected truth table.
Output
# OUTPUT
<img width="1917" height="475" alt="exp2 (1)" src="https://github.com/user-attachments/assets/8623755c-3c22-49c3-a386-9c54d28bc1f6" />
