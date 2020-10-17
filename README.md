# Hybrid parallelized thermal conduction
This project simulates thermal conduction within a metal plate. Edges of the plate are held at constant tempurature. Simulation calculates convergence via Jacobi iterations.

The unoptimized serial runtime costed roughly 27 minutes. When the same algorithm was optimized to use 4 multi-threaded processes across a Beowulf cluster of 4 dual-core hyper-threaded processors, the runtime was cut down to roughly 6 minutes.

## How it works
The beowulf cluster connects 4 laptops running a slim linux kernel are connected over a switch. The OpenMPI and OpenMP libraries were used to manage the threads and processes. 

### Converged plate heatmap

![Image of Converged Thermal Plate](./ConvergedThermalPlate.png)