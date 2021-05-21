---
draft: true
marp: true
---

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

Digital twins BMW

---

#### Domain Randomization
– Contextutal distractors: objetcs similar to possible real scene elementos, positioned randomly but coherently

– Flying distractors: geometric shapes with random texture, size, and position

* Differential Privacy

--- 
### Challenges

* Differences in camera hardware

* Photorealistic data is still hard to generate (is it comparable to annotate??)

---

<!-- paginate: false -->

# Thank You

[hallpaz@impa.br](mailto:hallpaz@impa.br)
