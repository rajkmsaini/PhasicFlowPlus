<div align ="center">
<img src="doc/phasicFlowPlus_Logo_github.png" style="width: 400px;">
</div>

.

**PhasicFlowPlus** is a software package for simulating fluid-particle flows. It is a combination of computational fluid dynamics (CFD) and discrete element method (DEM). The fluid is assumed as a continuum phase and the particles as discrete bodies.

Here, DEM calculations are handled using features of [PhasicFlow](https://github.com/PhasicFlow/phasicFlow). It is a parallel DEM package that can be run on multi-core CPUs or GPUs. The equations for the fluid phase are discritized based on finite volume (FV) and solved using OpenFOAM. OpenFOAM is parallelized based on MPI for being executed on multicore CPUs. The fluid-particle coupling (PhasicFlowPlus) uses both parallelization methods, shared-memory and MPI, to leverage the maximum computational resoureces. 

Based on the above configuration, PhasicFlowPlus can use the computational resources of a multi-core CPU or use the computational resource of both CPU and GPU. 

## What is under development?
The following parts are being developed at the moment:
* Course graining for CFD-DEM
* Resolved solver for CFD-DEM
* Modifying some parts for better functionality and performance  

## How to build version 0.1
First, you need to [install PhasicFlow-v0.1](https://github.com/PhasicFlow/phasicFlow/wiki/How-to-Build-PhasicFlow) and OpenFoam-v9 (For now, it is only tested with [OpenFOAM-v9](https://openfoam.org/download/9-source/)) on your computer. After that, copy [PhasicFlowPlus-v0.1](https://github.com/PhasicFlow/PhasicFlowPlus/releases/tag/v-0.1) on your computer. The `PhasicFlowPlus` folder shoule be located beside `phasicFlow` folder on your computer (in ~/PhasicFlow/ folder). Navigate to the root directory of the code and enter the following commands to install the code.

```
cd ~/PhasicFlow/PhasicFlowPlus/ 
./Allwmake
```


