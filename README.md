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
✔ Ideal for:
- quick experiments
- simple pipelines
- high-level monitoring

2️⃣ Context manager mode
Provides finer control by tracking operations inside a defined execution scope.
```Python
from floppy import FLOPpyTracker
tracker = FLOPpyTracker(run_name="context_example")
with tracker:
    model.fit(X_train, y_train)
report = tracker.report(print_summary=True)
```
✔ Ideal for:
- precise measurements
- custom workflows
- advanced usage

🤖 PyTorch Integration
FLOPpy can be integrated directly into deep learning pipelines:
```Python
tracker.torch_bind(
    model=model,
    optimizer=optimizer,
    loss_fn=loss_fn,
    device=device
)
```

## 📊 Example Scripts
Scikit-learn Example
- Dataset loading
- Model training
- FLOP/BOP tracking
- Performance reporting

PyTorch Example
- Neural network training
- Integrated computational tracking
- Detailed cost analysis

## 🌱 Green AI Perspective

FLOPpy contributes to sustainable AI development by enabling:
- efficient model evaluation
- reduced computational waste
- awareness of computational cost

## 👨‍💻 About

FLOPpy is a hardware-agnostic library for monitoring computational cost in ML/DL models, developed during a research internship at ICAR-CNR.

This repository is maintained by:
Francesco Mandarino
Junior Software Engineer | Machine Learning | Green AI
