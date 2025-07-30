# CrystalGen – Generative AI for Inorganic Materials Design

CrystalGen is a diffusion-based generative model designed to create stable, novel inorganic materials. It draws inspiration from the MatterGen paper but extends the baseline with a focus on broader property constraints, improved fine-tuning mechanisms, and enhanced adaptability to real-world use cases.

## 🚀 Motivation

Traditional material discovery relies on slow, trial-and-error experiments and human intuition. Modern AI tools like high-throughput screening and ML-based predictors have improved efficiency but remain limited:

- Only explore a small fraction (~10⁶–10⁷) of the possible material space (~10¹⁰)
- Fail to generate stable crystals or optimize complex properties like symmetry or magnetism

## 🎯 Our Solution

CrystalGen aims to overcome these limitations through:

- **Inverse design** to directly generate material structures
- **Support for diverse chemical elements and target properties**
- **Improved stability**, with generated materials up to **15× closer to local energy minima**

---

## 📋 Project Overview

| **Aspect** | **Details** |
|------------|-------------|
| **Objective** | Generate stable inorganic crystal structures based on user-defined properties (e.g., symmetry, magnetism, band gap) |
| **Approach** | Uses a diffusion-based generative process to refine atom types, positions, and the crystal lattice |
| **Fine-Tuning** | Adapter modules condition generation on specific property labels to steer toward desired outcomes |

---

## 🏗️ Architecture & Workflow

![Architecture Diagram](https://github.com/user-attachments/assets/21be3bd0-4594-4d2f-9fc4-4be254c7ef11)

### Process Flow:
1. **Input**: Randomized crystal structure
2. **Diffusion Process**: Corrupts and denoises atom types (A), coordinates (X), and lattice (L)
3. **Score Network**: Equivariant neural network trained to reverse the corruption process
4. **Adapter Modules**: Injected during fine-tuning for property-conditioned generation
5. **Output**: Stable, property-specific inorganic material

---

## 🛠️ Tech Stack

| Component | Technology |
|-----------|------------|
| **Core Framework** | Python, PyTorch |
| **Graph Processing** | PyTorch Geometric |
| **Generation Method** | Diffusion Models |
| **Neural Networks** | Equivariant GNNs |
| **Interface** | Streamlit / FastAPI |

---

## 👥 Target Users

| User Type | Use Case |
|-----------|----------|
| **Materials Scientists** | Accelerate discovery of new compounds with desired properties |
| **Chemical Engineers** | Design materials for industrial needs (catalysts, battery components) |
| **Academic Researchers** | Explore hypothetical materials and validate computational hypotheses |
| **AI Researchers** | Apply generative models to physical sciences |
| **Startups & R&D Labs** | Develop advanced materials for clean energy, semiconductors, carbon capture |

---

## ✨ Key Features

### 🔬 **Crystal Structure Generation**
Generate crystal lattices from parameters, templates, or latent representations.

### ⚛️ **Diffusion-Based Crystal Generator**
Uses a diffusion model that corrupts and denoises atomic structures to generate stable ones.

### 📐 **Symmetry and Lattice Validation**
Verify generated structures for stability, physical correctness, and crystallographic validity.

### 🧠 **AI-Powered Property Prediction**
Use pre-trained models to predict properties such as bandgap, density, energy, and stability.

### 🖼️ **3D Visualization**
Interactive rendering of unit cells, atoms, and bonds in 2D/3D using Plotly and ASE.

### 🌐 **Broader Chemical Element Support**
Unlike some models limited to narrow elements, CrystalGen works across diverse elements.

### 🔄 **Modular Agentic Design**
Each subtask (generation, validation, prediction, etc.) is managed by independent agents, making workflows flexible and extensible.



---

## 🤝 Contributors

| Contributor | GitHub |
|-------------|--------|
| Harini Manga | [@harinimanga31](https://github.com/harinimanga31) |
| Abhigna Sree | [@abhigna-sree](https://github.com/abhigna-sree) |
| Harshitha Nampally | [@HarshithaNampally](https://github.com/HarshithaNampally) |
| Siri Chandana Reddy | [@Siri-chandanareddy21](https://github.com/Siri-chandanareddy21) |
| Sadhvini | [@Sadhvini26](https://github.com/Sadhvini26) |

---


