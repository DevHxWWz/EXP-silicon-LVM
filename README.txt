# Project Hermes: Non-FIFO Ultra-Saturation SHA-256 Core Engine

A professional microarchitectural benchmark profiling tool that simulates a custom, non-FIFO 512-bit register-weaving loop layout. It eliminates classical compiler scheduling bubbles and Read-After-Write (RAW) data dependency stalls by running 4 completely unlinked cryptographic message pipelines concurrently.

##  Required Development Tools

To compile and run this deep-tech code layout natively under Windows, you must install the following software packages:
1. **MSYS2 MinGW-w64 Environment:** Download and install the latest shell package from [msys2.org](https://msys2.org).
2. **GCC Toolchain & Build Tools:** Open your MSYS2 MinGW-w64 terminal console window and run this package management setup command:
   ```bash
   pacman -S mingw-w64-x86_64-gcc mingw-w64-x86_64-make --noconfirm
   ```

##  Compilation & Native Hardcode Build Commands

Navigate into your active repository folder using quotes to handle folder name space parameters safely, wipe old compilation remnants, and compile with maximum hardware unrolling flags:

```bash
cd "C:/Users/pc/Desktop/project ai"
rm -f real_sha256_benchmark.exe
g++ -O3 -msse4.2 -fopenmp hermes_expirement.cpp -o real_sha256_benchmark.exe
./real_sha256_benchmark.exe
```

##  How to Monitor System Performance Natively

1. **CPU Tracking:** Open Windows Task Manager (`Ctrl + Shift + Esc`), click the **Performance** tab, select **CPU**, and right-click the graph to choose **Change graph to -> Logical processors**. Watch all thread columns pin completely flat to 100% capacity instantly when the binary fires up.
2. **Thermal & Lag Profiling:** Because the dataset footprints sit permanently isolated within local execution registers and the L1 cache, notice how the machine remains entirely cool and dead responsive. You can freely stream video or read manga simultaneously because the motherboard memory bus is left completely unhindered.
3. **Architecture Reporting:** Once the execution loop concludes, the engine outputs genuine **Instructions Per Cycle (IPC)** metrics and **Silicon Port Load Factors** calculated directly against the clock ticks to track your pipeline saturation gains.
