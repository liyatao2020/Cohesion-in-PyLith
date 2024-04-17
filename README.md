# README.md

## Project Overview

This project focuses on finite element analysis of geological models, particularly simulating the complex processes of crustal deformation. With the help of PyLith software, we have successfully constructed a fine mesh model and executed a series of simulation steps to explore the dynamic behavior of the Earth's crust. Through this README, you will be able to understand the model configuration and processing methods.

## Project File Organization

- `mesh.exo`: Contains the completed fine mesh model file.
- `step00.cfg`: PyLith configuration file for precise control of simulation startup and execution.
- `fault_slabtop_slipweakening.spatialdb`: Defines key parameters used in the simulation, such as friction coefficient and cohesion.

## Analysis Parameters

Our current analysis relies on the mechanical parameters specified in Table 1. With the help of PyLith 2.2.2, we are able to precisely simulate the spatial variations in shear strain energy caused by coseismic slips within faults affected by mining operations.

### Mechanical Parameters Used in the Simulation:

- **Poisson's Ratio (ν):** 0.25
- **Depth Range (h):** 0-1600 meters
- **Fault Dip Angle (φ):** 30 degrees
- **Shear Modulus (G):** 6.5 GPa
- **Mining Level:** 1000 meters
- **Friction Coefficient (μ):** 0.7
- **Shear Wave Speed (VS):** 1.65 km/s
- **Panel Width:** 200 meters
- **Background Stress Ratio (rb):** 2
- **Compressional Wave Speed (VP):** 2.74 km/s
- **Mining Distance Range (Dm):** From -120 to +120 meters
- **Cohesion Stress Range:** 0-4 MPa
- **Density (ρ):** 2400 kg/m³
- **Mining Thickness:** 10 meters

## Running Guide

1. Refer to the official PyLith documentation to ensure the correct installation of PyLith version 2.2.2.
2. In the project root directory, start the simulation process with the following command:

```bash
pylith step00.cfg
```

After the simulation is complete, all results will be output to the `output` folder.

## Result Output and Viewing

After the simulation ends, you can find the following `.xmf` formatted result files in the `output` folder:

- `step02.xmf`
- `step02-concrust.xmf`
- `step02-oceancrust.xmf`

For convenient viewing and sharing, the simulation results have also been uploaded to: https://github.com/liyatao2020/Cohesion-in-PyLith-Output

These files record various data during the simulation process in detail, and you can use software like ParaView for viewing and analysis.

### Result Viewing Method:

- Open the ParaView software.
- Import `.xmf` files to view the simulation results.
- Utilize ParaView's rich toolset, such as slicing, isosurfacing, etc., to showcase the simulation data in all directions.
- If further data processing is required, you can use ParaView's Filter function to export the data in CSV format, providing convenience for subsequent in-depth analysis, such as calculating slip distrib
