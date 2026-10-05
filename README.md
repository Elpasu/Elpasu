<!--
  README de PERFIL. Va en un repo PÚBLICO llamado exactamente "Elpasu" (igual que tu usuario).
  GitHub lo muestra arriba de todo en github.com/Elpasu.
  Los comentarios como este no se ven en la página: son notas para vos.
-->

# Hi, I'm Lucas 👋

**Computational chemist building deep-learning models for NMR structure elucidation** — from generating DFT-scale training data on HPC clusters to the models, the evaluation protocol and the software people actually use.

PhD candidate in Chemical Sciences at UNR · IQUIR–CONICET (Rosario, Argentina). I work where quantum chemistry, machine learning and software engineering meet.
<!-- Cuando defiendas, cambiá la línea de arriba por: "PhD in Chemical Sciences — UNR · IQUIR–CONICET (Rosario, Argentina)." -->

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Lucas%20Passaglia-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/passaglialucas/)
[![Email](https://img.shields.io/badge/Email-contact-555?logo=gmail&logoColor=white)](mailto:passaglialucas95@gmail.com)

🔎 **Open to** remote roles in computational chemistry, cheminformatics and ML for science.

---

## What I work on

### 🧠 Deep learning: from NMR spectra to molecular structure · [showcase →](https://github.com/Elpasu/nmr-structure-elucidation)

A model reads 2D NMR (HSQC), ¹³C peaks and the molecular formula, and predicts the molecule's **carbon-environment fingerprint**; that fingerprint then constrains an **automatic structure generator**, so it only explores structures consistent with the spectra. I built the whole chain: the data, the evaluation protocol, the representation, the models and the candidate generation.

- **Solved a data problem first:** built a **202k-molecule DFT-computed NMR dataset**, a leak-free frozen validation set, and found that rendering spectra as images was silently merging peaks in 89% of the molecules.
- **70% → 91%** exact match of the full fingerprint by moving from a CNN on spectrum images to an **attention model over peak sets** — with **70k parameters** (the original CNN had 8.6M).
- **Uncertainty-guided output:** ~97% of molecules keep the true answer in the candidate set while emitting **1.8 candidates on average instead of 3**.
- Trained on **NVIDIA A10** and ported to **Intel Data Center GPU Max (Clementina XXI)** with numerical-parity tests.

<sub>Code is private (institutional project). The showcase explains the approach, the data work and the results.</sub>

### ⚛️ Relativistic NMR for heavy-atom systems

**OPCW Fellowship at the University of Padova** (Prof. Giacomo Saielli): benchmarking non-relativistic DFT, scalar ZORA and four-component methods for ¹³C and ¹⁵N chemical shifts in molecules bearing Cl, Br and I — the heavy-atom-on-light-atom (HALA) effect — within a thesis built on DP4+-type structural assignment.
Open-source tool: **[nmr-timing](https://github.com/Elpasu/nmr-timing)** — parses ReSpect, ADF/ZORA and Gaussian outputs and compares compute cost in core-hours, stitching restarted runs together automatically.

### 🖥️ HPC & research automation

SLURM across several clusters (CPU, NVIDIA and Intel GPUs) · batch generation and automatic relaunch of thousands of DFT jobs · Telegram notifications for job status · Python GUI tools for NMR tensor extraction with Boltzmann weighting across ReSpect, ADF and Gaussian formats.

### 🤖 Agentic AI workflows

I run research with AI agents as collaborators, not as autocomplete: a persistent project context that encodes rules learned from real bugs, a design spec and implementation plan per experiment, unit and smoke tests before any GPU job, and a results log with decision criteria fixed *before* seeing the numbers. I also built an agent-assisted thesis-writing app on the Anthropic API (Flask + SQLite).

### 📱 Full-stack product: FonoApp · [showcase →](https://github.com/Elpasu/fonoapp-showcase)

Platform for speech-language therapists: patient records, scheduling, session logs, resource library, interactive therapy games, **AI-generated progress reports** and e-invoicing. Next.js + Supabase, **live on iOS and Android**, in beta with practicing therapists. Designed, built and shipped solo.

---

## 🛠️ Tools

**🐍 Languages** Python · Bash · JavaScript/TypeScript · Git

**🧠 Machine learning** PyTorch · NumPy · pandas · h5py · RDKit · Matplotlib · set & attention architectures · uncertainty-aware decoding · experiment design and ablations

**⚛️ Quantum chemistry** Gaussian 16 · ADF (ZORA) · ReSpect (four-component DFT) · DP4+ · relativistic NMR

**🖥️ HPC** SLURM · CUDA (NVIDIA A10) · Intel XPU / oneAPI (Data Center GPU Max 1550) · conda · multi-cluster workflows

**🤖 Agentic AI** Claude Code · Anthropic API · spec → plan → test → run workflows

**🌐 Web & mobile** Next.js · Supabase (PostgreSQL) · Vercel · iOS/Android deployment

**🧰 Desktop tooling** tkinter · openpyxl / Excel automation

## 🎓 Also

- **OPCW Fellowship** — University of Padova, Italy
- **Lecturer** in Physical Chemistry and General Chemistry II — UCA, Rosario

---
---

# Hola 👋 Soy Lucas

**Químico computacional que desarrolla modelos de deep learning para elucidación estructural por RMN** — desde la generación de datos de entrenamiento a escala DFT en clusters HPC hasta los modelos, el protocolo de evaluación y el software que la gente usa.

Doctorando en Ciencias Químicas en la UNR · IQUIR–CONICET (Rosario, Argentina). Trabajo donde se cruzan la química cuántica, el machine learning y la ingeniería de software.
<!-- Cuando defiendas: "Doctor en Ciencias Químicas — UNR · IQUIR–CONICET (Rosario, Argentina)." -->

🔎 **Abierto a** posiciones remotas en química computacional, quimioinformática y ML aplicado a ciencia.

## En qué trabajo

### 🧠 Deep learning: del espectro de RMN a la estructura molecular · [showcase →](https://github.com/Elpasu/nmr-structure-elucidation)

Un modelo lee RMN 2D (HSQC), picos de ¹³C y la fórmula molecular, y predice la **huella de entornos de carbono** de la molécula; esa huella acota un **generador automático de estructuras**, que solo explora estructuras compatibles con los espectros. Armé la cadena completa: los datos, el protocolo de evaluación, la representación, los modelos y la generación de candidatos.

- **Primero resolví un problema de datos:** construí un **dataset de 202 mil moléculas con RMN calculada por DFT**, un set de validación congelado y sin fugas, y detecté que representar los espectros como imagen fusionaba picos en silencio en el 89 % de las moléculas.
- **70 % → 91 %** de acierto exacto de la huella completa al pasar de una CNN sobre imágenes a un **modelo de atención sobre conjuntos de picos** — con **70 mil parámetros** (la CNN original tenía 8,6 millones).
- **Salida guiada por incertidumbre:** ~97 % de las moléculas conservan la respuesta correcta en el conjunto de candidatos, emitiendo **1,8 candidatos en promedio en lugar de 3**.
- Entrenado en **NVIDIA A10** y portado a **Intel Data Center GPU Max (Clementina XXI)** con tests de paridad numérica.

<sub>El código es privado (proyecto institucional). El showcase explica el enfoque, el trabajo sobre los datos y los resultados.</sub>

### ⚛️ RMN relativista en sistemas con átomos pesados

**Beca OPCW en la Universidad de Padua** (Prof. Giacomo Saielli): comparación de DFT no relativista, ZORA escalar y métodos de cuatro componentes para desplazamientos químicos de ¹³C y ¹⁵N en moléculas con Cl, Br e I — el efecto HALA (*heavy atom on light atom*) — dentro de una tesis basada en asignación estructural tipo DP4+.
Herramienta open source: **[nmr-timing](https://github.com/Elpasu/nmr-timing)** — lee salidas de ReSpect, ADF/ZORA y Gaussian y compara el costo de cómputo en core-hours, uniendo automáticamente las corridas relanzadas.

### 🖥️ HPC y automatización

SLURM en varios clusters (CPU, GPUs NVIDIA e Intel) · generación por lotes y relanzamiento automático de miles de cálculos DFT · notificaciones por Telegram del estado de los jobs · herramientas con GUI en Python para extraer tensores de RMN con ponderación de Boltzmann desde ReSpect, ADF y Gaussian.

### 🤖 Flujos de trabajo con IA agéntica

Investigo con agentes de IA como colaboradores, no como autocompletado: un contexto de proyecto persistente con reglas aprendidas de bugs reales, una especificación y un plan de implementación por experimento, tests unitarios y de humo antes de cada job en GPU, y un registro de resultados con criterios de decisión fijados *antes* de ver los números. También desarrollé una app de escritura de tesis asistida por agentes sobre la API de Anthropic (Flask + SQLite).

### 📱 Producto full-stack: FonoApp · [showcase →](https://github.com/Elpasu/fonoapp-showcase)

Plataforma para fonoaudiólogas: fichas de pacientes, agenda, registro de sesiones, biblioteca de recursos, juegos terapéuticos interactivos, **informes de evolución generados con IA** y facturación electrónica. Next.js + Supabase, **publicada en iOS y Android**, en beta con fonoaudiólogas en ejercicio. Diseñada, desarrollada y lanzada por mí.

## 🛠️ Herramientas

**🐍 Lenguajes** Python · Bash · JavaScript/TypeScript · Git

**🧠 Machine learning** PyTorch · NumPy · pandas · h5py · RDKit · Matplotlib · arquitecturas de conjuntos y atención · decodificación con incertidumbre · diseño de experimentos y ablaciones

**⚛️ Química cuántica** Gaussian 16 · ADF (ZORA) · ReSpect (DFT de cuatro componentes) · DP4+ · RMN relativista

**🖥️ HPC** SLURM · CUDA (NVIDIA A10) · Intel XPU / oneAPI (Data Center GPU Max 1550) · conda · flujos multi-cluster

**🤖 IA agéntica** Claude Code · API de Anthropic · flujos spec → plan → test → ejecución

**🌐 Web y mobile** Next.js · Supabase (PostgreSQL) · Vercel · publicación en iOS/Android

**🧰 Herramientas de escritorio** tkinter · openpyxl / automatización de Excel

## 🎓 Además

- **Beca OPCW** — Universidad de Padua, Italia
- **Docente** de Fisicoquímica y Química II — UCA, Rosario
