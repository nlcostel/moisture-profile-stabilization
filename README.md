# Moisture Profile Control Optimization & Scanner Calibration Case Study

![Reliability Engineering](https://img.shields.io/badge/Discipline-Reliability%20Engineering-blue)
![Process Control](https://img.shields.io/badge/Discipline-Process%20Control-green)
![Instrumentation](https://img.shields.io/badge/Focus-Instrumentation%20%26%20Controls-orange)
![Root Cause Analysis](https://img.shields.io/badge/Method-RCFA-red)
![FMEA](https://img.shields.io/badge/Method-FMEA-yellow)
![Data Analytics](https://img.shields.io/badge/Analysis-Variability%20%26%20Profile%20Analysis-lightgrey)
![Paper Manufacturing](https://img.shields.io/badge/Industry-Pulp%20%26%20Paper-brown)
![Status](https://img.shields.io/badge/Status-Active-success)
![License](https://img.shields.io/badge/License-MIT-black)

## A Reliability Engineering, Process Control, and Data Analytics Project

This repository demonstrates a real-world reliability and process control remediation project, reconstructed with synthetic data and diagrams for confidentiality.
The project showcases root cause analysis, moisture control stabilization, scanner calibration, actuator mapping reconstruction, 
and DCS logic correction on a high-speed manufacturing system.

# 📌 Project Overview

A tissue machine experienced significant moisture profile variability, unstable feedback control, and recurring operator workarounds
due to a combination of instrumentation, control logic, and mapping issues. Core contributing factors included:

            Incorrect CD (cross-direction) actuator mapping to scanner zones

            Secondary scanner calibration drift following a rebuild

            Primary scanner offline due to communication and alignment faults

            Steam box actuators maxing out due to improper limits and biasing

            Basis-weight variation amplifying moisture instability

            Disabled or incorrectly configured DCS alarms

These issues led to:

            High sheet moisture variability

            Quality-related holds and unnecessary downgrades

            Operators running in manual mode due to lack of trust in instrumentation

            Inefficient moisture control and downstream converting issues

            This project applied reliability engineering, control system troubleshooting, data analytics, and 
            calibration methods to restore stable, accurate moisture control.

# 📘 System Background (Sanitized Summary)

The moisture control system includes:

            A primary and secondary moisture scanner providing MD (machine direction) and CD moisture measurements

            A dilution profiling system adjusting local CD basis weight and moisture

            A steam box modulating sheet moisture across multiple zones

            Deckle and edge detection logic defining active sheet width

            DCS PID loops and alarms governing moisture control

            Accurate mapping between actuator zones and scanner bins is essential; misalignment causes inverted or 
            incorrect moisture corrections.

# 🎯 Objectives

Identify root causes of inaccurate CD moisture measurement

Restore correct actuator-to-scanner mapping

Recalibrate moisture scanning equipment

Return steam box and moisture loops to stable automatic control

Reinstate alarm functions supporting closed-loop control

Reduce moisture variability to within target performance limits

# 🔍 Root Cause Analysis (Summary)
✔ Incorrect CD Actuator Mapping

Zones did not match scanner bins, causing inverted or asymmetric profile corrections.

✔ Scanner Calibration Drift

Moisture values deviated significantly from reference samples, leading to inconsistent loop behavior.

✔ Actuator Saturation (“Max-Out”)

Steam box zones could not respond due to incorrectly configured limits and bias terms.

✔ Basis Weight Instability

Upstream BW variation exaggerated moisture swings and masked true moisture deviations.

✔ Disabled / Missing Alarms

Key alarms for moisture deviation and actuator saturation were disabled or mislabeled.

✔ Failure Signatures Observed

            Flatlined CD sections

            Irresponsive zones during bump testing

            Edge misalignment

            Deadband logic preventing actuator movement

            Inaccurate edge trim boundaries

            Drift between scanner measurement and physical samples

# ⚙️ Corrective Actions Implemented
            CD Mapping Reconstruction

            Conducted bump testing on each actuator zone

            Rebuilt the actuator-to-scanner mapping table

            Verified left/right orientation and pitch alignment

            Ensured mapping integrity with synthetic profile tests

            Moisture Scanner Calibration

            Performed moisture curve recalibration

            Corrected deckle configuration errors

            Restored scanner communication & alignment functionality

            Verified MD/CD stability after calibration

            Steam Box & Dilution Profiling Corrections

            Reset actuator limits and removed saturating biases

            Corrected deadband logic

            Returned loops from manual override to automatic

            Ensured full modulation across all control zones

            DCS Logic Improvements (Sanitized Summary)

            Repaired slope/offset calculation issues

            Restored alarm blocks for deviations and actuator saturation

            Corrected labeling inconsistencies for operator displays

            Improved deckle/edge detection logic

            Updated SOPs for scanner outages and calibration workflows

            Data Validation

            Compared before/after CD profiles

            Ran variability calculations (2-sigma, std dev)

            Correlated moisture trends with steam pressure/temp

            Verified moisture accuracy with physical reference samples (method only, data not included)

# 📊 Before & After Trend Snapshot (Redacted)

(Synthetic illustration based on the real project)

Include your redacted trend image here:

/images/moisture_trend_redacted.png


Shows:

      Instability and flatlining before calibration

      Stable, predictable moisture after corrections

# 📈 Results & Performance Improvements

**Metric	Before	After**

CD Moisture 2-Sigma	1.1–1.5%	0.18–0.25%

Steam Box Actuator Behavior	Several maxed	Fully modulating

Loop Stability	Poor	Stable and reliable

Operator Confidence	Low (manual mode)	High (automatic mode)

**Operational Improvements**

            Moisture loop restored to automatic control

            Improved converting performance & downstream quality

            Fewer moisture-related quality events

            Enhanced scanner reliability and measurement accuracy

# 🛠 Methods Used

            Bump testing & response validation

            Scanner calibration and reference sample matching

            Statistical analysis (std dev, sigma, histograms)

            Time-series evaluation of moisture, temp, pressure

            CD profile visualization and comparison

            Root cause analysis (FMEA/RCFA methodology)

            DCS logic review and correction

            Multi-team troubleshooting coordination

# 🧠 Engineering Skills Demonstrated

            Reliability Engineering: FMEA, RCFA, condition monitoring

            Process Control: PID loop tuning, actuator mapping, deadband correction

            Instrumentation: scanner alignment, calibration, signal validation

            Data Analytics: variability analysis, trend analysis, moisture modeling

            Project Leadership: vendor coordination, multi-day troubleshooting, documentation

# 📘 Repository Contents

/data

    synthetic_before_after_cd_profiles.csv

/notebooks

    moisture_profile_variability_analysis.ipynb

/images

    sample_cd_profile_plot.png
    mapping_diagram_generic.png
    moisture_trend_redacted.png

/docs

    sanitized_case_summary.pdf   (optional)

/src

    cd_profile_analysis.py


All datasets and diagrams are synthetic recreations for confidentiality.

# 🔐 Synthetic Data Notice

No proprietary mill data, equipment diagrams, DCS logic, or process details are included.
All values, plots, names, and diagrams have been recreated for public demonstration.

# 🚀 Future Enhancements

            ML-based predictive moisture deviation detection

            DCS loop tuning simulation

            Power BI moisture stability dashboard

            Synthetic steam box digital twin model

# 📫 Contact

Coley Costello

Reliability Engineer • Data Analyst

[LinkedIn Profile] (add your link)

# 📄 License

This project is released under the MIT License.

You may use, adapt, and distribute this content with attribution.
