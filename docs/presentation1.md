---
color: white
draft: true
marp: true
---
<!-- backgroundColor: #003462 -->
# Why Does Synthetic Data Matter? 

### [Generation of synthetic data for machine learning]()

<br/>

### Hallison Paz

---
# Generation of synthetic data for machine learning

### 1. Why does synthetic data matter?
### 2. How to generate synthetic data and train a model with it
### 3. Do they live in a simulation? Training models for dynamic environments

---

<!-- paginate: true -->
# Context

* Machine learning has enabled a lot of nice stuff

Examples:
– Object Detection
– Classification
– Instace segmentation
– Semantic segmentation
– Autonomous vehicles
– Object reconstruction
– Deep Fake

<!-- pictures to illustrate --->
---

# What do we need?

* Computational power / storage
* Methods
* **Data** a lot of data

---

# THERE'S NOT ENOUGHT DATA

---

### This is an issue for applications of ML in all areas. However, in this lecture series, we'll focus on computer graphics and vision problems

many applications require labeling which is expensive or impossible to do by hand, other applications have a wide underlying data distribution that real datasets do not or cannot fully cover, yet other applications may benefit from additional modalities unavailable in real datasets, and so on.

---

# We need labeled data

* Most of these applications are trained using supervised learning

<!--Yan Lecunn Self supervised learning lecture GTC-21-->
Research:
* Create new **methods** to train machine learning models using less **computational power** and less **data**.

* Illustrate f(x) = y

---

# How do we label data?

**Annotation Process**
* Human labels data
  * expensive: you must pay someone to do it
  * error prone: repetitive task and sometimes it can be hard for human to annotate (illustration instace segmentation, 6DoF estimation)
  * You must validate (check if it is correct)

---
# Bias

<!-- Give some dimension on the amount of data used to train something -->
* We need a lot of data 
* We also need to have a good balance between
https://www.theverge.com/21298762/face-depixelizer-ai-machine-learning-tool-pulse-stylegan-obama-bias

CODED BIAS

---

# BIAS

* "Rare" cases
– Self driving car: snowing, rainning etc

---

# Copyright

* Web scrapping
* ImageNet

---

# Privacy

* Data might be related to people
* FaceApp e similares
* Do dilema das redes a PRIVACIDADE HACKEADA

---

# Summarizing issues (Why creating large scale databases is hard?)

### Technical
* Need to annotate data
* Must have sufficent examples for each class
* Must guarantee class balance (BIAS)
  * These requirements might be hard. Rare cases.
## Ethical
* Copyright issues
* Privacy concerns

---

# Data augmentation

* Limited - WHY?

"A related idea is to generate synthetic data from real data by learning to trans- form real data with conditional GANs. This could either simply serve as “smart augmentation” to extend the dataset or, more interestingly, could “fill in the holes” in the data distribution, obtaining synthetic data for situations that are lacking in the original dataset"

