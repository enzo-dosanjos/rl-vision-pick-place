The Robot base is the project origin.
one global coordinate system
Positive axes

Skeleton :
- Define a single source of truth for the entire robotic cell
- Every assembly shall reference the skeleton rather than other assemblies whenever practical
- Define all global coordinate systems
- Define all major workspaces
- Define robot origin
- Define camera origin
- Define future conveyor location
- Define pickup and drop zones
- Define calibration plate location
- Define electronics envelope
- Define maintenance clearances
- Support automatic URDF generation
- Support MuJoCo model generation
- Support ROS 2 TF tree creation
- Construction geometry only