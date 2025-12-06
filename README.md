<img width="900" height="250" alt="image" src="https://github.com/user-attachments/assets/80ff1307-b163-4d7b-8f79-c814b5721ea0" />



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

            This project applied reliability engineering, control system troubleshooting, 
            data analytics, and calibration methods to restore stable, 
            accurate moisture control.

# 📘 System Background (Sanitized Summary)

The moisture control system includes:

            A primary and secondary moisture scanner providing MD (machine direction) and 
            CD moisture measurements

            A dilution profiling system adjusting local CD basis weight and moisture

            A steam box modulating sheet moisture across multiple zones

            Deckle and edge detection logic defining active sheet width

            DCS PID loops and alarms governing moisture control

            Accurate mapping between actuator zones and scanner bins is essential; 
            misalignment causes inverted or incorrect moisture corrections.

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

*Here is the dilution profile at the start of work:*

<img width="709" height="524" alt="dcs_pre_dpmapping" src="https://github.com/user-attachments/assets/89e4082b-e6f7-45cc-9554-f9aaa87d32e8" />

*And a FLUKE image that shows visibly aggressive streaking:*

<img width="693" height="482" alt="fluke_premapping" src="https://github.com/user-attachments/assets/78517f10-6de4-476f-8fc9-64f010c4f13f" />

*This is the dilution profile when work concluded:*

<img width="698" height="524" alt="dcs_post_dpmapping" src="https://github.com/user-attachments/assets/951417d9-3666-4ba7-bc80-b635ea7d26e8" />

*Confirmed by a FLUKE image that shows a more uniform profile and significantly less streaking:*

<img width="638" height="479" alt="fluke_postmapping" src="https://github.com/user-attachments/assets/1d9abf89-0c11-421a-91c4-ece51790f2b6" />

*Please note that FLUKE was permitted to drift off sheet while completing visual checks, min and max temperatures may not be accurate.*

Shows:

      Instability and flatlining before calibration

      Stable, predictable moisture after corrections

# 📈 Results & Performance Improvements

**Metrics Before & After**

**CD Moisture 2-Sigma:** 

Before: 1.1–1.5% 

After:0.18–0.25%

*In this trend, marker **M1** is pre-work and marker **M2** is post work*

<img width="748" height="426" alt="parcview_reel_moisture" src="https://github.com/user-attachments/assets/3c5f7928-0518-495a-8153-7f2cda573ee2" />


**Steam Box Actuator Behavior**	

Before: Several maxed

After: Fully modulating

**Loop Stability:**

Before: Poor

After: Stable and reliable

*This image references the bump testing completed on the steambox actuators, and shows I correctly positioned them to scanner zones.*

<img width="894" height="395" alt="dcs_steambox_bumptest_results" src="https://github.com/user-attachments/assets/11cc71af-4f1a-4d31-869c-66444302d91d" />

**Operator Confidence:**

Before: Low (manual mode)

After: High (automatic mode)

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

<img width="311" height="637" alt="image" src="https://github.com/user-attachments/assets/4d0429ea-0a76-4917-800d-a50539c91c48" />

All datasets and diagrams are synthetic recreations for confidentiality.

# 🔐 Synthetic Data Notice

## No proprietary mill data, equipment diagrams, DCS logic, or process details are included.
## All values, plots, names, and diagrams have been sanitized for public demonstration.

# 🚀 Future Enhancements

            ML-based predictive moisture deviation detection

            DCS loop tuning simulation

            Power BI moisture stability dashboard

            Synthetic steam box digital twin model

# 📫 Contact

Coley Costello

Reliability Engineer • Data Analyst

# 📄 License

This project is released under the MIT License.

You may use, adapt, and distribute this content with attribution.
