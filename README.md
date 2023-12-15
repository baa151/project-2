# project-2

## APA citation of the paper :
Sebastião, P. J., Beira, M. J., Cordeiro, R., Kumar, A., Fernandes, J. C., Ferraz, A., & Gonçalves, L. N. (2022). The art of fitting ordinary differential equations models to experimental results. European Journal of Physics, 43(3), 035807. DOI 10.1088/1361-6404/ac563a

This work aims for an improvement ( if possible ) on the above paper. This paper introduces an approach for fitting ordinary differential equation (ODE) models to experimental results. It addresses situations where traditional statistical estimators fall short, and analytical solutions are unavailable. The method involves solving ODEs numerically and fitting the results to experimental data, providing meaningful parameter sets. The paper showcases a user-friendly web-based ODE solver and fitter, demonstrating its application in analyzing a rigid pendulum's motion and the dynamics of a viral infection (our intreset). Overall, the paper presents a practical and accessible solution for researchers and students across diverse academic levels and fields.

The model they used was the extended SIR model which represents the population into three categouries : Susceptible, Infected and Recovered.
<p align="center">
  <img src="https://github.com/baa151/project-2/assets/123330888/1f234564-925d-4776-8a84-8ea0f7c22913" width="300"><br>
</p>

n : Daily new cases

T : Total number of cases

$\tau_I$ : (Infection time) : Average duration it takes for an infected individual to be able to transmit the infection to a susceptible individual.

$\tau_R$ : (Recovery time) :  Average duration an individual remains infected before recovering. 

with initial conditions as shown below : 

<p align="center">
  <img src="https://github.com/baa151/project-2/assets/123330888/1044d81d-2e1c-4f6a-82b5-d18289797700" width="450"><br>
</p>


I tried to get a similar fit to the papers fit but the problem is, they used a range of numbers for their parameters and not a specific value. The papers fit is shown below : 


<p align="center">
  <img src="https://github.com/baa151/project-2/assets/123330888/5d8edf39-bdbb-4753-9378-3baebe43a2f9" width="450"><br>
</p>

My optimized fit compared to the papers fit is shown below : 

<p align="center">
  <img src="https://github.com/baa151/project-2/assets/123330888/8ada3f91-dde2-47ac-8b35-2a842e548c2f" width="350"><br>
</p>

