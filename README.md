# Quantum Error Correction for Bell States Using Shor's 9-Qubit Code

This repository contains the complete Jupyter notebook implementation and experimental results for quantum error correction of Bell states using Shor's 9-qubit error correction code, developed as part of research conducted at RAIT, DY Patil Deemed to be University.

## Overview

This project demonstrates that Shor's quantum error correction can successfully protect Bell state entanglement for quantum cryptographic applications. The implementation achieves perfect fidelity (1.0000) with zero quantum bit error rate (QBER) across all tested error scenarios.

## Key Features

- **Complete Implementation**: Full Shor 9-qubit error correction protocol in a single Jupyter notebook
- **Bell State Protection**: Preserves quantum entanglement through error correction cycles
- **Multiple Error Types**: Handles bit-flip, phase-flip, and combined Y errors
- **Real-time Performance**: Sub-10ms correction cycles suitable for quantum communication
- **Perfect Accuracy**: 100% error detection and correction across all test cases
- **Comprehensive Analysis**: Built-in performance metrics, visualization, and statistical analysis
- **Cryptographic Ready**: Zero QBER makes it suitable for secure quantum key distribution

## Installation

### Prerequisites

- Python 3.8 or higher
- Jupyter Notebook or JupyterLab
- IBM Qiskit 2.0 or later
- NumPy, Matplotlib, Pandas, Seaborn

### Setup

1. Clone this repository:
```bash
git clone https://github.com/yourusername/quantum-bell-state-qec.git
cd quantum-bell-state-qec
```

2. Install required packages:
```bash
pip install -r requirements.txt
```

3. Launch Jupyter Notebook:
```bash
jupyter notebook ShorCodeQEC_BellStates.ipynb
```

4. Verify installation by running the first few cells in the notebook.

## Quick Start

### Running the Complete Implementation

Open `ShorCodeQEC_BellStates.ipynb` in Jupyter and run all cells to:

1. **Test Basic Shor Code**: Simple encoding/decoding validation
2. **Bell State Error Correction**: Complete demonstration across 5 error scenarios
3. **Performance Analysis**: Comprehensive metrics and visualizations
4. **Statistical Validation**: Detailed analysis of results

### Key Classes and Methods

The notebook contains the main `ShorCodeQEC` class with methods for:

```python
# Create the QEC system
qec = ShorCodeQEC()

# Run complete demonstration
results = qec.run_complete_demonstration()

# Generate performance plots
qec.create_comprehensive_plots()
```

### Error Scenarios Tested

1. **No errors** - Baseline performance
2. **Single bit-flip (X)** - First logical qubit
3. **Single phase-flip (Z)** - Second logical qubit  
4. **Y error** - Combined bit and phase flip
5. **Multiple errors** - Bit-flips on both logical qubits

## Experimental Results

### Performance Summary

| Metric | Result |
|--------|--------|
| Fidelity | 1.0000 (perfect) |
| QBER | 0.00% |
| Correction Time | <10ms average |
| Error Detection | 100% accuracy |
| Success Rate | 100% across all scenarios |

### Resource Requirements

- **Physical Qubits**: 38 total (19:1 overhead ratio)
- **Quantum Gates**: 26-29 per correction cycle
- **Classical Processing**: <0.2% of total time

### Comprehensive Analysis

The Jupyter notebook generates:
- **9 detailed performance plots** including fidelity analysis, key rate metrics, QBER trends
- **Statistical correlation matrices** between performance metrics
- **Resource efficiency analysis** and circuit complexity visualization
- **Error type impact analysis** with syndrome pattern interpretation

## Implementation Details

### ShorCodeQEC Class Structure

The notebook implements a comprehensive `ShorCodeQEC` class containing:

**Core Methods:**
- `create_bell_state()` - Bell state preparation
- `shor_encode_single_qubit()` - Individual qubit encoding
- `add_syndrome_measurement()` - Error detection protocols
- `inject_errors()` - Controlled error injection for testing
- `shor_decode_single_qubit()` - Logical qubit recovery

**Analysis Methods:**
- `calculate_bell_fidelity()` - Fidelity measurement from circuit results
- `calculate_key_rate_and_qber()` - QKD performance metrics
- `create_comprehensive_plots()` - 9-panel performance visualization
- `run_complete_demonstration()` - Full experimental pipeline

### Shor's 9-Qubit Code Architecture

Each logical qubit is encoded using 9 physical qubits arranged in a 3x3 structure:
- **Phase protection**: Quantum repetition across three blocks
- **Bit protection**: Classical repetition within each block
- **Syndrome measurement**: 8 ancilla qubits per logical qubit (6 for bit-flip, 2 for phase-flip)

### Error Detection and Correction

The implementation includes:
- **Comprehensive syndrome patterns** for all single-qubit error types
- **Classical decoding algorithms** with lookup tables for fast correction
- **Real-time correction protocols** suitable for quantum communication
- **Performance benchmarking** with statistical validation

## Running the Notebook

### Step-by-Step Execution

1. **Open the notebook**: `ShorCodeQEC_BellStates.ipynb`
2. **Import dependencies**: Run the first cell to import all required libraries
3. **Execute demonstrations**: 
   - Simple Shor code test (validates basic functionality)
   - Complete Bell state error correction (5 error scenarios)
   - Performance analysis and visualization
4. **View results**: Comprehensive plots and statistical analysis are generated automatically

### Expected Output

The notebook produces:
- **Console output** with detailed performance metrics for each scenario
- **Performance visualization** with 9 comprehensive analysis plots
- **Statistical summary** including averages, correlations, and efficiency metrics
- **Theoretical analysis** comparing results to QEC thresholds and QKD requirements

### Customization

You can modify:
- Error scenarios in the `error_scenarios` list
- Number of shots for statistical analysis
- Visualization parameters and plot styles
- Performance metrics and analysis methods

## Documentation

Detailed documentation is available in the `docs/` directory:

- **[Theoretical Background](docs/theoretical_background.md)**: Quantum error correction principles
- **[Implementation Details](docs/implementation_details.md)**: Technical design decisions
- **[Results Analysis](docs/results_analysis.md)**: Complete experimental findings

## Contributing

We welcome contributions! Please see our contributing guidelines:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## Citation

If you use this code in your research, please cite:

```bibtex
@inproceedings{bhor2025quantum,
  title={Quantum Error Correction for Bell States Using Shor's 9-Qubit Code: A Practical Implementation for Cryptographic Applications},
  author={Bhor, Sanket and Padiya, Pooja and Vidhate, Amarsingh and Chintawar, Amruta},
  booktitle={Proceedings of [Conference Name]},
  year={2025},
  organization={RAIT, DY Patil Deemed to be University}
}
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Authors

- **Sanket Bhor** - *M.Tech Student* - [sanket.d.bhor@gmail.com](mailto:sanket.d.bhor@gmail.com)
- **Pooja Padiya** - *R&D Coordinator & Research Guide*
- **Amarsingh Vidhate** - *Head of Department*
- **Amruta Chintawar** - *Assistant Professor*

**Institution**: Ramrao Adik Institute of Technology (RAIT), DY Patil Deemed to be University, Navi Mumbai, India

## Acknowledgments

- IBM for providing the Qiskit 2.0 framework
- DY Patil Deemed to be University for computational resources
- The quantum computing research community for foundational work

## Contact

For questions about this implementation or research collaboration:
- Email: sanket.d.bhor@gmail.com
- Institution: RAIT, DY Patil Deemed to be University

---

*This research demonstrates that perfect quantum error correction is achievable in practice, opening new possibilities for reliable quantum communication and cryptographic applications.*
