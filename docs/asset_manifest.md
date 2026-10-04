# Asset manifest

Record provenance when downloading or authoring an asset. No asset has been downloaded by creating this workspace.

| Asset | Source URL / revision | License | Local path | Dependencies / modifications |
| --- | --- | --- | --- | --- |
| Stock SO-101 follower | To select from the official LeIsaac asset source | To verify | Expected by stock tasks: `external/leisaac/assets/robots/so101_follower.usd` | Preserve referenced files |
| Stock table-with-cube scene | LeIsaac v0.1.2 asset release, or corresponding Hugging Face package | To verify | Expected: `external/leisaac/assets/scenes/table_with_cube/scene.usd` | Extract the full scene package |
| Custom tic-tac-toe scene | Authored by you | To choose | `scenes/tic_tac_toe/` | References validated robot and object assets |

## Asset-handling rules

- Keep source geometry and simulator-ready assets distinguishable.
- Preserve relative paths and dependencies when moving assets.
- Record units, up axis, joint definitions, and meaningful physical settings.
- Verify geometry and articulation separately from appearance.
- Keep downloaded upstream assets in their expected stock-task location initially.
- Check redistribution terms before adding downloaded assets to a remote repository.

For authored assets, record which scene/robot revision was used in each experiment so changes can be traced.
