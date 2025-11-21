# Buffer Overflow Exploitation Lab

This repository documents my successful exploitation of a stack-based buffer overflow vulnerability using the Labtainer cybersecurity training environment.  
I completed the full workflow: identifying the vulnerability, constructing an exploit string, bypassing protections, gaining a **root shell**, and validating results using `checkwork`.

---

## 🚀 Overview

The objective of this lab was to exploit a vulnerable C program and redirect execution flow to custom shellcode.  
Using GDB, I analyzed the program’s memory layout, identified the return address offset, and crafted an exploit payload to escalate privileges.

---

## 🔧 Tools & Technologies Used
- **Linux (Ubuntu / Labtainer)**
- **GDB** (GNU Debugger)
- **GCC** (compiling without stack protection)
- **ASLR testing**
- **Custom shellcode**
- **Hex payload construction**
- **Python scripting for payload generation**
- **Privilege escalation exploitation**

---

## 🧠 Key Skills Demonstrated

### ✔️ Memory Analysis
- Located `EBP`, buffer start, and return address using GDB.
- Identified the exact return offset (`retoffset = 507`).

### ✔️ Exploit Development
- Disabled stack protection and compiled vulnerable C code.
- Injected shellcode into the stack.
- Crafted a malicious input string to overwrite EIP.
- Redirected control flow to shellcode.

### ✔️ Privilege Escalation
- Successfully opened a **root shell**.
- Accessed and displayed the `/root/.secret` file.

### ✔️ Validation
- Ran `stoplab` and `checkwork` to confirm:
  - `gain_root_priv = Y`
  - `stack_protect` tested
  - `while_run` requirements acknowledged

---
