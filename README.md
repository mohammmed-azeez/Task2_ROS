# COMP4034 Robotics - Minitask 2
## Group 30

### Team Members
- Mohammed Azeez
- Muhammed Mehboob

## Project Overview
This project extends our ROS2-based control system by implementing behavior-based robotics concepts for the TurtleBot3. The implementation focuses on creating a robot that can navigate autonomously while avoiding obstacles using sensor data and reactive behaviors.

### Project Structure
```
.
├── minitask_2/
    └── minitsak2.py    # Main implementation with behavior-based control
```

### Features
1. Behavior-Based Control:
   - Real-time obstacle detection
   - Dynamic path adjustment
   - Multiple concurrent behaviors
   - Sensor-based reactive control

2. Sensor Integration:
   - LiDAR data processing
   - Distance-based behavior triggering
   - 360-degree environmental awareness
   - Real-time sensor data interpretation

### Team Contributions

#### Mohammed Azeez
- Implemented the behavior-based architecture
- Developed obstacle detection algorithms
- Created sensor data processing routines
- Handled behavior arbitration system
- Implemented emergency response behaviors

#### Muhammed Mehboob
- Implemented LiDAR data processing
- Developed behavior coordination system
- Created motion control algorithms
- Optimized sensor reading parameters
- Added safety features and fail-safes

### Technical Implementation
The project utilizes advanced ROS2 concepts:
- Subscribers for LiDAR data (`scan`)
- Publishers for velocity commands (`cmd_vel`)
- Multi-threaded behavior processing
- Priority-based behavior arbitration
- Real-time sensor data filtering

### Running the Code
1. Build the package:
   ```bash
   colcon build --packages-select minitask_2
   ```

2. Source the setup file:
   ```bash
   source install/setup.bash
   ```

3. Run the implementation:
   ```bash
   ros2 run minitask_2 minitsak2
   ```

### Behavior Parameters
- Obstacle detection range: 0.5 meters
- Maximum linear velocity: 0.2 m/s
- Maximum angular velocity: 0.5 rad/s
- Safety margin: 0.3 meters
- Behavior update rate: 10 Hz

### Design Decisions
1. Behavior Architecture:
   - Subsumption-based behavior hierarchy
   - Priority-based behavior selection
   - Smooth behavior transitions
   - Real-time behavior adaptation

2. Safety Features:
   - Continuous obstacle monitoring
   - Gradual velocity adjustments
   - Emergency stop capability
   - Fail-safe behaviors

3. Code Organization:
   - Modular behavior implementation
   - Clear behavior hierarchy
   - Well-documented sensor processing
   - Configurable behavior parameters

### Testing
The system was tested under various conditions:
- Different obstacle configurations
- Dynamic environment changes
- Various lighting conditions
- Multiple obstacle types and sizes

### Future Improvements
1. Advanced behavior learning
2. Dynamic behavior creation
3. Environmental mapping integration
4. Multi-robot coordination
5. Machine learning-based behavior optimization

### References
- ROS2 Documentation
- TurtleBot3 Manual
- Behavior-Based Robotics (Arkin)
- Reactive Robot Navigation
- Sensor Processing Techniques
