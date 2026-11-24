# Column Buckling — Model vs. Test & Full 2D Drawing

An interactive **Google Colab** tool built with `ipywidgets`, `NumPy`, and `Matplotlib` to evaluate axial column buckling for **Paper**, **Balsa Wood**, and **3D-Printed PLA** columns and compare experimental/measured loads against a simple analytical buckling model.

## Overview

Slender columns subjected to axial compression can buckle laterally well below direct material crushing limits. This notebook lets you select a column material, cross-section geometry, and end boundary condition, estimate or enter an experimental load ($P_{\text{exp}}$), compare it with a simple Euler/compression model ($P_{\text{model}}$), and inspect the 2D buckled column and cross-section drawings.

### Supported Materials & Cross-Sections
- **Materials:** `Paper`, `Balsa Wood`, `3D-Printed PLA`
- **Cross-Sections:** `Hollow Tube`, `Rectangular Strip`, `Solid Square`
- **End Conditions:** `Pinned-Pinned (K=1.0)`, `Fixed-Pinned (K=0.7)`, `Fixed-Fixed (K=0.5)`, `Cantilever (K=2.0)`

## Key Features

- **Interactive Controls (`ipywidgets`):** Select material, section geometry, end support, length, section dimensions, and experimental load (`P_exp`), or populate a realistic reference test load with one click.
- **Load Comparison Bar Chart:** Compares the simple theoretical model load against the experimental load and reports percentage difference and effective slenderness ($K \cdot L / k$).
- **Full 2D Column & Cross-Section Views:** Displays the column along its height with boundary/buckled mode behavior alongside the 2D cross-sectional geometry.
- **Difference & Physical Cause Summary:** Explains why real test results can differ from ideal Euler theory (such as initial crookedness, load eccentricity, fixture compliance, and material/manufacturing effects).

## How to Run in Google Colab

1. Open a new notebook in [Google Colab](https://colab.research.google.com/).
2. Paste the code cell into the notebook and run it.
3. Adjust the controls or click **Fill Realistic P_exp** / **Update Chart & 2D Drawing** to explore different cases.

## Engineering Notes

- The simple model evaluates Euler critical buckling load $P_{\text{cr}} = \frac{\pi^2 E I}{(K L)^2}$ alongside direct compressive capacity $\sigma_c A$.
- Real test behavior depends on setup alignment, end support stiffness, and material/manufacturing variability, so physical test data and FEA provide valuable complementary insight.
