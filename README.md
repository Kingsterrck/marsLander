# marsLander
The project I'm working on that 1. finalizes an existing simulation of a mars lander and 2. develops advanced functionalities like autopilot, comms sim, etc. Finished and archived by mid August, 2023

# How does autopilot work
Currently, the autopilot does not support deorbit burns and is only compatible with the EDL phase. The engine would be turned on at 70k km (or any value defined as `entryBurnThreshold`) and perform an entry burn until the spacecraft slows down enough to deploy its parachute at 8 km (`parachuteDeploy`). As the parachute provides drag for the lander, the engine would go on standby until 400m (`landingBurnThreshold`) above the surface when it is turned on again to bring the lander to a soft landing.
