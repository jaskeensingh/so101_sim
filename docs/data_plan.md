# Data and model storage

Initially keep recordings local. Running a keyboard-controlled simulation does not require a Hugging Face account or a remote GitHub repository.

## Directory meanings

- `data/raw/`: untouched source recordings, initially LeIsaac HDF5 episodes.
- `data/lerobot/`: converted datasets whose camera names, action mapping, timing, and schema have been checked.
- `checkpoints/`: learned model weights and related training state.
- `outputs/`: per-run logs, videos, and evaluation outputs.
- `docs/`: small reviewed reports and manifests you deliberately commit.

Use task and session identifiers, for example `data/raw/tic_tac_toe/session_001/` and `outputs/evaluation/tic_tac_toe/run_001/`. Avoid overwriting a recording when changing the task or action convention. A filename is not a substitute for a metadata record.

## Remote services when useful

| Service | Suggested responsibility |
| --- | --- |
| GitHub project repository | Project source, docs, configurations, small scene compositions, and provenance manifests |
| Hugging Face dataset repository | A selected version of your validated robotics dataset, with a dataset card |
| Hugging Face model repository | A selected checkpoint with model/configuration information and a model card |
| Git LFS, release storage, or object storage | Selected large assets/artifacts when there is a reason to share them |

GitHub and Hugging Face are common choices, not a mandatory community standard. Both can host Git repositories; their tooling and typical use differ. Do not duplicate every recording in both services.

For each shared dataset/model, link the project commit, task definition, robot revision, units, cameras, data split, and evaluation results. Choose visibility and review asset/data licenses before uploading. No upload, remote creation, or publishing is part of this starter scaffold.
