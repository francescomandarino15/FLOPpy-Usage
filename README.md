# FLOPpy-Usage

![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![PyPI](https://img.shields.io/badge/PyPI-floppy--tracker-blue)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Status-Active-brightgreen)

This repository provides practical examples demonstrating how to use **FLOPpy**, a hardware-agnostic Python library for monitoring the computational cost of Machine Learning and Deep Learning models.

FLOPpy enables the estimation of computational cost using metrics such as:

- **FLOP** (Floating Point Operations)  
- **BOP** (Bit Operations)  

supporting the development of efficient and sustainable AI systems in line with **Green AI** principles.

---

## 🔗 Resources

- 📦 PyPI: https://pypi.org/project/floppy-tracker/  
- 💻 Official Repository: [ADD OFFICIAL FLOPPY REPO LINK HERE]

---

## ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/floppy-examples.git
cd floppy-examples
# Install dependencies
pip install -r requirements.txt
# Install FLOPpy
pip install floppy-tracker
```

## 🧠 FLOPpy Usage Modes

FLOPpy supports two main usage paradigms:

1️⃣ Run-based mode
The simplest way to monitor computational cost.

```Python
from floppy import FLOPpyTracker
tracker = FLOPpyTracker(run_name="sklearn_example")
tracker.run(model=model)
model.fit(X_train, y_train)
report = tracker.report(print_summary=True)
```



FLOPpy is a hardware-agnostic library for monitoring computational cost in ML/DL models, developed during a research internship at ICAR-CNR.
