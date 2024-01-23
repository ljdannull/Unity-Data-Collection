# Unity Data Collection Procedure
These scripts allow for automated data collection in any Unity environment with any objects being labelled using the Perception package.
## Automated Object Detection Labelling and Data Collection
1. Create an IDLabelConfig and specify the objects that should be la-
belled. For this dataset, the objects classes labelled were door, chair,
table, sofa, television, window, bed. *For further detail on steps 1 and
2, see the [Unity Perception documentation](https://docs.unity3d.com/Packages/com.unity.perception@1.0/manual/Tutorial/Phase1.html)*
2. Go through all of the prefabs used in the asset, and attach the Per-
ception Labelling script to those which should be labelled with boxes,
specifying the relevant class
3. Replace the default script attached to the camera for player control
with `FirstPersonAIO.cs` for automated data collection.
4. Specify points from which to collect data in `RECORDINGPOINTS` variable of `FirstPersonAIO.cs`
5. Run the game and the images and annotations will appear in the folder specified in Perception settings
## Converting Data into COCO Format
1. Specify `source_dir`, `target_dir`, and `val_pct` in `convert_to_coco.ipynb`
2. Run notebook and the converted data will be in `target_dir`
