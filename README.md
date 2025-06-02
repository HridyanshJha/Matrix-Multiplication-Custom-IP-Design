# 🚀 Custom IP Design for 8x8 Matrix Multiplication using Vivado HLS

This project demonstrates the design and optimization of a custom IP block for 8x8 matrix multiplication using **Xilinx Vivado HLS** and Vivado Block Design. The implementation focuses on **performance optimization techniques** such as **pipelining**, **array partitioning**, and **memory-mapped interfacing**, achieving significant speedup compared to standard software execution.

---

## 🛠️ Tools & Technologies
- Xilinx Vivado HLS
- Xilinx Vivado Block Design
- Xilinx SDK
- C/C++ (HLS)
- ARM Cortex-A9 (Processing System)

---

## ⚙️ Optimization Techniques Used

### 🔁 `#pragma HLS PIPELINE`
Used to enable **loop pipelining**, allowing concurrent execution of operations across multiple clock cycles. Reduces loop **Initiation Interval (II)** towards 1 for maximum throughput.

### 🧩 `#pragma HLS ARRAY_PARTITION`
Removes memory bottlenecks by **partitioning arrays** for parallel access, enabling simultaneous data fetch and compute.

### 🧠 Memory-Mapped Interface
Directly maps matrix data between PS and PL, **reducing transfer latency** and removing dependency on DMA.

---

## 📊 Performance Results

| Method                                  | Avg Execution Time (µs) |
|----------------------------------------|--------------------------|
| PS (Software on ARM)                   | 26.074                   |
| Pipelined MMUL in PL                   | 31.892                   |
| Pipelined + Array Partitioned MMUL     | 7.284                    |
| Pipelined + AP + Memory Mapped MMUL    | 6.415                    |

✅ **Achieved ~4× speedup**, reducing execution time from **26.07µs to 6.41µs**

---

## 📈 Key Contributions
- Developed a fully functional 8x8 MMUL IP using HLS and Vivado
- Integrated IP into Vivado Block Design with PS-PL communication
- Optimized hardware logic for speed using advanced HLS directives
- Verified output using **JTAG terminal** and **Xilinx SDK C code**

---

## 📷 Output Example (JTAG Terminal)
