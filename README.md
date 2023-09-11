# DeepONet for epidemic modelling

DeepONet is an artificial neural network framework to solve partial differential equations (PDEs). Deep learning techniques are used to approximate the solutions of PDE by directly learning a mapping between input variables and the corresponding PDE solutions. We adapt DeepONet to learn an operator mapping basic reproduction number $R_0$ to the solution of compartment model, $I(t)$ in SIS model.


# How the code works
1. Install deepxde https://github.com/lululxvi/deepxde

2. Download the scripts in https://github.com/lululxvi/deeponet/tree/8d62345afd39e1df9c2c8c8d0e7c41882b06a9bf/src 

3. Download and run trainig_data_set.py to generate training and test data set for constant R_0 case.
   Or download and run training_data_set.py for time dependent R_0 case.

5. Download and run deeponet_pde.py after to train and see the result.



# Case1: $R_0(t)$ is constant
ODE: $\frac{dI}{dt} = R_0(x) \gamma  (1-I(t))  I(t) - \gamma  I(t)$

Number of sensors: 30

Number of traning set: 10000

Number of test set: 11000

Learning rate: 0.01

Epochs: 400



![Alt text](/R=1.3.png)

L2 relative error: 0.3781961877344248

![Alt text](/R=2.03.png)


L2 relative error: 0.036210400064317846

![Alt text](/R=2.12.png)

L2 relative error: 0.06472685408335464

# Case2: $R_0(t)$ is time dependent
