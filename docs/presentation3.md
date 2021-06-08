---

marp: true
inlineSVG: true
theme: blue
draft: true
paginate: true

---
<!-- _color: white -->
<!-- _class: invert -->
<!-- _paginate: false -->
![bg fit right:32%](img/visgraf-part.jpeg)

# How to generate synthetic data and train a model with it? 

### Generation of synthetic data for machine learning

<br/>

### Hallison Paz

---

# Generation of synthetic data for machine learning

### 1. ~~Why does synthetic data matter?~~
### 2. **How to generate synthetic data and train a model with it**
### 3. Do they live in a simulation? Training models for dynamic environments

---

<!-- _class: topic -->
<!-- _paginate: false -->

# Recap

---
# Two weeks ago ...

* **We need a lot of data** to train machine learning models
* Creating large scale **datasets** is hard and presents both **technical and ethical challenges**
* **Synthetic data** can help us overcome these challenges
* But we must pay the cost of the **Reality Gap**
  * Domain randomization
  * Domain adaptation

---

# Last week ...

* There are many tools available to generate synthtetic datasets
* It's important to have a strategy to generate good data
  * We can iterate dataset versions
* Even a small team can generate large scale synthetic datasets
  * There are already tutorials to help with this task

---

# Today's agenda

* Why learn on simulations?
* How to generate these simulations?
* Techniques to train on simulation

---
<!-- _class: topic -->
<!-- _paginate: false -->

# Why Simulations?

---

# Why learn on simulations

* Large diversity of training data
* Faster than real time


---

Training robot for Mars?

Caso da pesquisadora que simulava crowd?
- films, games, urban engineering, behavioural science

finding Landing sites for Unmanned Aircraft Systems (Castagno)

---

https://dl.acm.org/doi/abs/10.1145/3274247.3274510

<video poster="https://videodelivery.net/eyJraWQiOiI3YjgzNTg3NDZlNWJmNDM0MjY5YzEwZTYwMDg0ZjViYiIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIwNzQ3MjEzNDBmMGE5NGE0YWNhNDY5YjBlMTA4MDMyYyIsImtpZCI6IjdiODM1ODc0NmU1YmY0MzQyNjljMTBlNjAwODRmNWJiIiwiZXhwIjoxNjIzMTM4MzM1fQ.BD0WpUdzK6k_Z8DGTMx_qlbCLQiDLh8jShLV3xoMXjLqlLpK9byFSz1QFjnnxJLezbpMb8YWZMz_lln2LkR-V4y6oLKXMvuJkZWi7RkhQpLZUPoHQHQeuQpiTCiQlRPLUAdXZNT_7xp98B4PI_BfVLX7W9kMnJr69QFbz-pzraD8LxV1BUkHyxcRprVzCB2qRyRkbvIQzXpKKSXGhQ9QckQgtaKZ79nWkJS1AHCXZ-T_RCJB-Jn207FaT2R4pWkHCmJoyyIIzYBkVTliYs6QjV8v4V_Na7tHAmFt0vptfHK6PlkHeB3XCyeOQnQe8j2rvJnEBteHrA13P8NCCUn_9w/thumbnails/thumbnail.jpg?time=10.0s" class="css-14ogxpa" playsinline="" preload="metadata" muted="false" src="blob:https://embed.videodelivery.net/8f1b65c7-7c4f-4822-81cf-26757253cf8d"></video>

---

DeepMotion: Physically Simulated AI Agents | Can They Replace Stuntmen?
https://youtu.be/SIB760LoAGM


Basketball
https://blog.deepmotion.com/2018/08/07/deepdribble-simulating-basketball-with-ai/

---

https://dl.acm.org/doi/10.1145/3072959.3083723

---

https://deepmind.com/blog/article/producing-flexible-behaviours-simulated-environments

---

"Learning to drive in simulation offers a number of
benefits, including the ability to vary appearance, lighting
and weather conditions along with more structural varia-tions, such as curvature of the road and complexity of the
surrounding obstructions. It is also possible to construct
scenarios in simulation which are difficult (or dangerous) to
replicate in the real world."

- Learning to drive without labels

---

- Trajectory prediction
- Crowd simulations
- Training digital humans
  - worker ergonomics, eficiency, collaboration with robots
- Training robots to perform tasks in real life 

---

# Tools

- Nvidia Isaac
- http://gazebosim.org
- https://carla.org
- ML Agents (Unity)

---


