# DDPA-3DVG

This repo is the official implementation of "DDPA-3DVG: Vision-Language Dual-Decoupling and Progressive Alignment for 3D Visual Grounding".

## :star:Overview
3D visual grounding aims to localize target objects in point clouds based on free-form natural language, which often describes both target and reference objects. Effective alignment between visual and text features is crucial for this task. However, existing two-stage methods that rely solely on object-level features can yield suboptimal accuracy, while one-stage methods that align only point-level features can be prone to noise. In this paper, we propose DDPA-3DVG, a novel framework that progressively aligns visual locations and language descriptions at multiple granularities. Specifically, we decouple natural language descriptions into distinct representations of target objects, reference objects, and their mutual relationships, while disentangling 3D scenes into object-level, voxel-level, and point-level features. By progressively fusing these dual-decoupled features from coarse to fine, our method enhances cross-modal alignment and achieves state-of-the-art performance on three challenging benchmarks—ScanRefer, Nr3D, and Sr3D.

## :crown:Main Results
| Methods               | Modality | Unique(IOU25) | Unique(IOU50) | Multiple(IOU25) | Multiple(IOU50) | Overall(IOU25) |Overall(IOU50)|
|-----------------------|----------|-------------:|---------:|--------------:|---------:|------------:|---------:|
| **FFL-3DOG**          | 3D       |         78.8 |     67.9 |          35.2 |     25.7 |        41.3 |     34.0 |
| **3DJCG**             | 3D+2D    |         83.5 |     64.3 |          41.4 |     30.8 |        49.6 |     37.3 |
| **BUTD-DETR**         | 3D       |         82.9 |     65.0 |     44.7 |     34.0 |        50.4 |     38.6 |
| **EDA**               | 3D       |     85.8 |     68.6 |     49.1 |     37.6 |     54.6 |     42.3 |
| **ViewRefer**         | 3D       |           -  |       -  |          33.1 |     26.5 |        41.3 |     33.7 |
| **3DRP-Net**          | 3D       |         83.1 |     67.7 |          42.1 |     32.0 |        50.1 |     38.9 |
| **3DVLP**             | 3D       |     85.2** |     70.0 |          43.7 |     33.4 |     51.7 |     40.5 |
| **DDPA-3DVG**         | 3D       |     **86.8** |     **70.2** |     **49.8** |     **38.4** |     **55.3** |     **43.3** |
|-----------------------|----------|-------------:|---------:|--------------:|---------:|------------:|---------:|
| **3D-SPS***           | 3D       |     81.6 |     64.8 |          39.5 |     29.6 |        47.7 |     36.4 |
| **BUTD-DETR***        | 3D       |         81.5 |     61.2 |     44.2 |     32.8 |     49.8 |     37.1 |
| **EDA***              | 3D       |     86.4 |     69.4 |     48.1 |     36.8 |     53.8 |     41.7 |
| **DDPA-3DVG***        | 3D       |     **86.5** |     **69.9** |     **48.6** |     **37.4** |     **54.3** |     **42.2** |
