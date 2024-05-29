# Regression Models for IMRT and VMAT

## P1 Model (IMRT)
The P1 model predicts the likelihood of compliance for IMRT plans based on the following logistic regression equation:

\[ P1 = \frac{1}{1 + e^{-(−0.816 - 0.513 \cdot \frac{TLV}{PTV} + 0.024 \cdot PTV \; volume)}} \]

## P2 Model (VMAT)
The P2 model predicts the likelihood of compliance for VMAT plans based on the following logistic regression equation:

\[ P2 = \frac{1}{1 + e^{-(−1.442 - 0.522 \cdot \frac{TLV}{PTV} + 0.641 \cdot PTV \; length)}} \]

## Explanation
- **TLV/PTV ratio**: Ratio of Total Lung Volume to Planning Target Volume.
- **PTV volume**: Volume of the Planning Target Volume.
- **PTV length**: Length of the Planning Target Volume.
