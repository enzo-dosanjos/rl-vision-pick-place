Joints :
J1 — Base Yaw
J2 — Shoulder Pitch
J3 — Elbow Pitch
J4 — Wrist Yaw
J5 — Wrist Pitch
J6 — Wrist Roll
J7 — Parallel Gripper

| Joint   | Motor Location |       Transmission       |
| ------- | -------------- | ------------------------ |
| J1      | Base           | Direct w/ bearings       |
| J2      | Shoulder       | Direct w/ bearings       |
| J3      | Shoulder       | Timing belt              |
| J4      | Forearm        | Direct                   |
| J5      | Wrist          | Direct                   |
| J6      | Wrist          | Direct                   |
| Gripper | Gripper        | Direct                   |

lower moving inertia as half of the motors ar close to the base and reduce strain on motors moving the most mass using bearings and shafts.

For J2, the rotating hub acts as a shaft. The hub has thick walls to be stiff enough to avoid the introduction of torsional compliance and reduce bearing support


The workspace is defined after camera calibration.

There are no permanently defined physical pickup or placement areas. Object Position is sampled randomly and Goal position is sample independently. Object and goal shall remain within the reachable workspace and respect edge clearances


Ros 2 data flow :

Camera
   ↓
Camera Node
   ↓
Calibration Node
   ↓
Detection Node
   ↓
Pose Estimation Node
   ↓
Task Manager
   ↓
Policy / Planner
   ↓
Robot Controller
   ↓
Hardware Interface


The PPO policy observes structured state only :
Joint Positions
Joint Velocities
Gripper State
Object Pose
Goal Pose