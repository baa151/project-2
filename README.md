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

The purpose of applying bifurcation analysis is to gain deep insights into the qualitative changes and transitions that occur in the dynamics of a system as a parameter is varied. I chose this parameter because I was curious on how the period of time for a person to be contagious would affect the dynamics of the model.

<p align="center">
  <img src="https://github.com/baa151/project-2/assets/123330888/3a656b16-08e7-4db0-a6ed-46798a48db80" height="450"> <br>
</p>

The reason I chose $\tau_R$ from [1,14] is because I read from a different paper that a person can still transmit the infection for more than 10 days.
As the infection time is small, lets say 2 days, this individual is able to transmit the virus for two days only, the number of recovered cases slightly decreases. And as that time increases, which means that this person is contagious for a longer period of time, he can transmit the infection for more people.
