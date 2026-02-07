# FLUX-GEO  
**Multiphase Flow and Transport Modeling for Subsurface Energy and Storage Systems**

---

## Executive Summary

**FLUX-GEO** is a computational modeling framework for subsurface flow and transport across energy, environmental, and storage applications. It integrates multiple, well-established subsurface simulators—including **PFLOTRAN**, **FEHM**, **MODFLOW**, **VS2DI**, and **VS2DTI**—within a unified, Python-driven workflow. The framework enables consistent model setup, execution, postprocessing, and reporting across solvers while preserving the unique physical strengths and numerical formulations of each code.

FLUX-GEO delivers **reproducible and traceable simulation packages**, operational scenarios with explicit physical and engineering constraints, and **decision-ready outputs** that support subsurface system design, performance assessment, monitoring strategy development, and technical review. By emphasizing physical realism, transparent assumptions, and rigorous QA/QC, FLUX-GEO enables robust evaluation of **pressure evolution, multiphase flow, plume migration, transport processes, trapping mechanisms, reactive behavior, and long-term system performance**.

FLUX-GEO is intentionally designed as a **general-purpose subsurface modeling framework**. It supports a broad range of applications, including **geologic CO₂ storage and carbon management**, **groundwater flow and contaminant transport**, **geothermal and coupled thermal–hydrologic systems**, **hydrogen and other gas storage**, **energy and waste isolation**, and **near-field and variably saturated processes**. This breadth allows FLUX-GEO to be applied consistently across diverse subsurface problems while maintaining solver-appropriate physics and defensible, transparent assumptions.


---

## Supported Numerical Engines

FLUX-GEO is designed to work across multiple subsurface flow and transport simulators, each applied where its physics and numerical strengths are most appropriate.

- **PFLOTRAN**  
  Multiphase CO₂–brine flow, reactive transport, geochemical coupling, and large-scale reservoir simulations.

- **FEHM**  
  Multiphase flow, heat transport, and coupled thermal–hydrologic processes, particularly for systems with strong thermal or energy coupling.

- **MODFLOW (and MODFLOW-family tools)**  
  Saturated groundwater flow and pressure evolution, including density-coupled and transport extensions when appropriate.

- **VS2DI / VS2DTI**  
  Variably saturated flow and transport, near-field processes, leakage pathways, and infiltration-dominated systems.

Python serves as the integration layer, providing a consistent interface for scenario definition, execution control, output parsing, QA/QC, and reporting across all solvers.

---

## Capabilities

### Multiphase CO₂ Flow (CO₂–Water / sCO₂)

FLUX-GEO supports modeling of CO₂ injection and long-term multiphase evolution using solver-appropriate physics.

#### What We Can Do
- Injection scenarios with pressure buildup and plume migration  
- Buoyancy-driven flow and containment behavior  
- Salinity- and temperature-dependent variants where they materially affect results  

**Primary engines:** PFLOTRAN, FEHM  
**Supporting engines:** MODFLOW (density-aware extensions)

---

### Wells and Operations

FLUX-GEO represents coupled wells and operational controls under realistic engineering constraints.

#### What We Can Do
- Well injection and production scheduling, including WAG and brine extraction strategies  
- Constraint evaluation (fracture pressure limits, minimum pressure thresholds, bottom-hole pressure limits)  
- Well performance summaries and field-level key performance indicators (KPIs)  

**Primary engines:** PFLOTRAN, FEHM  
**Supporting engines:** MODFLOW well packages, Python-based operational logic

---

### Reactive Transport and Mineralization

When permanence and geochemistry are critical, FLUX-GEO incorporates reactive transport and geochemical bookkeeping.

#### What We Can Do
- Coupled flow, transport, and geochemistry for CO₂ partitioning  
- Tracking of CO₂ into mobile/free-phase, dissolved, and mineralized fractions  
- Mass-balance-based KPIs with explicitly stated assumptions and limitations  

**Primary engines:** PFLOTRAN  
**Supporting workflows:** Python-driven reaction tracking and postprocessing

---

### Variably Saturated Flow and Near-Field Processes

FLUX-GEO supports near-field and unsaturated-zone modeling where capillary effects and partial saturation dominate behavior.

#### What We Can Do
- Variably saturated flow and transport simulations  
- Infiltration, leakage, and near-surface process representation  
- Consistent comparison with saturated-flow and reservoir-scale models  

**Primary engines:** VS2DI, VS2DTI  
**Integration layer:** Python-based preprocessing and postprocessing

---

### Post-Processing, KPIs, and Reporting

FLUX-GEO converts raw simulator outputs into consistent, decision-ready products across all supported solvers.

#### What We Can Do
- Automated plots for pressure evolution, plume footprint proxies, and well behavior  
- CO₂ mass partitioning summaries through time  
- Cross-solver KPI comparison (pressure, plume extent, trapping and storage metrics)  
- Clear, reviewable documentation and run logs suitable for technical and regulatory review  

---

### Reproducibility and QA/QC

FLUX-GEO deliverables are designed to be rerun, audited, and extended across modeling engines.

#### What We Can Do
- Reproducible run packages (inputs, execution instructions, and standardized plots)  
- QA/QC checks including mass balance, timestep stability, and solver diagnostics  
- Versioning and change tracking for iterative projects  
- Explicit documentation of solver-specific assumptions and limitations  

---

## Deliverables

Deliverables scale with data availability and project goals, from rapid feasibility screening to site-scale and permanence analyses.

---

### Deliverable Set A — Rapid Screening (2–4 Weeks)

#### Deliverables
- Screening models sized to available information (injectivity, pressure buildup, first-order plume behavior)  
- Sensitivity results for dominant parameters (e.g., permeability, relative permeability, salinity/temperature assumptions)  
- Concise PDF report summarizing assumptions, results, and recommended next steps  

---

### Deliverable Set B — Site Concept Model (6–12 Weeks)

#### Deliverables
- Site-scale model setup (initialization, boundary conditions, stratigraphy, heterogeneity representation)  
- One or more well configurations and schedules with constraint checks  
- Decision outputs including pressure envelopes, plume evolution, and trapping diagnostics  
- Reproducible model package with run instructions and standardized plots  

---

### Deliverable Set C — Mineralization and Permanence Analysis (6–12 Weeks)

#### Deliverables
- Chemistry configuration (species, minerals, reaction rates, database selection)  
- CO₂ partitioning versus time (mobile gas, dissolved, mineralized)  
- Permanence KPIs suitable for technical narratives, with explicit assumptions and limitations  

---

### Deliverable Set D — MRV-Ready Model Package (Ongoing)

#### Deliverables
- Standard QA/QC checklist and run log for each update  
- Versioned scenario library with consistent reporting format  
- Monitoring implications highlighting measurements that most constrain plume and pressure behavior  

---

## Why This Is Valuable

FLUX-GEO converts site data and operational goals into testable scenarios with traceable assumptions, quantitative KPIs, and repeatable simulation packages. By supporting **PFLOTRAN, FEHM, MODFLOW, VS2DI, and VS2DTI within a single, coherent workflow**, FLUX-GEO reduces uncertainty, improves cross-model consistency, and enables clear communication with technical stakeholders, sponsors, and reviewers.

---

## License

*License to be defined.*

---

## Citation

If you use **FLUX-GEO** in research, proposals, or technical studies, please cite appropriately. Citation details for FLUX-GEO will be provided in a future release. Users are responsible for citing underlying numerical engines (**PFLOTRAN, FEHM, MODFLOW, VS2DI, VS2DTI**) according to their respective guidelines.
