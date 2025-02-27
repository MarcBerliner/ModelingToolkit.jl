# ODESystem

## System Constructors

```@docs
ODESystem
```

## Composition and Accessor Functions

  - `get_eqs(sys)` or `equations(sys)`: The equations that define the ODE.
  - `get_states(sys)` or `states(sys)`: The set of states in the ODE.
  - `get_ps(sys)` or `parameters(sys)`: The parameters of the ODE.
  - `get_iv(sys)`: The independent variable of the ODE.
  - `get_u0_p(sys, u0map, parammap)` Numeric arrays for the initial condition and parameters given `var => value` maps.

## Transformations

```@docs
structural_simplify
ode_order_lowering
dae_index_lowering
liouville_transform
alias_elimination
tearing
```

## Analyses

```@docs
ModelingToolkit.islinear
ModelingToolkit.isautonomous
ModelingToolkit.isaffine
```

## Applicable Calculation and Generation Functions

```@docs; canonical=false
calculate_jacobian
calculate_tgrad
calculate_factorized_W
generate_jacobian
generate_tgrad
generate_factorized_W
jacobian_sparsity
```

## Standard Problem Constructors

```@docs
ODEFunction(sys::ModelingToolkit.AbstractODESystem, args...)
ODEProblem(sys::ModelingToolkit.AbstractODESystem, args...)
SteadyStateProblem(sys::ModelingToolkit.AbstractODESystem, args...)
```

## Torn Problem Constructors

```@docs
ODAEProblem
```

## Expression Constructors

```@docs
ODEFunctionExpr
DAEFunctionExpr
SteadyStateProblemExpr
```
