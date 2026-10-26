# Static Sign-Language Alphabet Recognition Prototype

An educational computer-vision prototype for recognizing a discrete subset of static manual alphabet hand postures with built-in uncertainty estimation and ethical safeguards.

> **Important Sociotechnical Note:**  
> This prototype recognizes isolated, static hand configurations from a manual alphabet (fingerspelling). **It is NOT a sign language translator and does not replace human interpreters.** Natural signed languages (ASL, BSL, etc.) are full languages featuring dynamic spatial grammar, movement, and critical non-manual facial and bodily markers. See [Accessibility & Limitations Note](docs/accessibility_and_limitations.md) for detailed community perspectives and citations.

---

## Project Structure

```
sign_alphabet_recognition/
├── README.md                           # Project overview & ethical scope
├── data/                               # Dataset storage and splits
│   ├── raw/                            # Original downloaded datasets
│   ├── processed/                      # Extracted hand landmarks / normalized tensors
│   └── splits/                         # Signer-independent train/val/test split manifests
├── notebooks/                          # Interactive analysis & model pipelines
│   └── static_alphabet_recognition.ipynb # Reproducible end-to-end model notebook
├── src/                                # Core Python modules
│   ├── __init__.py
│   ├── landmarks.py                    # MediaPipe extraction & coordinate normalization
│   ├── dataset.py                      # Signer-stratified data loader
│   ├── models.py                       # Baseline & improved classifiers
│   ├── evaluation.py                   # Per-class metrics & confusion matrix generators
│   └── uncertainty.py                  # Softmax entropy & confidence thresholding
├── demo/                               # Interactive visual application
│   └── app.py                          # Live webcam / image demo with abstention indicator
└── docs/                               # Formal project deliverables
    ├── dataset_card.md                 # Deliverable 1: Dataset provenance & consent audit
    ├── per_class_evaluation.md         # Deliverable 3: Detailed metric breakdown
    ├── accessibility_and_limitations.md # Deliverable 5: Sociotechnical & community analysis
    └── final_report.md                 # Deliverable 6: Complete technical report
```

---

## Six Project Deliverables

- [ ] **Deliverable 1:** [Dataset Card](docs/dataset_card.md)
- [ ] **Deliverable 2:** [Reproducible Model Notebook](notebooks/static_alphabet_recognition.ipynb)
- [ ] **Deliverable 3:** [Per-Class Evaluation Results](docs/per_class_evaluation.md)
- [ ] **Deliverable 4:** [Gesture Recognition Demo](demo/app.py)
- [ ] **Deliverable 5:** [Accessibility & Limitations Note](docs/accessibility_and_limitations.md)
- [ ] **Deliverable 6:** [Final Report & Presentation](docs/final_report.md)

---

## Technical Stack
- **Python 3.10+**
- **MediaPipe Hands** (21 3D hand landmarks)
- **OpenCV** (Image processing & demo stream)
- **Scikit-Learn & PyTorch** (Baseline & calibrated classifiers)
- **Matplotlib & Seaborn** (Confusion matrices & subgroup visualizations)
