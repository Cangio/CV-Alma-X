# CV-Alma-X
This software 

## The competition
ERC is a worldwide robotic challenge in which different teams get involved in many tasks and acquire a score, based on how the solution is innovative and autonomous.
Each rover must be completely wireless, both for power and remote control, and must have a robotic arm with a manipulator to get soil samples from the ground and for operate on a panel with switches and sockets.
### The task
This software is specifically designed for the maintenance task.
That task is intended to demonstrate the ability of the rover to operate on a variety of manipulation elements, mounted on a panel. The team has to use the rover manipulating device to set switches to the required positions, measure electrical parameters, set other panel controls and observe indicator feedback.
In detail, the rover has to:
* set the 'main' switch of the panel to the ON position;
* (sector 2) align the platform by accurately making contact with the positioning pin and report your position in reference to it;
* change the state of a group of switches, make contact with terminals and report the measured voltage, pull the plug out and insert back to the socket;
* (sector 3) actuate 2 push buttons sensitive to excessive forse, detect and localise buttons and the socket.
### Goals
This software provides:
* automatic panel detection;
* automatic approach;
* automatic element detection;
* automatic manipulation;
## The panel
![Panel](/images/panel.png)
1. Switches can be lever or rotational type;
2. The panel will have the form of a box positioned flat on the ground with dimensions of 0.72x0.72m at the base and a height of about 0.30-0.40m;
3. Controls can be mounted on the top or sides of the panel;
4. The panel surface will be divided into 3 sectors between which the rover will need to be relocated;
5. All switches should be manipulated one by one - the activation of more than one in a single move will cause the reset of all the elements;
6. Voltage measurement is to be conducted on standard ‘German type F’/’French type E’ or similar power socket or terminals with similar dimensions and connection requirements;
7. Some panel elements can be sensitive to forces and torques exceeding operational limits. Those elements should not be ‘damaged’ during operations and can be scored differently than stiff ones.