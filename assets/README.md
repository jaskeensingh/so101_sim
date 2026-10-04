# Downloaded and reusable assets

Use `robots/so101/usd/`, `robots/so101/urdf/`, and `robots/so101/meshes/` for your own referenced robot asset set, preserving its internal reference paths. Use `objects/tokens/`, `objects/chess_pieces/`, and `objects/cloth/` for task objects.

A USD or URDF can reference other files. Moving the top-level file alone can break the asset; keep the complete referenced tree or update/re-export references deliberately. Record the original source, exact revision, license, and changes in `docs/asset_manifest.md`.

These directories are placeholders. The first LeIsaac stock exercise uses its documented asset layout under `external/leisaac/assets/`, including the follower USD and the complete table-with-cube scene package. It does not use this project's asset folders automatically.

Large assets are ignored by the parent Git repository by default. This README and other asset README files can be committed.
