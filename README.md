# LFSR - Linear Feedback Shift Register

A Python implementation of Linear Feedback Shift Registers (LFSRs) for cryptographic applications, random number generation, and digital signal processing.

## Overview

This project provides two LFSR implementations:
- `BasicLFSR`: A simple 4-bit LFSR with hardcoded feedback polynomial
- `GeneralLFSR`: A configurable LFSR supporting arbitrary sizes, tap configurations, and seeds

LFSRs are widely used in cryptography, random number generation, digital communications, and more.

## Features

- Basic and general-purpose LFSR implementations
- Support for arbitrary-sized registers
- Configurable feedback taps (polynomial configuration)
- Utility functions for sequence generation and analysis
- Comprehensive test suite
- Educational examples including a simple stream cipher

## Usage

Basic example:

```python
from lfsr.basic_lfsr import BasicLFSR

# Create a basic 4-bit LFSR
lfsr = BasicLFSR()

# Generate bits
for _ in range(10):
    bit = lfsr.next_bit()
    print(f"Generated bit: {bit}, New state: {lfsr.get_state()}")
```
## Installation
bashgit clone https://github.com/your-username/lfsr.git
cd lfsr
pip install -e .

## Testing
Run the test suite:
```
python -m unittest 
```
License
This project is licensed under the MIT License - see the LICENSE file for details.

### .gitignore

Create a .gitignore file to avoid committing unnecessary files:
Byte-compiled / optimized / DLL files
pycache/
*.py[cod]
*$py.class
Distribution / packaging
dist/
build/
*.egg-info/
Virtual environments
venv/
env/
.env/
IDE files
.idea/
.vscode/
*.swp
*.swo
Test cache
.pytest_cache/
.coverage
htmlcov/
OS specific files
.DS_Store
Thumbs.db

### setup.py

Create a setup.py file for package installation:

```python
from setuptools import setup, find_packages

setup(
    name="lfsr",
    version="0.1.0",
    packages=find_packages(),
    description="Linear Feedback Shift Register Implementation",
    author="Your Name",
    author_email="your.email@example.com",
    url="https://github.com/your-username/lfsr",
    classifiers=[
        "Development Status :: 3 - Alpha",
        "Intended Audience :: Developers",
        "Programming Language :: Python :: 3",
        "Programming Language :: Python :: 3.6",
        "Programming Language :: Python :: 3.7",
        "Programming Language :: Python :: 3.8",
        "Programming Language :: Python :: 3.9",
    ],
    python_requires=">=3.6",
)
