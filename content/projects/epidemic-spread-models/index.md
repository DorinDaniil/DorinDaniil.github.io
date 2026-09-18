---
title: "Epidemic spread models: COVID-19 as stochastic chemical kinetics"
weight: 40
year: 2023
cover: sir.png
coverContain: true
summary: Various approaches to modeling the spread of epidemics, in particular COVID-19, through differential equations and Markov processes. Deterministic and stochastic SIR models fitted to real multi-wave data.
tags: [epidemiology, ODE, Markov processes]
links:
  - name: GitHub
    url: https://github.com/DorinDaniil/Epidemic-Spread-Models
    icon: github
  - name: Report
    url: https://github.com/DorinDaniil/Epidemic-Spread-Models/blob/main/paper.pdf
    icon: paper
  - name: Slides
    url: https://github.com/DorinDaniil/Epidemic-Spread-Models/blob/main/slides.pdf
    icon: slides
---

Various approaches to modeling the spread of epidemics, in particular COVID-19, are studied: the classical SIR model as a system of ordinary differential equations, and its stochastic counterpart formulated as a model of stochastic chemical kinetics, where infections and recoveries are Markov jump processes. The models are fitted to observed case counts and used to reproduce several consecutive epidemic waves.

Joint work with Peter Babkin, Nikita Kiselev, Matvei Kreinin and Maria Nikitina, December 2023.

![Deterministic SIR model: susceptible, infected and recovered fractions over time.](sir.png)

![Stochastic SIR model: sample trajectories of the Markov jump process.](stochastic_sir.png)

![Stochastic SIR fitted to three consecutive epidemic waves.](three_waves.png)