Moreover, there are no guar-antees that the applied randomization would actually lead to a sensible real world policy as the design choices made in randomizing the parameters tend to be somewhat biased by the expertise of the practitioner. In this work, we apply a data-driven approach and use real world data to adapt sim-ulation randomization such that the behavior of the policies trained in simulation better matches their behavior in the real world. Therefore, starting with some initial distribution of the simulation parameters, we can perform learning in simulation and use real world roll-outs of learned policies to gradually change the simulation randomization such that the learned policies transfer better to the real world without requiring the exact replication of the real world scene in simulation.

"Closing the Sim-to-Real Loop:
Adapting Simulation Randomization with Real World Experience"

---


we aim at using a simulation
engine as a form of parameterized model that can help us to
embed prior knowledge about the world.


In addition, our approach does
not require estimating the reward in the real world, which
might be challenging if some of the reward components
can not be observed.

---



unsupervised transfer of an end-to-end driv-ing model from a simulated environment to a real vehicle.

This work goes beyond simple
image-to-image translation by making the desired task of
driving a differentiable component within a deep learning
architecture.


"Learning to Drive from Simulation without Real World Labels
Alex"

---

Domain adaptation seems to be an important technique for many of these works.
- How to reduce the effort to generate coeherent simulations?
  "Though our simulated city models rooftop obstacles accu-rately, future work is required to build rooftop models with a higher level of fidelity to cities such as Manhattan" – Realtime rooftop landing...

---

<!-- _class: topic -->
<!-- _paginate: false -->

# Wow! What's next?

---

# We made it!
##### Generation of synthetic data for machine learning

<br/>

#### 1. ~~Why does synthetic data matter?~~
#### 2. ~~How to generate synthetic data and train a model with it~~
#### 3. ~~Do they live in a simulation? Training models for dynamic environments~~

---
<!-- paginate: false -->
<!-- _class: invert -->
![bg](img/visgraf-background.jpeg)

# THANK YOU!

[hallpaz@impa.br](mailto:hallpaz@impa.br)

---

1. Why learn on simulations?
2. How to generate these simulations?
3. Techniques to train on simulation



 https://ai.googleblog.com/2017/10/closing-simulation-to-reality-gap-for.html
 "In this work, we compared the effect of using procedurally-generated and realistic objects from the ShapeNet model repository, and found that simply using random objects generated programmatically was not just sufficient for efficient experience transfer from simulation to reality, but also generalized better to the real world than using ShapeNet ones."

 "We further evaluate randomization as a way to provide generalization by separately evaluating the effect of using appearance randomization (randomly changing textures of different visual components of the virtual environment), and dynamics randomization (randomly changing object mass, and friction properties)"


"There are also a number of domain-specific developments that improve syn-thetic data generation for specific fields. For example, Cheung et al. [110]
present LCrowdV, a generation framework for crowd videos that combines a
procedural simulation framework that concentrates of movements and human
behaviour and a rendering framework for image/video generation, while An-derson et al. [19] develop a method for stochastic sampling-based simulation of
pedestrian trajectories (see Section 2.3)." [Survey, p52]


Closing the Sim-to-Real Loop: Adapting Simulation Randomization with Real World Experience
https://arxiv.org/abs/1810.05687 


Simulating many years of robotic interaction is quite feasible with modern parallel computing, physics simulation, and rendering technology. Moreover, the resulting data comes with automatically-generated annotations, which is particularly important for tasks where success is hard to infer automatically. The challenge with simulated training is that even the best available simulators do not perfectly capture reality. Models trained purely on synthetic data fail to generalize to the real world, as there is a discrepancy between simulated and real environments, in terms of both visual and physical properties. In fact, the more we increase the fidelity of our simulations, the more effort we have to expend in order to build them, both in terms of implementing complex physical phenomena and in terms of creating the content (e.g., objects, backgrounds) to populate these simulations. This difficulty is compounded by the fact that powerful optimization methods based on deep learning are exceptionally proficient at exploiting simulator flaws: the more powerful the machine learning algorithm, the more likely it is to discover how to "cheat" the simulator to succeed in ways that are infeasible in the real world. The question then becomes: how can a robot utilize simulation to enable it to perform useful tasks in the real world


Autonomous vehicles

# Time is an illusion

- Simulations can run faster than real-time


<iframe width="560" height="315" src="https://www.youtube.com/embed/jwSbzNHGflM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

# Imitation Learning


# Tools
- [PyBullet](https://docs.google.com/document/d/10sXEhzFRSnvFcl3XxNGhnD4N2SedqwdAvK3dsihxVUA/edit#heading=h.2ye70wns7io3)


---


drone applications include aerial photogra-phy, search and rescue, package delivery, and surveillance
will benefit.

Real-time confirmation that the rooftop is unoccupied and approach planning to the landing site are also necessary

---
Jeremy Castagno, Yu Yao and Ella Atkins. Realtime Rooftop Landing Site Identification and Selection in Urban City Simulation.