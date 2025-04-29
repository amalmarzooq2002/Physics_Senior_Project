# Senior Project: *Characterization of Geomagnetic Pulsations in Corroboration with the Solar Wind Parameters*

**Author:** Amal Marzooq  
**Institution:** University of Bahrain  
**Supervisor:** Prof. Aswini Kumar Sinha  
**Degree:** B.Sc. in Physics
**Academic Year:** 2024

---

## Overview

This project, titled *"Characterization of Geomagnetic Pulsations in Corroboration with the Solar Wind Parameters"*, is submitted in partial fulfillment of the requirements for the Bachelor of Physics degree. It explores the key parameters affecting the generation one of the important tools (i.e. geomagnetic pulsations) of the magnetosphere diagnostics.

## Objectives

- To investigate geomagnetic pulsations (ULF waves) as indicators of magnetospheric response to solar wind disturbances.
- To analyze the observational link between solar wind conditions and geomagnetic activity during an intense solar storm.
- To study the distribution of continuous pulsations (Pcs) across selected equatorial stations.
- To correlate Pc pulsations with solar wind parameters (IMF, velocity, pressure, temperature).
- To contribute to understanding the generation mechanisms of equatorial Pcs, which remain poorly understood.



## Tools & Technologies

- Programming Language: Python
- Libraries: NumPy, Pandas, SciPy, Matplotlib.
- Data Sources: NTERMAGNET, WDC for Geomagnetism, OMNIWeb.

## Methodology

### Coordinate Systems
Two IAGA-recommended systems are used:
- **XYZ**: X (Geographic North), Y (East), Z (Down).
- **HDZ**: H (Horizontal intensity), D (Declination angle), Z (Down).

Conversions:
- X = H·cos(D), Y = H·sin(D), D = arctan(Y/X), H = √(X² + Y²)

### Magnetic Local Time (MLT)
MLT relates UT to solar time:
- MLT = UT + (φ + Φ_N)/15


### Geomagnetic Indices
- **Kp**: Global 3-hour magnetic disturbance scale.
- **Dst**: Hourly equatorial storm strength.
- **AU/AL/AE**: Auroral electrojet indices (AE = AU − AL).

### Data Selection
Data from 4 INTERMAGNET stations (GUA, DLT, ASC, KOU) from March 14–18, 2015. Sampling rate: 1 Hz. Only frequencies < 0.5 Hz are analyzed (Pc3–Pc5, Pi2).

### Filtering & Spectral Analysis
- Butterworth filter (order 4).
- STFT: `fs=1 Hz`, `nfft=512`, `noverlap=230`.

### Pulsation Extraction
Pulses (≥3 cycles) recorded if:
- Pc3 ≥ 0.1 nT, Pc4 ≥ 0.3 nT, Pc5 ≥ 0.5 nT.
Midpoint used to assign Kp and MLT.

### Solar Wind Fitting
Solar wind data from OMNIWeb.  
Welch method applied hourly (512-point segments) using:


## Citation

If you'd like to cite this project, please use:

```bibtex
@thesis{marzooq2025senior,
  author = {Amal Marzooq},
  title = {Characterization of Continuous Geomagnetic Pulsations},
  school = {University of Bahrain},
  year = {2025},
  type = {Bachelor's Thesis}
}


