# Toy example to use access control with wildcards

Launch the zenoh router

```bash
source ~/ros2_rolling/install/setup.bash
export ZENOH_ROUTER_CONFIG_URI=<path to rmw_zenoh_toy_example>/ROUTER_CONFIG.json5
export RMW_IMPLEMENTATION=rmw_zenoh_cpp
ros2 run rmw_zenoh_cpp rmw_zenohd
```

Talker:

```bash
source ~/ros2_rolling/install/setup.bash
export ZENOH_SESSION_CONFIG_URI=<path to rmw_zenoh_toy_example>/TALKER_CONFIG.json5
export RMW_IMPLEMENTATION=rmw_zenoh_cpp
ros2 run demo_nodes_cpp talker
```

Listener:

```bash
source ~/ros2_rolling/install/setup.bash
export ZENOH_SESSION_CONFIG_URI=<path to rmw_zenoh_toy_example>/LISTENER_CONFIG.json5
export RMW_IMPLEMENTATION=rmw_zenoh_cpp
ros2 run demo_nodes_cpp listener
```

------

Issue:

```bash
2025-02-20T15:57:19.505016Z  WARN net-0 ThreadId(02) zenoh::net::routing::dispatcher::interests: Didn't receive DeclareFinal Face{1, 4436bf22a96c364ae823a6fbefeadfe0}:3 from Face{2, 5a3ba086361c16be8fa4eb06419c235} for interests: Timeout(10s)!
```