# Two-stage-pipeline-RV32I-processor-core
 Developed an energy-efficient two-stage RV32I processor
core with simplified pipeline control and reduced hardware complexity, targeting low-power
edge-computing applications.
The proposed architecture is designed in a way that prevents the occurrence of any control hazards. The primary cause of control hazard is the processor's incapacity to determine the instruction memory's subsequent address when branch and jump instructions are used in pipeline architecture. The entire architecture was split into two sections by the pipeline register, Stage 1 and Stage 2. All of the functional blocks of the architecture, including the Register Bank, ALU, Program Counter, MUX, Data Memory, etc., were managed by the control unit represented in Figure 2. When it detects a branch or jump signal instruction, the control unit will produce a control signal known as pc⁢_src. The program counter value is updated in response to the signal produced by the control unit. Either PC + 4, Masked⁢_value or Imm⁢_add is the program counter's updated value. In order to mitigate the control hazard, the pipeline register must be positioned after the ALU. The pipeline register, which can traverse all data paths, is positioned after the ALU. Therefore, stage 1 includes the functional blocks till ALU, also illustrated in Figure 2. Stage 2 supports register writing and data memory access. The control signal must also pass via the pipeline register in order to control register write and data memory read/write. All of the architecture's functional blocks are arranged in stage 1 so that the control unit can handle branch and jump instructions without needing extra hardware, such as stalling units or branch prediction units.
<img width="1345" height="763" alt="image" src="https://github.com/user-attachments/assets/9ae5da0e-4488-41b3-904f-6de211eb207f" />
Data hazard handling and forwarding unit
<img width="1339" height="759" alt="image" src="https://github.com/user-attachments/assets/62f837cf-baff-4b4f-86a1-f8ef452ce191" />
HAhazrd control unit
<img width="1326" height="759" alt="image" src="https://github.com/user-attachments/assets/3bc5c244-5750-4387-981d-9e582e798fbf" />
Area and complexity analysis
<img width="1339" height="757" alt="image" src="https://github.com/user-attachments/assets/d7e21220-92be-4efc-961a-79febe9a411f" />
Fibonacci series generation on two stage rv32I 
<img width="1336" height="753" alt="image" src="https://github.com/user-attachments/assets/2276e9fd-ec29-4fb5-b8a1-7cba411d4a12" />
Fpga Prototype and resource utilisation
<img width="360" height="224" alt="image" src="https://github.com/user-attachments/assets/cbdc7538-2a7d-4a7d-ac02-f746d0d32009" /> <img width="333" height="183" alt="image" src="https://github.com/user-attachments/assets/9dba4a37-4ff7-4af7-9859-a2aac1eb9682" />

