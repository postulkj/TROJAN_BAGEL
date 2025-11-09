## 🧩 Alternative Version of [ChemShell–ABIN Interface](https://github.com/postulkj/CHEMSHELL_INTERFACE): BAGEL Integration

A modified version of the ChemShell–ABIN interface that extends its functionality to support the **BAGEL** quantum chemistry program,  
which is not natively integrated with ChemShell.

---

## 🔍 Overview

ChemShell typically interfaces with QM codes such as ORCA, MOLPRO, and MNDO.  
This version introduces a **protocol emulation layer** that enables ChemShell to communicate with BAGEL as if it were using ORCA:

1. ChemShell is configured to call the ORCA backend.  
2. The ORCA executable is replaced by a **wrapper script**.  
3. The script runs **BAGEL**, reformats its output into ORCA-compatible format, and returns energies and gradients to ChemShell.

This design allows **ABIN–ChemShell dynamics** to use BAGEL transparently, without modifying either ChemShell or BAGEL.

---

## ⚙️ Structure

```text
TROJAN_BAGEL/
├── run_script.sh      # Wrapper bridging ChemShell and BAGEL
├── test_inputs/       # Example ChemShell/BAGEL inputs
└── README.md
