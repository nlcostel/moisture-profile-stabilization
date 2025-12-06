# 📌 Project Overview

## A tissue machine experienced significant moisture profile variability, frequent loop instability, and numerous operator workarounds due to:

      Incorrect CD actuator mapping from a lightweighted dilution system

      Inaccurate secondary moisture scanner readings after a rebuild

      A primary scanner offline due to communication and alignment issues

      Steam box actuators operating in manual due to “max-out” conditions

      Basis-weight fluctuations impacting downstream moisture

      Missing or disabled DCS alarms supporting moisture control

## These issues collectively resulted in:

      Poor moisture uniformity across the sheet

      High sheet variability entering converting

      Increased quality holds related to out-of-spec moisture

      Operators running in manual due to lack of trust in instrumentation

      Unnecessary downgrades and efficiency losses

**This project used reliability engineering methods, data analysis, instrument calibration, and DCS logic correction to restore stable moisture control.**

# 🎯 Objectives

1) Identify root causes of inaccurate CD moisture measurement and unstable control.

2) Restore correct mapping between dilution profiling actuators and scanner CD zones.

3) Recalibrate moisture scanning equipment and validate measurement accuracy.

4) Return moisture and steam box loops to automatic control with proper limits and tuning.

5) Establish new operating standards to prevent recurrence.

6) Quantify the variability improvement after corrective actions.

# 🔍 Root Cause Analysis (Summary)
Findings Included:

✔ Incorrect CD Zone Mapping

Actuator zones did not correspond to scanner measurement bins, causing asymmetric or inverted profile corrections.

✔ Scanner Calibration Soft-Failed

Moisture readings drifted significantly from oven-dry reference values, leading to poor control-loop decisions.

✔ Steam Box Maxed Out

Multiple actuators were pinned at upper limits due to improper biasing, making automatic correction impossible.

✔ Basis Weight Variation Upstream

BW swings were amplifying moisture instability and masking scanner inaccuracies.

✔ Disabled / Missing Alarms

Key DCS alarms for moisture deviation and actuator saturation were disabled or improperly configured.

# ⚙️ Corrective Actions Implemented
1. CD Mapping Reconstruction

      Performed systematic bump-testing on each actuator.

      Rebuilt an accurate mapping table correlating actuator index to scanner bin.

      Validated left-right alignment and zone pitch.

2. Moisture Scanner Calibration

      Conducted moisture curve recalibration.

      Corrected deckle-position configuration issues.

      Restored communication and alignment functions.

      Verified MD and CD stability post-calibration.

3. Steam Box & Dilution System Corrections

      Reset actuator limits.

      Eliminated deadbanding conditions.

      Returned systems from manual override to automatic.

      Resolved saturation scenarios preventing control.

4. Data Validation

      Collected before/after moisture profile distributions.

      Performed variability analysis (std dev, 2-sigma, CD uniformity).

      Verified physical sheet samples for moisture accuracy.

5. DCS Logic / Alarm Improvements

      Restored alarm functionality for actuator overload conditions.

      Re-established moisture deviation alarms with correct thresholds.

      Clarified SOPs for operators during scanner outages.

# 📈 Results & Performance Improvements
## Moisture Variability Reduction

CD moisture 2-sigma reduced by ~75–85% after calibration and mapping corrections
(values represented with illustrative data for confidentiality):

## Metric	Before	After

CD Moisture 2-Sigma	1.1–1.5%	0.18–0.25%

Steam Box Actuator Range	Several maxed	Fully modulating

MD/Cross-Direction Stability	Poor	Stable and predictable

Operator Trust in Loop	Low (manual use)	High (automatic use)

## Operational Improvements

Moisture loop fully restored to automatic control.

Sheet quality at converting significantly improved.

Reduction in moisture-related quality events.

Improved scanner reliability and accuracy.

# 🧠 Engineering Skills Demonstrated

## This project showcases capabilities in:

      Reliability Engineering

      Failure Mode & Effects Analysis (FMEA)

      Condition monitoring (moisture, temp, BW)

      Root Cause Failure Analysis (RCFA)

      Instrumentation & Controls

      Profile actuator mapping

      Scanner calibration

      PID loop analysis

      DCS logic validation

      Data Analytics

      Variability reduction analysis

      Profile visualization

      Time-series moisture trend evaluation

      Project Leadership

      Coordination with vendors, process control, E&I, and operations

      Multi-day troubleshooting events

      Delivering corrective action plans and documentation

# 📘 Repository Contents (Public-Safe Materials)
/data

    synthetic_before_after_cd_profiles.csv

/notebooks

    moisture_profile_variability_analysis.ipynb

/images

    sample_cd_profile_plot.png
    mapping_diagram_generic.png

/docs

    sanitized_case_summary.pdf (optional)

/src

    cd_profile_analysis.py


**(All data and diagrams are recreated with synthetic values to protect confidentiality.)**

# 🚀 Future Enhancements

Integrate a predictive moisture deviation alert using ML-based anomaly detection

Add a simulated DCS loop tuning tool

Build a dashboard version of the moisture stability analytics in Power BI

# 📫 Contact

Coley Costello

Reliability Engineer • Data Analyst 

(Insert LinkedIn or professional contact link)

# LICENSE

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

MIT License

This project is licensed under the **MIT License**.  
You are free to use, modify, and distribute this project, provided proper credit is given.


