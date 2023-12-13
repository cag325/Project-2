# Modeling shows that the NS5A inhibitor daclatasvir has two modes of action and yields a shorter estimate of the hepatitis C virus half-life

## Background 
Hepatitis C virus is a major health burden in today's World, affecting over 150 million people. This virus often leads to further health complications and is one of the leading causes of liver cancer. Current treatment seeks to target non-structural (NS) viral protein. One of particular interest being NS5A which plays an important role in viral replication and infectious particle release. The aim of this study was to compare the efficacy of daclatasvir, a new NS5A drug target, and the current most common drug to treat HCV IFN- $\alpha$. In addition, this work sought to revise the current working model for viral infection published by Neumann Et. al and establish a new mathematical model for viral infection.   

## Objective 
This project's objective was to replicate the viral dynamic model demonstrated in this paper given their optimized parameters reported in the paper. After which we attempted to generate our own set of optimized parameters to see how they compared to that reported. Following our own parameter optimization we sought to conduct a bifurcation analysis 
## Model and Results of the Paper 
The model demonstrated in this model consists of a system of three ordinary differential equations which can be seen in Figure 1 below. Our work began with attempting to replicate the model with the optimized parameters to the experimental data. In figure 2 we observe the decrease of HCV RNA over time following the admistration of daclastasvir and IFN- $\alpha$. Additionally, we note the quality fit generated from the system of differential equations.  
\
![image](https://github.com/cag325/Project-2/assets/144633699/14287549-125c-4d9f-8342-52bec6f66e21)
\
Figure 1. System of differential equations in the publication to model the viral dynamics of HCV.
\
![image](https://github.com/cag325/Project-2/assets/144633699/7a23e423-3763-4382-bcee-9c4c69f175fe)
\
Figure 2. Plots of HCV RNA decreasing over time following administration of daclastasvir and IFN-\alpha (empty circles). Plots are complemented with the fits generated from the model (solid black lines).

## Replication of Model Published 
Our work began with attempting to replicate the model shown in the paper with their reported optimized parameters. The concluded parameter values were as follows: clearance rate (c) = 23.3 $d^{-1}$, loss rate of infected cells ($\delta$) = 1.06 $d^{-1}$, and effectiveness in blocking viral production ($\epsilon$) = 0.997. However, as seen in the system of differential equations in Figure 1 there are several other parameters needed for this model. The paper referenced previous work that provided the valuing optimized parameters: rate constant of infection ($\beta$) = $3 x 10^{-7}$ $(virion \ per \ milliliter)^{-1} per \ day$, rate of production of virons per cell (p) = 8.3 $d^{-1}$. The only parameter that remained the rate at which target cells were produced. After extensive searching we were unable to identify an explicit value for this parameter but we found that Neumann Et. al reported the growth model invoked had little impact on the model. Thus, we used a logistic growth model $s(t) = T_0e^{kt}$ to represent the rate of target cell production where $T_0$ is the initial number of target cells in the model and k was assumed to be 1. With all these parameters at hand we generated the following model to fit the experimental data (Figure 3). 
\
![image](https://github.com/cag325/Project-2/assets/144633699/d4b28c43-fed1-4c92-a130-5f158a538199)
\
The result above was of fair quality in appearence, however, it differed significantly from that shown in the paper (Figure 1). More specifically, the model reported in the paper appeared to capture the linearity of the experimental data greater than our model had. Therefore, we pursued optimizing our own parameters in an attempt to generate a more accurate model to that of the experimental data.  


