# Grpah Neural Network Software & Hardware Implementation.

## Software Implementation:
- Several implementations available using DGL, Pytorch, and from scratch.
- Their comparisions are also availabel.
- They are in `GNN_Practice` folder.
- Backdoor attack is also simulated using `cora` dataset.
- TO DO: Run the code from `https://github.com/sharc-lab/DGNN-Booster`  because this is the one that has been used for hardware implementation.

## Hardware Implementation:
- HLS using Vivado, the source is taken from `https://github.com/sharc-lab/DGNN-Booster`.
- There are a number of changes needed. We perform those and the updated code for a `DGNN-booster1-EvolveGCN.cpp` is run.
- Also required to do some changes in `script_EolveGCN.tcl`.
- Please refer to `DBNN-Booster/HLS` folder of the Ubuntu machine (laptop).
- Run the code `vivado_hls -f script_EolveGCN.tcl` from that folder.
- The synthesis step is successfully completed. IP export step failed.
- Nevertheless the HDLs are generated in `EvolveGCN_final_100/solution3/impl/ip/hdl/verilog` folder.
- Then the RTL synthesis is also done sucessfully. Please refer to the folder `RTL_project` in the `DGNN-Booster`.
- TO DO: THe implementation, bit-stream generation, loading, and verification on the FPGA.