- Refer to section 5.3 and 5.4 (GAN's) of survey


"As we discussed in Section 1, data augmentation differs from synthetic data in
that it modifies real data rather than creates new; the modifications are usually
done with predefined transformation functions (TFs) that do not change the
target labels."

---

# Generate new data from the dataset GANs

* You are sampling the same distribution

---

# Synthetic ambiente, synthetic world, synthtetic data

* Build 3D digital scenes to produce data


---

# Synthetic data advantages

* Automatic annotation
* Control over the amount of examples and class balancing
* 
* Protect privacy
* Copyright?

* Data democratization - build solutions outside big corps (Google, Facebook)

---

# AI Graphics

Bridge between computer vision and computer graphics

Shapenet: synthetic but build with human annotations

for many problems, we do not need "realism".

---

## How to build synthetic dataset?

* Media platforms
  * Simulators engines
  * Game Engines
  * Inside games themselves

<!-- Illustrate with examples; "we'll talk more about how to do it in the next lecture next week -->
---
### Tools

– Unreal 
– Mujoco http://www.mujoco.org

--- 

### Beforehand Questions

* How much realism do we need?
* Do we even need real data?
* How much effort to make it work well on real scenarios?
* How about the effort to generate synthetic data?
* Who is using it?
  
---
# BMW Digital Twin
### Who is using it?

Digital twins BMW

---

The Reality Gap

---

"Furthermore, low-fidelity simulated sensors like image renderers are often unable to reproduce the richness and noise produced by their real- world counterparts. These differences, known collectively as the reality gap, form the barrier to using simulated data on real robots."

---

One approach is to make the simulator closely match the physical reality by performing system identification and using high-quality rendering. Though using realistic RGB rendering alone has had limited success for transferring to real robotic tasks [16], incorporating realistic simulation of depth information can allow models trained on rendered images to transfer reasonably well to the real world [32]. Combining data from high-quality simulators with other approaches like fine-tuning can also reduce the number of labeled samples required in the real world


---
# How much realism do we need?

"Unlike these approaches, ours allows the use of low-quality renderers optimized for speed and not carefully
matched to real-world textures, lighting, and scene configurations."


Tobin J, Fong R, Ray A, Schneider J, Zaremba W, Abbeel P (2017) Domain randomization fortransferring deep neural networks from simulation to the real world.2017 IEEE/RSJ Interna-tional Conference on Intelligent Robots and Systems (IROS):23–30

---

#### Domain Randomization

"The purpose of domain randomization is to provide
enough simulated variability at training time such that at test time the model is able to generalize to real-world data. We randomize the following aspects of the domain for each sample used during training"

The idea is simple: let us try to make the synthetic data distribution psyn suffi- ciently wide and varied so that the model trained on psyn will be robust enough to work well on preal. Ideally, we would like to cover preal with psyn, but in reality this is never
achieved directly. Instead, synthetic data in computer vision can be randomized and made more diverse in a number of different ways at the level of either constructing a 3D scene or rendering 2D images from it:
• at the scene construction level, a synthetic data generator (SDG) can ran- domize the number of objects, its relative and absolute positions, number and shape of distractor objects, contents of the scene background, textures of all objects participating in the scene, and so on;
• at the rendering level, SDG can randomize lighting conditions, in partic- ular the position, orientation, and intensity of light sources, change the rendering quality by modifying image resolution, rendering type such as ray tracing or other options, add random noise to the resulting images, and so on

---

Prakash et al. [462] take the next logical step, continuing this effort to structured domain randomization. They still randomize all of the settings mentioned above, but only within realistic ranges, taking into account the structure and context of a specific scene. Finally, another important direction is learning how to randomize. Van
Vuong et al [616] provide one of the first works in this direction, concentrating on picking the best possible domain randomization parameters for sim-to-real transfer of reinforcement learning policies. They show that the parameters that control sampling over Markov decision processes is important for the quality of transferring the learned policy to a real environment and that these parameters can be optimized. We mark this as a first attempt and expect more works devoted to structuring and honing the parameters of domain randomization.

---

Realism on image level
– Realism in sensor level:
  - Depth sensor (not so perfect)
  - Camera noise and distortion as real camera

Realism on Scene level
- Coherence

---
We note a recent joint effort
in this direction by NVIDIA, University of Toronto, and MIT: Kar et al. [309]
present Meta-Sim, a general framework that learns to generate synthetic urban
environments (see also Section 3.1). Meta-Sim represents the composition of
a 3D scene with a scene graph and a probabilistic scene grammar, a common
representation in computer graphics [715].


The goal is to learn how to trans-form samples coming from the probabilistic grammar so that the distribution of
synthetic scenes becomes similar to the distribution of scenes in a real dataset;
this is known as bridging the distribution gap. What’s more, Meta-Sim can also
learn these transformations with the objective of improving the performance
of networks trained on the resulting synthetic data for a specific task such as
object detection (see also Section 8.2).
---

– Contextutal distractors: objetcs similar to possible real scene elementos, positioned randomly but coherently

– Flying distractors: geometric shapes with random texture, size, and position

---

Number and shape of distractor objects on the table • Position and texture of all objects on the table • Textures of the table, floor, skybox, and robot • Position, orientation, and field of view of the camera • Number of lights in the scene • Position, orientation, and specular characteristics of the lights
• Type and amount of random noise added to images Since
---

# Domain Adaptation
Domain adaptation is a set of techniques designed to make a model trained on one domain of data, the source domain, work well on a different, target domain

---
## Synthetic to real refinement

Pg 57-58 survey

Ashish Shrivastava, Tomas Pfister, Oncel Tuzel, Joshua Susskind, Wenda Wang, Russell Webb; Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition (CVPR), 2017, pp. 2107-2116

---
Dilipkumar [148] applied SimGAN to improve handwriting recognition. They generated synthetic handwriting images and applied SimGAN to refine them, with significantly improved recognition of real handwriting after training on a hybrid datase

---

A recent example that applies GAN-based refinement in a classical computer
vision setting is provided by Wang et al. [623]. They consider the problem of recognizing objects inside an automatic vending machines; this is a basic functionality needed for monotoring the state of supplies and is usually done based on object detection. Wang et al. begin by scanning the objects, adding random deformations to the resulting 3D models (see Section 5.2), setting up scenes and rendering with settings matching the fisheye cameras used in smart vending machines. Then they refine rendered images with virtual-to-real style transfer done by a CycleGAN-based architecture. The novelty here is that Wang et al. separate foreground and background losses, arguing that style transfer needed for foreground objects is very different from (much stronger than) the style transfer for backgrounds. Thus, they use the overall loss function [pg62]

Segmentation into foreground and background is done automatically in syn- thetic data and is made easy in [623] for real data since the camera position is fixed, and the authors can collect a dataset of real background templates from the vending machines they used in the experiments and then simply subtract the backgrounds to get the foreground part. As a result, Wang et al. report signif- icantly improved results when using hybrid datasets of real and synthetic data for all three tested object detection architectures: PVANET [320], SSD [372], and YOLOv3 [482]. Even more importantly, they report a comparison between basic and refined synthetic data with clear gains achieved by refinement across all architectures.

Wang et al. Synthetic Data Generation and Adaption for Object Detection in Smart Vending Machines

---
GANs image to image ... SKIP?
Another idea for generating synthetic data from real is to compose parts
of real images to produce synthetic ones. We have discussed the cut-and-paste approaches in 5.3; a natural continuation of these ideas would be to use more complex, semantic conditioning with a GAN-based architecture.

---

## Domain adaptation at the feature/model level

feature-level or model-level domain adaptation, i.e., methods that work in the space of features or model weights and never go back to change the actual data.


"A key insight of our approach is that the synthetically generated images should be similar to real images, not in terms of image quality, but rather in terms of features used during the detector training."

Artem Rozantsev, Vincent Lepetit, and Pascal Fua. On rendering syn- thetic images for training an object detector. Computer Vision and Image Understanding, 137:24 – 37, 2015

---
* Differential Privacy???
--- 
### Challenges

* Differences in camera hardware

* Photorealistic data is still hard to generate (is it comparable to annotate??)

---

* How about the effort to generate synthetic data?

next week...
---
Finally, a note of caution: GAN-based refinement is not the only way to go.
Kan et al. [304] compared three approaches to data augmentation for pupil cen- ter point detection, an important subproblem in gaze estimation: affine trans- formations of real images, synthetic images from UnityEyes, and GAN-based refinement. In their experiments, real data augmentation with affine transfor- mations was a clear winner, with the GAN improving over UnityEyes but falling short of the augmented real dataset.
This is one example of a general common
wisdom: in cases where a real dataset is available, one should squeeze out all
the information available in it and apply as much augmentation as possible,
regardless of whether the dataset is augmented with synthetic data or not.

---
Procedural generation?

---
Will be even more important in the future

---
<!-- paginate: false -->

# Thank You

[hallpaz@impa.br](mailto:hallpaz@impa.br)


For other domains, we recommend:

Nikolenko, Sergey. “Synthetic data for deep learning,” arXiv preprint
arXiv:1909.11512, 2019.

---


