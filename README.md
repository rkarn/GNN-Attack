# Graph Neural Network

## Backdoor Attack:
- Backdoor attack is simulated using in `Backdoored GNN (Cora dataset).ipynb` and `Backdoored GNN (Amazon Co-purchase Network).ipynb`.
- Two datasets have been used:
  - `Cora`
  - `Amazon Co-purchase Network`
- Twelve different mechanism of poisoning backdoor is shown. THey are as follows:
  - Edge Insertion/Deletion
  - Node Injection
  - Feature Manipulation
  - Subgraph Trigger Insertion
  - Graph Structure Poisoning
  - Label Manipulation
  - Model Parameter Manipulation
  - Graph Sampling Attack
  - Mixing Clean and Poisoned Data
  - Adaptive Backdoor Triggering
  - Attribute Injection
  - Temporal Graph Poisoning

#### Baseline Software Implementation for get started:
- Several implementations available using DGL, Pytorch, and from scratch.
- Their comparisions are also availabel.
- They are in `GNN_Practice` folder.

#### Hardware Implementation (in progress):
- HLS using Vivado, the source is taken from `https://github.com/sharc-lab/DGNN-Booster`.
- There are a number of changes needed. We perform those and the updated code for a `DGNN-booster1-EvolveGCN.cpp` is run.
- Also required to do some changes in `script_EolveGCN.tcl`.
- Please refer to `DBNN-Booster/HLS` folder of the Ubuntu machine (laptop).
- Run the code `vivado_hls -f script_EolveGCN.tcl` from that folder.
- The synthesis step is successfully completed. IP export step failed.
- Nevertheless the HDLs are generated in `EvolveGCN_final_100/solution3/impl/ip/hdl/verilog` folder.
- Then the RTL synthesis is also done sucessfully. Please refer to the folder `RTL_project` in the `DGNN-Booster`.
- TO DO: THe implementation, bit-stream generation, loading, and verification on the FPGA.
- TO DO: Run the code from `https://github.com/sharc-lab/DGNN-Booster`  because this is the one that has been used for hardware implementation.
