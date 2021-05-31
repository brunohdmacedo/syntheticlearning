---
draft: true
marp: true
---

# How to generate synthetic data and train a model with it? 

<br/>

### Hallison Paz

---

# Generation of synthetic data for machine learning

### 1. Why does synthetic data matter?
### 2. How to generate synthetic data and train a model with it
### 3. Do they live in a simulation? Training models for dynamic environments

---
For each foreground object, we start by generating a
large set of poses uniformly covering the pose space in which we want to be able to detect the corresponding ob- ject. To do so, we use the approach described in [10] and generate rotations by recursively dividing an icosahedron, the largest convex regular polyhedron. This approach yields uniformly distributed vertices on a sphere and each vertex represents a distinct view of an object defined by two out- of-plane rotations.

---

Procedural generation?

S. Qi, Y. Zhu, S. Huang, C. Jiang, and S. Zhu. Human-centric indoor scene synthesis using stochastic grammar. In 2018 IEEE/CVF Conference on Computer Vision and Pattern Recognition, pages 5899–5908, June 2018.



SCHEMA: https://www.nuscenes.org/nuscenes#data-format
https://github.com/Unity-Technologies/com.unity.perception/blob/master/com.unity.perception/Documentation%7E/Schema/Synthetic_Dataset_Schema.md
---
https://logicai.io/blog/synthetic-data-deep-learning/

https://github.com/DLR-RM/BlenderProc
