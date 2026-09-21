# Rocket Propulsion & Variable Mass Dynamics Lab

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.8-3178c6.svg?logo=typescript)](https://www.typescriptlang.org/)
[![React](https://img.shields.io/badge/React-19.0-61dafb.svg?logo=react)](https://react.dev/)
[![Vite](https://img.shields.io/badge/Vite-6.2-646cff.svg?logo=vite)](https://vitejs.dev/)
[![Author: Shamsuddin Piash](https://img.shields.io/badge/Author-Shamsuddin%20Piash-0ea5e9.svg)](https://piashoverflow.github.io)
[![BUET ME](https://img.shields.io/badge/Institution-BUET%20'25-10b981.svg)](https://buet.ac.bd)

> **Interactive Computational Physics Simulator & Educational Workbench**  
> Developed by **Shamsuddin Piash** | Department of Mechanical Engineering, Bangladesh University of Engineering and Technology (BUET).

---

## 🔬 Overview & Conceptual Motivation

Interactive aerospace mechanics simulation for the Tsiolkovsky rocket equation, variable mass dynamics, multi-stage optimization, and thrust vectoring.

Designed from **first-principles physics and numerical mechanics**, this simulation bridges textbook analytical theory and real-time computation. It enables students, researchers, and competitive engineering candidates to visualize dynamic force interactions, observe parametric trends, and verify conservation laws interactively.

---

## 📐 Mathematical Formulation & Physics Derivations

### Governing Dynamic Equations

The motion of a variable mass rocket in a gravitational field with atmospheric drag is governed by:

$$m(t) \frac{d\vec{v}}{dt} = \vec{F}_{thrust} + m(t)\vec{g} + \vec{F}_{drag}$$

Where instantaneous thrust $F_{thrust}$ is derived from fuel burn rate $\dot{m} = \frac{dm}{dt}$ and effective exhaust velocity $v_e$:

$$F_{thrust} = \dot{m} v_e + (p_e - p_a) A_e$$

Integrating across propellant depletion yields the classical **Tsiolkovsky Rocket Equation**:

$$\Delta v = v_e \ln\left(\frac{m_0}{m_f}\right) - \int_0^{t_b} g\sin\theta\,dt - \int_0^{t_b} \frac{F_{drag}}{m(t)}\,dt$$

---

## ✨ Key Features & Interactive Workbench

- **Tsiolkovsky Trajectory Integrator**: Real-time evaluation of payload ratio $\lambda = m_l / m_0$ and burnout velocity.
- **Multi-Stage Staging Optimization**: Simulates serial stage jettisoning to maximize terminal velocity.
- **Dynamic Telemetry Dashboard**: Monitors instantaneous mass $m(t)$, burn rate $\dot{m}$, Mach number, and acceleration $G$-force.
- **Atmospheric Density Gradient**: Models barometric altitude scaling $ho(h) = ho_0 e^{-h/H}$ and drag resistance.

---

## 🔒 Confidentiality, Security & Academic Integrity

This repository adheres strictly to professional security standards, privacy guidelines, and academic integrity policies:

- **Proprietary & Institutional Protection**: Underlying academic curricula, institutional questions, and confidential research data are sanitized and protected under institutional agreements.
- **Environment & Secrets Hygiene**: No private keys, passwords, or personal credentials are hardcoded. API tokens (e.g., Gemini AI or cloud compute) must be supplied via local `.env` files or secure CI/CD secrets.
- **Vulnerability Reporting**: Please refer to [SECURITY.md](SECURITY.md) for instructions on confidential disclosure.

---

## 🛠️ Project Structure & Architecture

```
.
├── src/
│   ├── components/       # UI panels, canvas renderer, sliders & controls
│   ├── utils/            # Physics solvers, RK4 ODE integration, vector math
│   ├── types.ts          # Strongly typed simulation interfaces
│   ├── App.tsx           # Primary application workbench
│   └── main.tsx          # Application root
├── public/               # Static assets & icons
├── metadata.json         # Simulator metadata & capabilities
├── package.json          # Dependencies & build scripts
├── tsconfig.json         # TypeScript compiler configuration
├── vite.config.ts        # Vite bundle & dev server configuration
├── SECURITY.md           # Confidentiality & vulnerability disclosure policy
└── LICENSE               # MIT License
```

---

## 🚀 Quickstart & Local Setup

### Prerequisites
- **Node.js**: `v18.0.0` or higher
- **npm** or **bun** / **pnpm**

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/piashoverflow/Rocket-Propulsion.git
cd Rocket-Propulsion

# 2. Install dependencies
npm install

# 3. Configure environment variables (if applicable)
cp .env.example .env

# 4. Launch the local development server
npm run dev
```

Visit `http://localhost:3000` in your browser to interact with the simulation.

### Production Build

```bash
npm run build
npm run preview
```

---

## 👤 Author & Academic Affiliation

**Shamsuddin Piash**  
*B.Sc. in Mechanical Engineering (Graduated March 2025)*  
**Bangladesh University of Engineering and Technology (BUET)**  
Dhaka, Bangladesh

- **Portfolio Website**: [piashoverflow.github.io](https://piashoverflow.github.io)
- **GitHub**: [@piashoverflow](https://github.com/piashoverflow)
- **LinkedIn**: [linkedin.com/in/shamsuddin-piash](https://linkedin.com/in/shamsuddin-piash)
- **Email**: [mohammadshamsuddinpiash0722@gmail.com](mailto:mohammadshamsuddinpiash0722@gmail.com)

---

## 📜 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for complete details.
