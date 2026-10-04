# Environment record

## Existing other-project environment: inspected 4 October 2026

| Component | Observed value |
| --- | --- |
| Interpreter | `/home/frankaarmblr/env_isaaclab/bin/python` |
| Python runtime | 3.11.16 |
| Isaac Sim Python distribution | 5.1.0.0 |
| Isaac Lab repository VERSION file | 2.3.2 |
| Isaac Lab core extension distribution | 0.54.4 |
| Isaac Lab checkout | `/home/frankaarmblr/IsaacLab`, commit displayed as `3d43d9e139`, with local modifications |
| Editable package origin | `/home/frankaarmblr/IsaacLab/source/isaaclab` |
| PyTorch | 2.7.0+cu128 |
| LeIsaac / LeRobot in this environment | Neither found as a named installed distribution |
| Available home filesystem space | About 192 GB |

The repository/framework version and core extension package version are different numbering systems. Package metadata was read without launching Isaac Sim or importing its runtime. This is an inventory, not a runtime test.

## Planned SO-101 setup

| Component | Target | Status |
| --- | --- | --- |
| Workspace | `/home/frankaarmblr/so101_sim` | Starter folders/docs created |
| Python environment | `/home/frankaarmblr/env_so101_sim`, Python 3.11 | Not created |
| LeIsaac checkout | `external/leisaac` | Not cloned |
| LeIsaac version/revision | 0.4.0 / `24d3bcd3f1e4585740fc79921782c41617237812` | Source/docs reviewed |
| Isaac Lab source | LeIsaac's pinned `dependencies/IsaacLab` submodule | Not cloned/installed |
| Isaac Lab target | v2.3.0 / `3c6e67bb5c7ada942a6d1884ab69338f57596f77` | Upstream pin verified |
| Isaac Sim | 5.1.0, in the dedicated environment | Not installed |
| PyTorch | 2.7.0, CUDA 12.8 wheel | Not installed |
| First task | LeIsaac-SO101-LiftCube-v0 |
| First input | Keyboard |
| LeRobot | Defer for initial keyboard control | Optional upstream extra pins 0.4.2 |

Using a dedicated environment may install another set of Isaac Sim packages. The existing pip-based installation lives inside the other project's environment, so sharing it is not automatic. Package/download caches can sometimes save downloads, but are not the same as an installed environment.

## Verification to fill after setup

- Interpreter and pip point to the dedicated environment:
- GPU available from this environment with the expected CUDA build:
- Framework and LeIsaac dependencies pass a package check:
- Stock scene assets resolve:
- Stock task launches:
- Keyboard, reset, gripper, and camera behavior checked:
- First ten lift/release attempts and results:

## Later policy environment

Choose a separate policy-training environment when selecting the model. Current LeRobot v0.6.1 requires Python >=3.12, whereas this simulation recipe uses 3.11. Start with local raw recordings, then verify the conversion/dataset conventions of the chosen policy stack. Separate environments do not by themselves guarantee dataset/action compatibility.
