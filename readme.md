# GraspVOA

This project is an instantiation of the broader concept 'Value of Assistance', which is currently under research at the CLAIR Lab - The Taub Faculty of Computer Science at Technion.

The simulator that was used to generate simulation data:
[Sim](https://github.com/yuvalgos/grasp_voa_simulator)

The ROS node that we used to capture our observations:
[Lab](https://github.com/masarwy-m/grasp_voa)

The code for the UR5e and the depth camera:
[DC](https://github.com/masarwy/GraspVOA_DC)

# Notes

Since our model failed to capture the mouse and the marker in the simulation, we could not conduct the experiments. Possible reasons for this failure:
1. Very small models relative to the sensor.
2. Noisy meshes.
3. We tried to model the LDS sensor in the simulation using a depth camera, which caused many inaccuracies. Additionally, there is a gap between the prediction function and the LDS itself, which was exacerbated by the depth camera modeling.

For the spray flask, the observations were very noisy in the simulation. In addition to the previous reasons, apparently we didn't capture the stable poses correctly. We noticed that VOA directed us to choose the sensor configuration with the least gap between the sensor readings and the predicted observation.
