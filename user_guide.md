# User Guide for IMRT and VMAT Decision Support Tool

## Introduction
This guide provides step-by-step instructions on how to use the decision support tool for predicting the compliance of IMRT and VMAT treatment plans.

## Steps

### Step 1: Data Collection
Collect the necessary measurement parameters:
- PTV volume
- TLV
- TLV/PTV ratio
- PTV length

### Step 2: Input Data into the Model
Using the collected data, input the values into the regression equations for P1 and P2 models.

### Step 3: Calculate Prediction Score
Use the following formulas to calculate the prediction scores:

#### P1 Model (IMRT)
\[ P1 = \frac{1}{1 + e^{-(−0.816 - 0.513 \cdot \frac{TLV}{PTV} + 0.024 \cdot PTV \; volume)}} \]

#### P2 Model (VMAT)
\[ P2 = \frac{1}{1 + e^{-(−1.442 - 0.522 \cdot \frac{TLV}{PTV} + 0.641 \cdot PTV \; length)}} \]

### Step 4: Interpretation
The resulting scores from the P1 and P2 models indicate the likelihood of treatment plan compliance. A higher score suggests a higher probability of compliance.

## Example
For demonstration purposes, sample data and calculation steps are provided in the [Sample Data](link-to-sample-data) file.
