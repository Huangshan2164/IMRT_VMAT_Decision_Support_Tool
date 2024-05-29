# IMRT and VMAT Decision Support Tool

## Introduction
This document provides a detailed description of the regression model-based decision support tool designed for optimizing intensity-modulated radiation therapy (IMRT) and volumetric modulated arc therapy (VMAT) treatment plans.

## Models
We developed two predictive models, P1 and P2, tailored for IMRT and VMAT plans, respectively.

### P1 Model (IMRT)
- **Variables**: PTV volume, TLV/PTV ratio
- **Equation**:
\[ P1 = \frac{1}{1 + e^{-(−0.816 - 0.513 \cdot \frac{TLV}{PTV} + 0.024 \cdot PTV \; volume)}} \]

### P2 Model (VMAT)
- **Variables**: TLV/PTV ratio, PTV length
- **Equation**:
\[ P2 = \frac{1}{1 + e^{-(−1.442 - 0.522 \cdot \frac{TLV}{PTV} + 0.641 \cdot PTV \; length)}} \]

## Validation
- **Hosmer and Lemeshow Test**: Used to confirm model reliability.
- **ROC Curve Analysis**: Demonstrated the models' effectiveness in predicting treatment plan compliance.

## Measurement Parameters
- **PTV volume**
- **Total Lung Volume (TLV)**
- **TLV/PTV ratio**
- **Total Heart Volume (THV)/PTV ratio**
- **PTV length**

These parameters were measured using the Varian Eclipse TPS.
