# MatterGen – Generative AI for Inorganic Materials Design

MatterGen is a diffusion-based generative model designed to create stable, novel inorganic materials. It addresses the limitations of traditional and AI-based material discovery methods by enabling inverse design with customizable property constraints.

Traditional material discovery relies on human intuition and physical experiments, making it slow and resource-intensive. Modern AI tools improve efficiency but are limited in scope—often failing to produce stable structures or handle multiple complex constraints.

MatterGen solves this by:
- Supporting **inverse design** of materials
- Handling **diverse elements and properties**
- Producing materials **15× closer to local energy minimum** than prior models

---

## Project Overview

- **Objective**: Generate stable inorganic crystal structures based on user-defined properties such as symmetry, magnetism, and band gap.
- **Approach**: Uses a diffusion-based generative process that iteratively refines atom types, positions, and the crystal lattice.
- **Fine-Tuning**: Employs adapter modules to condition generation on specific property labels for targeted material discovery.

---

## Architecture & Workflow

1. **Input**: Randomized crystal structure
2. **Diffusion Process**: Iteratively corrupts and denoises atom types (A), coordinates (X), and lattice (L)
3. **Score Network**: Equivariant neural network trained to reverse the corruption
4. **Adapter Modules**: Injected during fine-tuning for property-conditioned generation
5. **Output**: Stable, property-specific inorganic material

---

## Tech Stack

- **Python**, **PyTorch**
- **PyTorch Geometric** for graph-based structures
- **Diffusion models** for structure generation
- **Equivariant GNNs** for symmetry-aware learning
- **API**: **Streamlit / FastAPI** for interface

---

## Key Features

- Generate stable, novel inorganic materials
- Fine-tune for target properties (e.g., band gap, magnetic density)
- Explore beyond known materials (10⁶–10⁷ → ~10¹⁰ design space)
- Outperforms state-of-the-art generative models
