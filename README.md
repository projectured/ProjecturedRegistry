# ProjecturedRegistry

The Julia registry of [ProjecturEd](https://github.com/projectured/projectured-julia),
a projectional editor. It holds the packages of these repositories:

- [Projectured.jl](https://github.com/projectured/Projectured.jl): the packages of
  ProjecturEd, one folder for each package at its root, and the test and example
  packages that their tests need, in `test/` and `example/`.
- [AutoIntegration.jl](https://github.com/projectured/AutoIntegration.jl):
  AutoIntegration, which loads an installed package when its triggers are loaded.
  `Projectured` depends on it.
- [AutoPrecompile.jl](https://github.com/projectured/AutoPrecompile.jl):
  AutoPrecompile, which builds one package image for the packages that a session
  loads, from recorded precompile statements.

## Use it

```
pkg> registry add General
pkg> registry add https://github.com/projectured/ProjecturedRegistry
pkg> add Projectured
```

Add General too, for the packages that ProjecturEd depends on. If General is there
already, the line does nothing. The
[front page of Projectured.jl](https://github.com/projectured/Projectured.jl) says
which packages to add, and how they load.

The release of ProjecturEd adds the versions with LocalRegistry.jl. Do not change
the versions by hand.
