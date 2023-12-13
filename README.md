# Modeling shows that the NS5A inhibitor daclatasvir has two modes of action and yields a shorter estimate of the hepatitis C virus half-life

## Background 
Hepatitis C virus is a major health burden in today's World, affecting over 150 million people. This virus often leads to further health complications and is one of the leading causes of liver cancer. Current treatment seeks to target non-structural (NS) viral protein. One of particular interest being NS5A which plays an important role in viral replication and infectious particle release. The aim of this study was to compare the efficacy of daclatasvir, a new NS5A drug target, and the current most common drug to treat HCV IFN-$alpha$. In addition, this work sought to revise the current working model for viral infection published by Neumann Et. al and establish a new mathematical model for viral infection.   

## Objective 
This project's objective was to replicate the viral dynamic model demonstrated in this paper given their optimized parameters reported in the paper. After which we attempted to generate our own set of optimized parameters to see how they compared to that reported. Following our own parameter optimization we sought to conduct a bifurcation analysis 
## Model and Results of the Paper 
The model demonstrated in this model consists of a system of three ordinary differential equations which can be seen in Figure 1 below. Our work began with attempting to replicate the model with the optimized parameters to the experimental data. In figure 2 we observe the decrease of HCV RNA over time following the admistration of daclastasvir and IFN-\alpha. Additionally, we note the quality fit generated from the system of differential equations.  
\
![image](https://github.com/cag325/Project-2/assets/144633699/14287549-125c-4d9f-8342-52bec6f66e21)
\
Figure 1. System of differential equations in the publication to model the viral dynamics of HCV.
\
![image](https://github.com/cag325/Project-2/assets/144633699/7a23e423-3763-4382-bcee-9c4c69f175fe)
\
Figure 2. Plots of HCV RNA decreasing over time following administration of daclastasvir and IFN-\alpha (empty circles). Plots are complemented with the fits generated from the model (solid black lines).

## Replication of Model Published 
Our work began with attempting to replicate the model shown in the paper with their reported optimized parameters. The concluded parameter values were as follows: clearance rate (c) = 23.3, $\delta $ =


