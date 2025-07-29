# CrystalGen – Generative AI for Inorganic Materials Design

CrystalGen is a diffusion-based generative model designed to create stable, novel inorganic materials. It draws inspiration from the MatterGen paper but extends the baseline with a focus on broader property constraints, improved fine-tuning mechanisms, and enhanced adaptability to real-world use cases.

Traditional material discovery relies on slow, trial-and-error experiments and human intuition. Modern AI tools like high-throughput screening and ML-based predictors have improved efficiency but remain limited:

* Only explore a small fraction (\~10⁶–10⁷) of the possible material space (\~10¹⁰)
* Fail to generate stable crystals or optimize complex properties like symmetry or magnetism

CrystalGen aims to overcome these limitations through:

* **Inverse design** to directly generate material structures
* **Support for diverse chemical elements and target properties**
* **Improved stability**, with generated materials up to **15× closer to local energy minima**

---

## Project Overview

* **Objective**: Generate stable inorganic crystal structures based on user-defined properties (e.g., symmetry, magnetism, band gap)
* **Approach**: Uses a diffusion-based generative process to refine atom types, positions, and the crystal lattice
* **Fine-Tuning**: Adapter modules condition generation on specific property labels to steer toward desired outcomes

---

## Architecture & Workflow

> ![architecture_diagram](https://github.com/user-attachments/assets/21be3bd0-4594-4d2f-9fc4-4be254c7ef11)

1. **Input**: Randomized crystal structure
2. **Diffusion Process**: Corrupts and denoises atom types (A), coordinates (X), and lattice (L)
3. **Score Network**: Equivariant neural network trained to reverse the corruption process
4. **Adapter Modules**: Injected during fine-tuning for property-conditioned generation
5. **Output**: Stable, property-specific inorganic material

---

## Tech Stack

* **Python**, **PyTorch**
* **PyTorch Geometric** – Graph representation of crystal structures
* **Diffusion Models** – Generative process for structure creation
* **Equivariant GNNs** – Learn symmetry-aware representations
* **Streamlit / FastAPI** – Optional APIs and user interfaces

---

## End Users

* **Materials Scientists**: To accelerate discovery of new compounds with desired physical or chemical properties.
* **Chemical Engineers**: For designing materials tailored to industrial needs (e.g., catalysts, battery components).
* **Academic Researchers**: As a tool for exploring hypothetical materials and validating computational hypotheses.
* **AI Researchers**: Interested in applying generative models to physical sciences.
* **Startups & R&D Labs**: Developing advanced materials for clean energy, semiconductors, or carbon capture technologies.

---

## Key Features

* Generate stable, novel inorganic materials from scratch
* Fine-tune generation toward specific properties (e.g., band gap, magnetic density)
* Efficient exploration of the material space (\~10¹⁰ vs \~10⁶ in current methods)
* Outperforms existing state-of-the-art models in stability and diversity

---

## Contributors

* [@harinimanga31](https://github.com/harinimanga31)
* [@abhigna-sree](https://github.com/abhigna-sree)
* [@HarshithaNampally](https://github.com/HarshithaNampally)
* [@Siri-chandanareddy21](https://github.com/Siri-chandanareddy21)
* [@Sadhvini26](https://github.com/Sadhvini26)
