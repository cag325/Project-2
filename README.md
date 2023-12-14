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
Figure 2. Plots of HCV RNA decreasing over time following administration of daclastasvir and IFN- $\alpha$ (empty circles). Plots are complemented with the fits generated from the model (solid black lines).

## Replication of the Published Model and Generation of Our Own Model  
Our work began with attempting to replicate the model shown in the paper with their reported optimized parameters. The concluded parameter values were as follows: clearance rate (c) = 23.3 $d^{-1}$, loss rate of infected cells ($\delta$) = 1.06 $d^{-1}$, and effectiveness in blocking viral production ($\epsilon$) = 0.997. However, as seen in the system of differential equations in Figure 1 there are several other parameters needed for this model. The paper referenced previous work that provided the valuing optimized parameters: rate constant of infection ($\beta$) = $3 x 10^{-7}$ $(virion \ per \ milliliter)^{-1} \ per \ day$, rate of production of virons per cell (p) = 8.3 $d^{-1}$. The only parameter that remained the rate at which target cells were produced. After extensive searching we were unable to identify an explicit value for this parameter but we found that Neumann Et. al reported the growth model invoked had little impact on the model. Thus, we used a logistic growth model $s(t) = T_0e^{kt}$ to represent the rate of target cell production where $T_0$ is the initial number of target cells in the model and k was assumed to be 1. With all these parameters at hand we generated the following model to fit the experimental data (Figure 3). 
\
![image](https://github.com/cag325/Project-2/assets/144633699/d4b28c43-fed1-4c92-a130-5f158a538199)
\
Figure 3. Attempt to replicate the model reported by Guedj Et. al. 
\
The result above was of fair quality in appearence, however, it differed significantly from that shown in the paper (Figure 1). More specifically, the model reported in the paper appeared to capture the linearity of the experimental data greater than our model had. Therefore, we pursued optimizing our own parameters in an attempt to generate a more accurate model to that of the experimental data. We sought to optimize the parameters explicitly reported in the paper and none of those we found in the supporting reference papers because the parameter space would exceed the number of equations in our model. Our optimized parameters were as followed: clearance rate (c) = 22.3 $d^{-1}$, loss rate of infected cells ($\delta$) = 1.17 $d^{-1}$, and effectiveness in blocking viral production ($\epsilon$) = 0.488.Our resulting model was very similar in structure to the model we attempted to reconstruct and the error margins relative to the experimental data were also similar (Figure 4).   
\ 
![image](https://github.com/cag325/Project-2/assets/144633699/6410bdcf-79f3-4bbc-a5c5-23fb5604abc5)
\
Figure 4. Generation of our own model with differing optimized parameters.
\
#### Conclusion 1: We were unsuccessful in reconstructing the publish model using either the reported parameters or optimized parameters of our own. While neither model was ideal both appeared to be of resonable quality and demonstrated relatively sufficient accuracy to the experimental data. 


## Sensitivity Analysis
The last component of this work was to perform a sensitivity analysis on the collection of parameters in the model. We began with the local sensitivity analysis and perturbed each parameter by 5% to gain insight into the sensitivity the model has with respect to each parameter. We observed small deviations in the model upon perturbations of $d, \delta, s, \beta, and \ p$ (Figure 5). While the more significant deviations were observed when perturbations were induced to $c$ and $\epsilon$. For the ease of interpretation the local sensitivity results were plot in manner such that sensitivity of $V$ can be seen as a function of each parameter (Figure 6). In this figure one can more clearly see how influential clearance rate and drug effectiveness factor are on the viral volume.   
\
![image](https://github.com/cag325/Project-2/assets/144633699/43a337d8-ce85-4395-8ac5-57536f0ddd35)
\
Figure 5. Local Sensitivity Analysis of the influence of the parameter values on the model. (Note each parameter was perturbed by 5% of their reported value)
\
![image](https://github.com/cag325/Project-2/assets/144633699/d003d161-12b9-4ff9-a423-40c662fb30bc)
\
Figure 6. Sensitivity of the Viral Volume as a function of each parameter. (Continuation of the Local Sensitivity Analysis)
\
\
The analysis then shifted from a local perspective to a global perspective. Thus, we conducted a global sensitivity analysis to understanding the effects large perturbations have on the viral volume. The global sensitivity analysis was conducted twice, once on all seven parameters and again with a focus on the three parameters we previosuly sought to further optimize. Here we will discuss the global sensitivity analysis focues on the parameters $c, \epsilon, and \delta$. With perturbations of these three parameters by +/- 20% we notice an abundance of changes in the viral volume model (Figure 7). The construction of a parity plot from a linear regression analysis illustrated that large changes of the $\delta$ parameter had the greatest influence on the viral volume as shown by the magnitude of the coefficient in the linear equation (Figure 8). The parameters $c$ and $\epsilon$ had a very comparable influence on the global sensitivity.  
\
![image](https://github.com/cag325/Project-2/assets/144633699/f4c049e9-1746-439d-9095-8dedd00700ca)
\
Figure 7. Global Sensitivity Analysis (Perturbations only to $c, \ \epsilon, \ and \ \delta$)
\
![image](https://github.com/cag325/Project-2/assets/144633699/0f5cd3a0-2068-48e6-9902-dcbab3991de1)
\
\
Figure 8. The parity plot following the global sensitivity analysis and the resulting linear equation from normalized linear regression analysis.
\
#### Conclusion






