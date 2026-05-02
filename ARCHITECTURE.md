## Nodes

| Node | Workspace |
|------|-----------|
| `internnav_system1` | server_ws |
| `internnav_system2` | server_ws |
| `internnav_planner` | client_ws |
| `internnav_controller` | client_ws |

## Topics

| Topic | Type | Publisher | Subscriber(s) |
|-------|------|-----------|---------------|
| `/utlidar/robot_odom` | Odometry | *(hardware)* | internnav_planner, internnav_controller |
| `/internnav/server/system2/instruction` | String | *(external)* | internnav_system2 |
| `/internnav/server/system2/plan_context` | PlanContext | internnav_system2 | internnav_system1 |
| `/internnav/server/system2/output_discretes` | DiscreteStamped | internnav_system2 | internnav_system1, internnav_planner |
| `/internnav/server/system1/output_path` | Path | internnav_system1 | internnav_planner |
| `/internnav/client/cmd_path` | Path | internnav_planner | internnav_controller |
| `/internnav/client/cmd_pose` | PoseStamped | internnav_planner | internnav_controller |
| `/internnav/client/cmd_stop` | Header | internnav_planner | internnav_controller |
| `/api/sport/request` | Request | internnav_controller | *(hardware)* |
| `/camera/color/image_raw` | Image | *(hardware)* | internnav_system2, internnav_system1 |
| `/internnav/server/cmd_reset` | Empty | *(external)* | internnav_system2, internnav_system1 |
