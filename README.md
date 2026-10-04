# SO-101 simulation project

Learn to operate a simulated SO-101 by keyboard, then develop tic-tac-toe, chess, and cloth tasks. All three projects begin in simulation; physical transfer is a later stage.

This is a starter workspace containing directories, documentation, and Git tracking rules. No robot-control code, installed environment, downloaded robot, upstream clone, or remote repository has been created here. Git initialization is an exercise in the setup lesson.

## First milestone

Use LeIsaac's existing single-arm lift-cube task to verify the simulator, SO-101 asset, keyboard input, reset, and grasp/release. Then build a minimal board scene: table, follower, nine cells, token tray, and overhead camera.

## Where things belong

| Path | Contents | Storage |
| --- | --- | --- |
| `docs/` | Design notes, version records, asset provenance, experiment notes | Git/GitHub |
| `configs/` | Your task, camera, control, and experiment settings when created | Git/GitHub |
| `source/` | Your future implementation, written by you | Git/GitHub |
| `scenes/tic_tac_toe/` | Small authored USD scene compositions and notes | Small files in Git; large binaries need a separate plan |
| `scenes/chess/`, `scenes/folding/` | Later scene compositions and task notes | Same rule |
| `assets/robots/so101/` | Downloaded robot USD/URDF files and referenced meshes | Local initially; record source/license/revision in docs |
| `assets/objects/` | Token, chess-piece, and cloth assets | Local initially; record provenance |
| `data/raw/` | Original simulation recordings, initially HDF5 | Local, later suitable dataset storage |
| `data/lerobot/` | Converted/validated LeRobot datasets | Local; optional Hugging Face dataset repository |
| `checkpoints/` | Learned weights, not robot geometry | Local; optional Hugging Face model repository |
| `outputs/` | Videos, logs, evaluation reports, and run artifacts | Local; selected small reports can be copied into docs |
| `external/` | Independent upstream repositories such as LeIsaac | Their own Git histories; ignored by this parent workspace |

The default `.gitignore` excludes downloaded assets, recordings, weights, generated outputs, and nested upstream repositories. Small documentation files inside assets remain trackable. Binary USD files are also excluded by default; use small `.usda` scene descriptions or deliberately configure Git LFS for chosen large authored assets later.

LeIsaac stock tasks expect assets in the LeIsaac checkout's own `assets/` layout. Preserve that layout for the initial cube exercise. Your project's `assets/` directory is for assets organized/referenced by your custom tasks; the stock launcher does not automatically discover it.

## Learning notes

Read `../lerobot_learning/03a_project_setup.md` on this laptop for the guided setup steps. Record your chosen versions in [the environment record](docs/environment.md), assets in [the asset manifest](docs/asset_manifest.md), and recordings in [the data plan](docs/data_plan.md).

The next action is local Git initialization and the first documentation commit. Installation and a stock simulator smoke test follow. GitHub/Hugging Face publication is optional and happens only when you choose it.
