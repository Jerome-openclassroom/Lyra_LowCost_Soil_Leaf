# Low-Cost Soil and Leaf Analysis Protocol for Ecological Monitoring

This project presents a fully operational and low-cost protocol for assessing soil characteristics and green density in plant leaves. Designed for ecological monitoring, educational settings, and citizen science projects, this toolkit combines simple tests and scanner-based digital image analysis.

## Overview

The protocol is divided into two main components:

---

### I. Soil Analysis Protocol

Low-tech but effective methods are used to estimate key soil parameters:

- **Texture**: Using sedimentation test in a Lamotte tube with water and table salt (as a colloidal dispersant).
- **Structure and Structural Stability**: Based on immersion and observation.
- **Organic Matter**: Tested using hydrogen peroxide (H₂O₂) with bubbling indicating presence.
- **Carbonates**: Verified by strong effervescence when in contact with vinegar (20°).
- **Soil pH**: Tested with standard colorimetric strips.
- **Optional parameters**:
  - **pH KCl**: Measured alongside pH H₂O using potassium chloride (food-grade) for estimating exchangeable acidity.
  - **Exchangeable Aluminum**: Recommended in acid forest soils (granite base, conifer dominance).

All these tools are inexpensive, generally available in pharmacies or supermarkets.

---

### II. Leaf Green Density via Scanner

Using a flatbed scanner, leaf surface and green density (DO_green) are measured with precision. This data enables ecological models of plant productivity.

- A plasticized reference green chart was created and field-tested under direct sunlight.
- DO_green values were calibrated with ImageJ using a known gradient.
- Accuracy of visual chart was compared with scanner output: error margins are acceptable for field work.
- Validation of scanner DO_green was performed using SPAD502 (Minolta) readings in the companion repo:
  [Lyra_Leaf_SPAD_Calibration](https://github.com/Jerome-openclassroom/Lyra_Leaf_SPAD_Calibration)

---

## Modeling Primary Production Potential

From the scanner-based dataset, one can estimate a theoretical productivity using the following parameters:

- **Mean green density**
- **Mean leaf area**
- **Mean number of leaves per tree**
- **Mean number of trees per hectare**
- **Target surface (ha)**
- **Integrated solar flux** (W/m² ideally, Lux otherwise)
- **Photosynthesis efficiency (1–2%)**
- **Corrective coefficient** derived from comparison with actual primary net production

$$
P_{model} = DO_{green} \times A_{leaf} \times N_{leaves} \times D_{trees} \times S_{ha} \times I_{sun} \times R_{photo} \times k_{species}
$$

Where \(k_{species}\) is the species-specific empirical correction coefficient.

---

## Repository Structure

- `Calibrations_and_tests`: Calibration files for ImageJ, polynomial fit, example scan of 7 tomato leaves
- `ph_test`: Colorimetric pH test photos
- `Soil_texture`: Photos and results of soil sedimentation test
- `Tests_carbonates`: Vinegar test for carbonates + video of bubbling reaction
- `Tests_H2O2`: Organic matter test with visible foam
- `Visual_chart`: Plastified green chart + 2 field usage examples

---

## Applications

- Pedagogical use (agroecology, BTS GPN, natural sciences)
- Participatory science (community gardens, forest plots)
- Calibration dataset for fine-tuning AI models (Lyra Leaf, Lyra Soil)

This project demonstrates how ecological field monitoring can be democratized using inexpensive tools combined with digital processing and AI guidance.

---

🔗 **Related project**:  
## 🔗 Part of the Lyra Ecosystem

- [Lyra_Leaf_SPAD_Calibration](https://github.com/Jerome-openclassroom/Lyra_Leaf_SPAD_Calibration) – SPAD sensor calibration for estimating chlorophyll density in leaves.
- [TurbiditySensor_OpenScience](https://github.com/Jerome-openclassroom/TurbiditySensor_OpenScience/blob/main/README.md) – Optical-based estimation of aquatic turbidity and primary productivity using open-source sensors.
- [Leaf_Chlorose_CNN_Training](https://github.com/Jerome-openclassroom/Leaf_Chlorose_CNN_Training) – CNN-based classification of chlorotic vs. healthy leaves from scanned images.
- [Lyra_DO_Green_Mesurim](https://github.com/Jerome-openclassroom/Lyra_DO_Green_Mesurim/blob/main/README.md) - A low-tech protocol combining MesurimPro and ImageJ to estimate chlorophyll levels from scanned leaves, with validation against SPAD readings and AI-assisted correlation analysis.
