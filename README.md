A ROS package for testing internet speed using open source API from speedtest.net

# Dependency
- [speedtest-cli for python](https://pypi.org/project/speedtest-cli/)

# Quick start
- Run internet_speed_node:
```
rosrun ros_internet_speed internet_speed_node
```
- Echo ros topic `/internet_speed`:
```
rostopic echo /internet_speed
```
- Call ros service `/run_speed_test`:
```
rosservice call /internet_speed_node/run_speed_test "{}"
```

# internet_speedh_node
### Published Topics

```
internet_speed (ros_internet_speed/InternetSpeedReport.h)
    A report of the internet speed test result 
```

### Published Services

```
internet_speed_node/run_speed_test (std_srvs/Trigger.h)
    Trigger to run internet speed test once
```