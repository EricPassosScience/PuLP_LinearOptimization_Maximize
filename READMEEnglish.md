# PuLP_LinearOptimization_Maximize
In this mini-project, we will use one of the main frameworks for linear optimization, PuLP. We will use this excellent tool to try to solve the following business problem:

Lua Smart Tech assembles and tests two smartphone models, Lua1 and Lua2. For the next month, the company wants to decide how many units of each model it will assemble and then test.

No smartphones have been in stock since the previous month, and since these models will be switching after this month, the company doesn't want to keep any stock for the following month.

She believes that the maximum she can sell this month is 600 units of the Lua1 model and 1200 units of the Lua2 model.

Each Lua1 model is sold for R$300.00 and each Lua2 model for R$450.00. The cost of components for a Lua1 is R$150.00 and for a Lua2 it is R$225.00.

Labor is required for assembly and testing. There are a maximum of 10,000 hours of assembly and 3,000 hours of testing available. Each hour of assembly work costs R$11 and each hour of test work costs R$15. Each Lua1 requires five hours for assembly and one hour for testing. Each Lua2 requires six hours for assembly and two hours for testing.

Lua Smart Tech wants to know how many units of each model it should produce (assemble and test) to maximize its net profit, but it cannot use more man-hours than available and does not want to produce more than it can sell.

### Documentation
https://pypi.org/project/PuLP/

https://coin-or.github.io/pulp/

### Parameters
- Ai = Maximum number of type I smartphones to sell this month, where I belong to {Lua1, Lua2}
- Bi = Sale price of smartphones type I, where I belong to the set {Lua1, Lua2}
- Ci = Cost price of component parts for type I smartphones, where I belong to the set {Lua1. Lua2}
- Di = Cost of assembly labor per hour of smartphones tipi I model, where I belong to the set {Lua1, Lua2}
- Ei = Test labor cost per hour of smartphone type I model, where I belong to set {Lua1, Lua2}
- F = Maximum number of hours of assembly work
- G = Maximum number of test work hours
- Hf, i = Assembly hours needed to build each smartphone model type I, where I belongs to the set {Lua1, Lua2}
- Hg, i = Test hours needed to test each smartphone model type I, where I belongs to the set {Lua1, Lua2}

### Decision Variable
- Xi = Number of smartphones model I type to be produced this month, where I belong to the set {Lua1, Lua2}

We will also define constraints so that we don't have negative values ​​and values ​​that are outside those defined in the business problem.

### Restrictions
- The number of types I smartphones to be produced cannot be negative, that is, Xi >=0, where I belong to the set (Lua1, Lua2).
- The total number of assembly hours cannot be greater than the maximum number of available assembly labor hours
- The total number of test hours cannot be greater than the maximum available test manpower hours.
- The number of the model I smartphones to be produced cannot be greater than the maximum number of the model I smartphones to be sold this month, where I belongs to the set {Lua1, Lua2}
