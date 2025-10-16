#PlotSense Plugin Pack: Extending Plot Generation with Heatmaps, Line Plots & Correlation Analysis  
**Plotsense Hackathon Submission — Track 2 (PlotSense Dev)**  

**User ID:** `PSH2025-722`  
**Track:** PlotSense Dev  
**Team Name:** Remz  

---

## Project Description  

The core PlotSense library provides intelligent plot recommendations, automatic plot generation, and natural-language explanations.  
However, it was missing some essential analytical visualization types that are commonly used in exploratory data analysis.

This contribution introduces a **plugin pack** that extends PlotSense with **three powerful visualization capabilities**:  
- ✅ **Heatmap Generator** – visualize correlations and feature relationships in a compact, interpretable way.  
- ✅ **Line Plot Generator** – analyze trends across time or continuous variables.  
- ✅ **Correlation Analysis Plot** – compute and visualize feature correlations automatically.  

The plugins are designed to be registered seamlessly, **without modifying the PlotSense core source code** — following a clean, plug-and-play architecture.

---

## What We Did  

### 1️ Designed a Plugin Registration System  
We added a single function to handle **automatic plugin registration** from a `/plugins` folder.  
This allows users to drop in any new visualization module and have it integrated instantly into PlotSense’s plot generation workflow.

### 2️ Implemented Three New Plot Types  

Each plugin is implemented as a **separate Python file** inside the `plugins/` directory:

- **`heatmap_plugin.py`** → Uses seaborn to create feature-correlation heatmaps.  
- **`lineplot_plugin.py`** → Generates clean, customizable line plots.  
- **`correlation_plugin.py`** → Computes correlations and visualizes key relationships between numerical features.  

This modular design allows new plots to be added simply by dropping a `.py` file with a proper interface into the folder.

---

### 3️ Integrated with PlotSense Workflow  

Once registered, these new plots become **first-class citizens** in PlotSense:

- They are accessible through the same `PlotGenerator` interface.  
- They work seamlessly with the existing `recommender` and `explainer` pipeline.  
- Users don’t need to change their workflow — just call `plotgen(...)` and go.

## Why This Matters  

- **Broader Visualization Coverage** — Heatmaps and line plots are core EDA tools used in almost every data science workflow.  
- **Developer Extensibility** — Encourages a plugin ecosystem for PlotSense, enabling the community to build and share new plot types without touching the core source.  
- **Seamless User Experience** — Works exactly like built-in plots, keeping PlotSense’s API simple and intuitive.

---

## Tech Stack  

- **Languages & Libraries:** Python, Matplotlib, Seaborn, Pandas  
- **Framework:** PlotSense (extended via custom plugins)  
- **Dev Focus:** Modular plugin architecture, automatic registration, non-intrusive integration  

---

## 👥 Team Members  

| Name              | Role                        |
|-------------------|-----------------------------|
| Diugwu Izudiugwu  | Developer / Plugin Engineer |

---

## 🔗 Social Media  

- [Twitter/X Post](https://x.com/DiugwuIzuchukwu/status/1978962867069014212)  
- [LinkedIn Post](https://www.linkedin.com/posts/diugwu-izuchukwu-2977a6286_it-took-me-a-while-to-decide-on-what-to-build-activity-7384732504550809600-Fbi7?utm_source=social_share_send&utm_medium=member_desktop_web&rcm=ACoAAEWHSBMB-pkPplnmc1Hq5QY73du73kv2_NE)

## 🎥 Demo Video  

[Demo Video Link](https://drive.google.com/file/d/1wrYPjxhOc6itMDN49V4SS66Kr-D_v86_/view?usp=sharing)  


---

## Acknowledgement  

This contribution was built as part of the **PlotSense Hackathon 2025 (Track 2)**.  
It enhances the PlotSense ecosystem by introducing a **plugin architecture** and extending the library with essential visualizations — enabling faster and richer exploratory data analysis for developers and data scientists.

