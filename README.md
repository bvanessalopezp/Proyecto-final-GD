[![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=bvanessalopezp/Proyecto-final-GD)

# Final Project:  mathematical model of cardiac cycle

## Información de la estudiante
Brianna Vanessa Lopez Pardo \[22212261]; L22212261@tijuana.tecn.mx

Gemelos Digitales

Ingeniería Biomédica

## Docente
Dr. Paul Antonio Valle Trujillo; paul.valle@tectijuana.edu.mx

Departamento de Ingeniería Eléctrica y Electrónica, Tecnológico Nacional de México/IT Tijuana, Blvd. Alberto Limón Padilla s/n, Tijuana, C.P. 22454, B.C., México

# Course Description

The Digital Twins course is part of the Biomedical Engineering curriculum with the following general course competency: Formulates the digital twin through experimental data for the development of control strategies using nonlinear dynamic systems theories and in silico experimentation. This course aims to provide the Biomedical Engineer with the capacity to conduct scientific research in the area of Systems Biology, with the purpose of leading and participating in interdisciplinary work teams in national and international contexts, as well as providing computational solutions to solve problems in the field of Biomedical Engineering with professional ethics.
In the context of dynamic systems describing biological or physiological systems, in silico modeling is a logical extension of controlled in vitro experimentation. It is the natural result of the dramatic increase in computational power available at a continuously decreasing cost, combining the advantages of both in vivo and in vitro experimentation without being subject to the ethical considerations and lack of control associated with in vivo experiments. Unlike in vitro experiments, which exist in isolation, in silico models allow for the inclusion of a virtually unlimited set of variables and parameters, making results more applicable to real-world problems.
In silico experimentation has given rise to the paradigm known as "digital twins." In essence, digital twins are a replica or digital representation of a real-world process or system — where "replica" refers to a computational model developed on the basis of experimental data and special characteristics that allow it to connect the physical with the virtual, with the purpose of improving system performance, detecting and preventing failures, and making predictions about its response to different stimuli or operating scenarios. A more formal definition establishes that: a digital twin is a set of adaptive models that emulate the behavior of a physical system within a virtual system, obtaining real-time data to update itself throughout its life cycle; it replicates the physical system to predict failures and opportunities for change, prescribing real-time actions to optimize and/or mitigate unexpected events by observing and evaluating the system's operational profile.
In the particular field of Systems Biology, a digital twin is presented as an algorithm or set of computational algorithms developed on the basis of mechanistic models of a living organism, with the objective of emulating its physiology to illustrate its dynamics in both the short and long term, as well as predicting its response to different endogenous and exogenous stimuli.
#Objetive
To develop a digital twin of cardiac action potential dynamics by formulating a nonlinear mathematical model based on experimental data, enabling in silico experimentation to analyze, predict, and control the repolarization, depolarization, and refractory phases of cardiac cell behavior.
## Mathematical Model

The cardiac action potential dynamics are described by a three-state nonlinear dynamic system, where the state variables represent key electrophysiological phases of the cardiac cell measured in millivolts (mV): *x(t)* corresponds to the repolarization phase, *y(t)* represents the depolarization phase, and *z(t)* models the refractory phase. The system is governed by the following equations:

$$\dot{x}(t) = \rho_1 x + \rho_2 xz - \rho_3 x^2$$

$$\dot{y}(t) = \rho_4 y - \rho_5 xy$$

$$\dot{z}(t) = \rho_6 z - \rho_7 xz$$

where $\rho_1$ through $\rho_7$ are the model parameters to be estimated from data. In the first equation, the term $\rho_1 x$ drives the natural growth or decay of repolarization, the term $\rho_2 xz$ captures how the refractory state influences repolarization, and the term $-\rho_3 x^2$ introduces a self-limiting effect that prevents the variable from growing without bound. The second equation describes depolarization dynamics, where $\rho_4 y$ reflects the cell's natural tendency to depolarize and $-\rho_5 xy$ shows how repolarization suppresses this excitation, meaning that as *x* grows, depolarization is reduced. Finally, the third equation models the refractory phase, where $\rho_6 z$ represents the natural progression of recovery and $-\rho_7 xz$ captures how repolarization shortens or reduces the refractory state over time. Together, these three coupled equations form a nonlinear system that reproduces the essential electrophysiological behavior of a cardiac cell, serving as the mechanistic core of the proposed digital twin.

Keywords. Mathemetical model, linear regression, 2T prodiction, equilibrium points, electrophysiology 

#Planned Activities
A literature review on cardiac electrophysiology and dynamic systems modeling was conducted, establishing the theoretical foundation required to justify the proposed mathematical model.
The nonlinear mathematical model governing the three-state cardiac system — repolarization x(t), depolarization y(t), and refractory z(t) — was defined and analyzed by applying dynamic systems theory acquired throughout the course.
Simulation data were generated and processed, obtaining smooth and normalized datasets that accurately represent the physiological behavior described by the model.
Linear regression techniques were applied to estimate the model parameters ρ₁ through ρ₇, leveraging data-driven methods studied during the course to bridge experimental data and the mathematical model.
The digital twin was validated through 2T prediction, assessing the model's capacity to forecast the system's temporal evolution under different initial conditions.
The equilibrium points of the nonlinear system were determined and the Jacobian matrix was constructed, applying the linearization methods covered in the course.
The local stability of each equilibrium point was evaluated by interpreting the eigenvalue structure, characterizing the qualitative behavior of the cardiac dynamic system.
A positivity analysis was performed to ensure that the model's state variables remain physiologically meaningful and bounded throughout the simulation horizon.


# List of files included in the repository
1. MATLAB computational notebook [.mlx].
2. Simulation images [.pdf].
3. Biological diagram of the system [.png].
4. Eureka file [.fxp].
