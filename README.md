# SIR-Epidemic-Modeling
Numerical simulation and analysis of the SIR epidemic model using MATLAB

# SIR Epidemic Modeling

This project uses **MATLAB** to simulate the spread of an infectious disease using the **SIR (Susceptible–Infected–Recovered) model**. The project explores how different infection and recovery rates affect epidemic dynamics, introduces randomness into the model, compares simulations with COVID-19 data from Arizona, and extends the model to include deaths.

## Project Overview

The project is organized into several stages:

1. **Basic SIR Simulation**

   * Define the susceptible, infected, and recovered populations.
   * Solve the SIR system of differential equations using MATLAB's `ode45`.
   * Visualize how each population changes over time.

2. **Parameter Analysis**

   * Change the infection rate \(\beta\) and recovery rate \(\gamma\).
   * Compare how different parameter values affect the size and timing of an outbreak.

3. **Stochastic Simulation**

   * Randomly select infection and recovery rates for each simulation.
   * Run 20 simulations under the same initial conditions.
   * Visualize how uncertainty in model parameters can produce different epidemic outcomes.

4. **Comparison with Arizona COVID-19 Data**

   * Load COVID-19 data from Arizona.
   * Compare the general behavior of the SIR simulation with observed daily case data.
   * Examine how closely the simulated epidemic curve follows the overall pattern of the data.

5. **SIRD Model Extension**

   * Extend the original SIR model by introducing the death as a variable. 
   * Simulate infections, recoveries, and deaths using the expanded SIRD system.
   * Compare simulated infection and death trends with the Arizona data.

## Mathematical Model

The basic SIR model is described by the system

$$
\frac{dS}{dt}=-\beta\frac{SI}{N},
$$

$$
\frac{dI}{dt}=\beta\frac{SI}{N}-\gamma I,
$$

$$
\frac{dR}{dt}=\gamma I.
$$

where:

* \(S\) = susceptible population
* \(I\) = infected population
* \(R\) = recovered population
* \(N\) = total population
* \(β\) = infection rate
* \(γ\) = recovery rate

The basic reproduction number is

$$
R_0=\frac{\beta}{\gamma}.
$$

When \(R_0>1\), an outbreak can grow, while \(R_0<1\) indicates that infections tend to decline.

## Numerical Method

The system of differential equations is solved numerically using MATLAB's `ode45` solver.

Different values of β and γ are tested to study how changes in transmission and recovery affect epidemic behavior.

The stochastic section further introduces uncertainty by randomly selecting parameter values for each simulation.

## Results

The simulations demonstrate that epidemic behavior is highly sensitive to infection and recovery rates.

Higher transmission rates can produce faster and larger outbreaks, while lower transmission rates or higher recovery rates reduce the number of infections.

The stochastic simulations show that different parameter combinations can produce substantially different epidemic curves even when the initial population conditions remain the same.

The comparison with Arizona COVID-19 data shows that the SIR model can reproduce the general rise-and-fall pattern of an epidemic, although the simplified model does not capture all characteristics of real-world disease transmission.

The SIRD extension provides an additional way to model disease-related deaths and illustrates how the basic SIR framework can be expanded to include additional population compartments.

## Technologies

* MATLAB
* `ode45`
* Differential Equations
* Numerical Simulation
* Mathematical Modeling
* Data Visualization

## Files

* `SIR-Epidemic-Modeling Project.mlx` — complete MATLAB Live Script containing the model, simulations, analysis, and figures
* `SIR_Epidemic_Modeling_Report.pdf` — PDF version of the full project report
* `ArizonaData.mat` — COVID-19 data used for the Arizona comparison

## Key Concepts

* SIR epidemic model
* SIRD model
* Ordinary differential equations
* Numerical methods
* Parameter analysis
* Stochastic simulation
* Mathematical modeling
* Epidemic dynamics

## Author

Jiaen Qi

University of California - Irvine

B.S. Applied and Computational Mathematics
