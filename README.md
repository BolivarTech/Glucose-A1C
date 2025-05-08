# Glucose to A1C Conversion and Polynomial Approximation

## Disclaimer

This project is not intended to provide medical advice, diagnosis, or treatment. It is purely a numerical analysis based on publicly available data tables found on the internet. **Always consult a qualified healthcare professional for medical concerns or decisions.**

## Overview
This project analyzes the relationship between blood glucose levels and A1C percentages. It includes data visualization, curve fitting, polynomial approximation, and error analysis to model and simplify the relationship between glucose and A1C.

## Features
- **Data Visualization**: Plots the relationship between glucose and A1C.
- **Curve Fitting**: Fits a quadratic model to the data using `scipy.optimize.curve_fit`.
- **Polynomial Approximation**: Reduces the polynomial order for simplified calculations.
- **Error Analysis**: Calculates and visualizes errors between quadratic and linear approximations.
- **Symbolic Computation**: Uses `sympy` for symbolic polynomial manipulation.

## Requirements
- Python 3.x
- Libraries:
  - `numpy`
  - `pandas`
  - `matplotlib`
  - `scipy`
  - `sympy`

## Usage
1. **Data Preparation**: Ensure the `a1c_glucose` dictionary is populated with glucose and A1C data.
2. **Run the Notebook**: Execute the Jupyter Notebook to:
   - Visualize the data.
   - Fit the quadratic model.
   - Perform polynomial order reduction.
   - Analyze and visualize errors.
3. **Results**: View the plots and printed outputs for insights into the glucose-to-A1C relationship.

## Key Outputs
- **Fitted Parameters**: Coefficients of the quadratic model.
- **Reduced Polynomial**: Simplified linear approximation of the relationship.
- **Error Metrics**: RMSE, standard deviation, and uncertainty percentage.
- **Plots**:
  - Glucose vs. A1C with fitted curves.
  - Error between quadratic and linear approximations.
  - Root squared error visualization.

## Glucose to A1C polynomial approximation

$$
A1C = 0.028099 \cdot \text{glucose} + 2.1748
$$

Where *glucose* is in mg/dL and it is the average of 3 months of glucose readings.  
The resulting value for the *A1C* is in percentage.

## Example
```python
# Example of reduced polynomial
glucose = 120  # Example glucose value
a1c = 0.028099*glucose + 2.1748  # Simplified linear approximation
print(f"Estimated A1C for glucose {glucose} mg/dL: {a1c}%")
```

## License
This project is licensed under the MIT License.