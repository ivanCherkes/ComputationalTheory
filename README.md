# Computational Theory: SHA-256 Implementation

This repository contains my assessment work for the Computational Theory module. The project focuses on implementing and explaining the SHA-256 cryptographic hash algorithm step by step in Python, based on the NIST FIPS PUB 180-4 standard.

All explanations, implementations, and tests are documented in the main Jupyter notebook: [`problems.ipynb`](problems.ipynb).

---

## Getting Started

### Prerequisites

* **Python 3.10+**
* **Git**

### Installation and Running

1. **Clone the repository:**
   ```bash
   git clone https://github.com/ivanCherkes/ComputationalTheory.git
   cd ComputationalTheory
   ```

2. **(Optional) Create and activate a virtual environment:**
   * On macOS / Linux:
     ```bash
     python3 -m venv .venv
     source .venv/bin/activate
     ```
   * On Windows:
     ```cmd
     python -m venv .venv
     .venv\Scripts\activate
     ```

3. **Install required packages:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Launch the notebook:**
   ```bash
   jupyter notebook problems.ipynb
   ```
   *(Or open `problems.ipynb` directly in VS Code / JupyterLab).*

> **Tip:** In Jupyter, choose **Kernel -> Restart Kernel and Run All Cells** to run all cells from top to bottom and verify outputs.

---

## Problems Overview

The assessment is split into six sequential problems covering the SHA-256 specification:

| Problem | Title | Status | Summary |
| :--- | :--- | :--- | :--- |
| **Problem 1** | Representing SHA-256 Data | Completed | Explains representation of 32-bit words, 512-bit blocks, input byte strings, and big-endian formatting. |
| **Problem 2** | SHA-256 Bitwise Operations | Completed | Implements `Ch`, `Maj`, right rotation (`rotr`), shift (`shr`), and the four $\Sigma$ / $\sigma$ diffusion functions. |
| **Problem 3** | Generating SHA-256 Constants | Completed | Generates the 64 round constants from cube roots of the first 64 primes using NumPy, verified against FIPS 180-4. |
| **Problem 4** | Padding and Parsing Messages | Next up | Appending the '1' bit, zero padding, and 64-bit length suffix into 512-bit message blocks. |
| **Problem 5** | Compression Function | Upcoming | Inner round loop and updating the 8 working variables ($a$ through $h$). |
| **Problem 6** | Complete SHA-256 | Upcoming | End-to-end hash function tested against NIST standard test vectors. |

---

## Repository Structure

```text
.
├── README.md           # Project documentation and setup instructions
├── requirements.txt    # Minimal dependencies needed to run the notebook
├── problems.ipynb      # Main working notebook containing all problems and code
├── AGENTS.md           # AI and agent guidance documentation
├── .gitignore          # Files and virtual environments ignored by Git
├── data/               # Supporting data files (if needed)
└── img/                # Diagrams and images used in the notebook
```

---

## References

* National Institute of Standards and Technology (NIST). (2015). *Secure Hash Standard (SHS)* (FIPS PUB 180-4). https://doi.org/10.6028/NIST.FIPS.180-4
* Eastlake, D., & Hansen, T. (2011). *US Secure Hash Algorithms (SHA and SHA-based HMAC and HKDF)* (RFC 6234). Internet Engineering Task Force. https://doi.org/10.17487/RFC6234
* Python Official Documentation: [`struct` module](https://docs.python.org/3/library/struct.html) and [`int.from_bytes()`](https://docs.python.org/3/library/stdtypes.html#int.from_bytes).
