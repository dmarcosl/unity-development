# Non-Player Characters

To import a Character package go to Assets → Import Package → Characters

To edit the pose of a character, select the Animator Component → Avatar Object → The revealed file → Configure Avatar.

## Performance Bottlenecks

### CPU Bound

The CPU takes longer to process a frame than the GPU.

The GPU wait to render the next frame while the CPU is preparing it.

### GPU Bound

The GPU takes longer to process a frame than the CPU.

The CPU wait to prepare the next frame while the GPU is rendering it.

## Balancing the Pipeline

| Technique                               | CPU | GPU | Rule of Thumb                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|:----------------------------------------|:----|:----|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Polygon Count                           |     | X   | The number of polygons each individual model has should not exceed 1500 on mobile or 4000 on desktop. Overall scenes should not exceed 150.000 polygons on mobile but can be several million on desktop. To keep polygon count down while still achieving the look of a high poly model you can use 'projection' in your modelling package. Have your 3D modeller model & skin your model in very high poly, then project the detailed material onto a lower poly version. |
| Few Materials                           | X   |     | No more than 2 per mesh. One can optimise further by decreasing the quality settings of a mesh down by finding the material and overriding its quality settings.                                                                                                                                                                                                                                                                                                           |
| Few Bones                               | X   | X   | Avatar animated models can be optimised by reducing bone count. You can also achieve this in Quality Settings → Blend Weights → Bone Counts                                                                                                                                                                                                                                                                                                                                |
| Separate Forward and Inverse Kinematics | X   |     | Ensure they are separated in your animation package to allow unity to not over process.                                                                                                                                                                                                                                                                                                                                                                                    |
| Single "Skinned Mesh Renderer"          | X   |     | In general Skins are not very optimised and should be used sparingly on mobile devices. Skins on a mesh should be kept to one.                                                                                                                                                                                                                                                                                                                                             |