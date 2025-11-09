## 🧩 Alternative Version of [CHEMSHELL INTERFACE](https://github.com/postulkj/TROJAN_BAGEL): BAGEL Integration

A modified version of the interface extends ChemShell functionality to support the **BAGEL** quantum chemistry program,  
which is not natively integrated with ChemShell.

To achieve this:
1. ChemShell is configured to believe it is using the **ORCA** backend.
2. Instead of calling the ORCA executable directly, ChemShell invokes a custom **run_script**.
3. This script runs **BAGEL**, reformats its output to mimic ORCA’s format, and returns the results to ChemShell.

This approach allows ChemShell and ABIN to obtain energies and gradients from BAGEL transparently,  
demonstrating flexible software coupling and file-level protocol emulation.
