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


I tried to get a similar fit to the papers fit but the problem is, they used a range of numbers for their parameters and not a specific value. The papers fit for a data is shown below : 


<p align="center">
  <img src="https://github.com/baa151/project-2/assets/123330888/5d8edf39-bdbb-4753-9378-3baebe43a2f9" width="450"><br>
</p>

Data sets collected from https://www.worldometers.info/coronavirus/country/Ireland/ and https://covid19ireland-geohive.hub.arcgis.com/ for Ireland over a period of about 200 days in 2020.

My optimized fit compared to the papers fit is shown below : 

<p align="center">
  <img src="https://github.com/baa151/project-2/assets/123330888/8cf2950f-9d49-4b61-8b35-3c8e8243f1ec" height="450"> <br>
</p>

With assuming that the paper's parameters:

$\tau_r$  = 4.9  

$\tau_I$ = 14

My optimized parameters are :

$\tau_r$  = 5.592 

$\tau_I$ = 17.091

Comparing both results, it can be seen that both can fit the data for a certain extent but their fit looks like it is shifted to the left with time ranges of [100,160].

# Bifurcation Analysis

The purpose of applying bifurcation analysis is to gain deep insights into the qualitative changes and transitions that occur in the dynamics of a system as a parameter is varied. I chose this parameter because I was curious about how the period of time a person remains contagious would affect the model's dynamics.

<p align="center">
  <img src="https://github.com/baa151/project-2/assets/123330888/3a656b16-08e7-4db0-a6ed-46798a48db80" height="450"> <br>
</p>

I chose the parameter $\tau_R$ to vary within the range of [1, 14] because, based on information from another study, individuals can potentially transmit the infection for more than 10 days. When the infection time is short, let's say 2 days, the individual can transmit the virus for a limited period, resulting in a slight decrease in the number of recovered cases. Conversely, as the infection time increases, signifying a longer contagious period, the individual has the potential to transmit the infection to a larger number of people.

# Sensitivty Analysis

Moving on to Sensitivty analysis, to identify the parameters to which the output is most sensitive !! 
Starting with local sensitivity analysis: 
I tried to perturb my parameters by 5% to see how can this affects my model :

<p align="center">
  <img src="https://github.com/baa151/project-2/assets/123330888/a7d90c52-2b48-4f43-8447-07bd8f16f0a3" height="450"> <br>
</p>

<p align="center">
  <img src="https://github.com/baa151/project-2/assets/123330888/6d1296e2-9a92-401e-b922-1e1efc065075" height="450"> <br>
</p>

It can be seen that $\tau_I$ affects the system more.

Also, I double-checked these results with applying Global sensitivty analysis by applying perturbation the parameters by ±20% :

<p align="center">
  <img src="https://github.com/baa151/project-2/assets/123330888/ef01f99d-c9bd-458f-9fe9-c3ad41e95c97" height="450"> <br>
</p>

<p align="center">
  <img src="https://github.com/baa151/project-2/assets/123330888/fd7b2456-0e0a-4650-bb3b-db071799ab5c" height="450"> <br>
</p>
