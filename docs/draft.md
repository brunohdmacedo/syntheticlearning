---
title: Rascunho
draft: true
---
# Synthetic Learning

ABSTRACT HERE

May 26th 2021 - What is synthetic learning and why does it matter?
June 2nd 2021 - How to generate synthetic data and train a model?
June 9th 2021 - Do they live in a simulation? Training models in dynamically synthetic environments

### What is it?
– To use synthetically generated data for training machine learning models

### What is machine learning?
– techinique to solve problems in which we design a model capable of estimating a function from data to achieve a desired result.

### Why use synthetic learning?
– because we don't have enough data

### DON'T HAVE ENOUGH DATA?

* give an idea of amount of data we produce on the internet today*

### BUT...

* For many cases, data must be annotated (expensive)
* Data ownership - privacy
* NOT ENOUGH data - self driving cars
* Dataset imbalacing - BIAS!
* Data democratization - build solutions outside big corps (Google, Facebook)

**Coded Bias?**

### Use cases
* Object detection and recognition
* Pose estimation
* Training Autonomous agents -  DIGITAL TWINS
 
- 
### Beforehand Questions

* How much realism do we need?
* Do we even need real data?
* How much effort to make it work well on real scenarios?
* How about the effort to generate synthetic data?
* Who is using it?

### Technical Discussions

#### Domain Randomization
– Contextutal distractors: objetcs similar to possible real scene elementos, positioned randomly but coherently

– Flying distractors: geometric shapes with random texture, size, and position

* Differential Privacy

### Challenges

* Differences in camera hardware

* Photorealistic data is still hard to generate (is it comparable to annotate??)

### Tools

– Unreal 
– Mujoco http://www.mujoco.org

-------

## A Study on the Impact of Domain Randomization for Monocular Deep 6DoF Pose Estimation

"The main issue arises from the fact that filming those
training sequences as well as **annotating** their ground truth
is generally a cumbersome, expensive, and time-consuming
task. Challenges include setting up and calibrating markers and
cameras to properly capture the ground truth [9]–[11], as well
as dealing with problems such as **camera noise, occlusions,
and motion blur**. Moreover, **a wide array of viewpoints** and
**rotation angles** must be covered, all while accounting for
**background, foreground, and illumination details**. Even then,
detection trained using those sequences might not work well
with different cameras or environments."


"It is worth noting that although these objects’ lack of
texturization makes them very suitable for AR, it also makes 
them more challenging, as they lack distinctive features and
can vary widely in terms of color, size, and specularity."

– linkar com dificuldades em simetria apresentada no vídeo do GTC


"NVIDIA also published their Deep learning Dataset Synthe-sizer (NDDS) [30], a UE4 plugin that can generate synthetic
data in real-time by randomizing illumination, objects, cam-eras, poses, textures, and distractors. The plugin can export
images, segmentations, depth maps, object pose annotations,
bounding boxes, keypoints, and custom stencils."


"Hinterstoisser et al. [35] proposed a strategy that generates
cluttered synthetic frames and trains a network to perform
2D detection of complex objects. Though the scenes are clut-tered, the technique guarantees that the objects of interest are
presented equally to the neural network in all scenarios. The
model trained with only synthetic data outperformed the model
trained with only real data. The authors also investigated
individual aspects of the image generation pipeline, which
revealed that blur and illumination color are the scene aspects
that influence results the most."

"The motivation being that photorealistic frames
(such as the ones from the FAT dataset) are hard to generate
and can be comparable in difficulty and time consumption to
recording and annotating real data, depending on the challenge
to be simulated. Thus, it is important to understand how the
simpler way (domain randomization) alone can impact results."


{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Check out the [Jekyll docs][Hinterstoisser-2019]

1. Hinterstoisser, S., Pauly, O., Heibel, H., Marek, M., & Bokeloh, M. (2019). An Annotation Saved is an Annotation Earned: Using Fully Synthetic Training for Object Instance Detection.

[Hinterstoisser-2019]: https://arxiv.org/abs/1902.09967
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/


– Autonomous vehicles

<!-- <video src="img/nerv_results.mp4" autoplay loop="true" poster="imagemprevia.jpg">
  Desculpa, o seu navegador não suporta vídeos incorporados,
  mas você pode <a href="videofile.ogg">baixá-lo</a>
  e assistir pelo seu reprodutor de mídia favorito!
</video> -->


# Research

### Create new **methods** to train machine learning models using less **computational power** and less **data**.

- Self-supervised learning
- Data augmentation
- **Synthetic data**


## How to build synthetic dataset?

* Media platforms
  * Simulators engines
  * Game Engines
  * Inside games themselves

<!-- Illustrate with examples; "we'll talk more about how to do it in the next lecture next week -->

# Closing the reality gap

One approach is to make the simulator closely match the physical reality by performing system identification and using high-quality rendering. Though using realistic RGB rendering alone has had limited success for transferring to real robotic tasks [16], incorporating realistic simulation of depth information can allow models trained on rendered images to transfer reasonably well to the real world [32]. Combining data from high-quality simulators with other approaches like fine-tuning can also reduce the number of labeled samples required in the real world

During training, the data generation process follows a curriculum strategy guaranteeing that all foreground models are preented to the network equally under all possible poses and conditions with increasing complexity. As a result, we en- tirely control the underlying statistics and we create optimal training samples at every stage of training. Using a set of 64 retail objects,

we demonstrate that our simple approach enables the training of detectors that outperform models trained with real data on a challenging evaluation dataset
---
# hintersoiser

The background generation method is designed follow-
ing three principles: maximize background clutter, mini- mize the risk of showing a network the same background image twice, and create background images with structures being similar in scale to the objects in the foreground layer. Our experiments indicate that these principles help to create training data which allows networks to learn the geomet- ric and visual appearance of objects while minimizing the chances of learning to distinguish synthetic foreground ob- jects from background objects simply from different prop- erties like e.g. different object sizes or noise distributions. The background layer is generated from a dataset of 15k

Key to the background generation is the size of the projected background objects, which is determined with respect to the size of the foreground object

For each background scene, we additionally convert each object’s texture into HSV space, randomly change the hue value and convert it back to RGB to diversify backgrounds and to make sure that background colors are well dis- tributed

- Occlusion layer


Thus, background, foreground and the occluding parts share
the same image properties which is contrary to other ap-proaches [10, 14, 22, 31, 20, 32] where real images and synthetic renderings are mixed. This makes it impossible for the network to differentiate foreground vs. background merely on attributes specific to their domain.

The amount of time spent for acquiring the real images was
around 10 hours and labeling required approximately 185
hours for the training set, with 6 additional hours spent for
correction. Note that for real data, acquisition and anno-tation efforts are always required if new objects are added
to the dataset, and images mixing the new objects and the
legacy objects need to be generated. In contrast, time spent
for scanning the 64 foreground objects was roughly 5 hours,
and this is a one time effort: if new objects are added to the
dataset, only one scan per additional object is required.

Number and shape of distractor objects on the table • Position and texture of all objects on the table • Textures of the table, floor, skybox, and robot • Position, orientation, and field of view of the camera • Number of lights in the scene • Position, orientation, and specular characteristics of the lights
• Type and amount of random noise added to images Since




# Adding more realism

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

---
Dilipkumar [148] applied SimGAN to improve handwriting recognition. They generated synthetic handwriting images and applied SimGAN to refine them, with significantly improved recognition of real handwriting after training on a hybrid datase

---



To reduce this gap, we propose Simulated+Unsupervised (S+U) learning, where the task is to learn a model to improve the realism of a simulator’s output using unlabeled real data, while preserving the annotation information from the simula- tor. We develop a method for S+U learning that uses an adversarial network similar to Generative Adversarial Networks (GANs), but with synthetic images as inputs instead ofrandom vectors. We make several key modifi- cations to the standard GAN algorithm to preserve an- notations, avoid artifacts, and stabilize training: (i) a ‘self-regularization’ term, (ii) a local adversarial loss, and (iii) updating the discriminator using a history of refined images. We show that this enables generation of highly realistic images, which we demonstrate both qualitatively and with a user study. We quantitatively evaluate the generated images by training models for gaze estimation and hand pose estimation. We show a significant improvement over using synthetic images, and achieve state-of-the-art results on the MPIIGaze dataset without any labeled real data.


Finally, a note of caution: GAN-based refinement is not the only way to go.
Kan et al. [304] compared three approaches to data augmentation for pupil center point detection, an important subproblem in gaze estimation: affine trans- formations of real images, synthetic images from UnityEyes, and GAN-based refinement. In their experiments, real data augmentation with affine transfor- mations was a clear winner, with the GAN improving over UnityEyes but falling short of the augmented real dataset.
This is one example of a general common
wisdom: in cases where a real dataset is available, one should squeeze out all
the information available in it and apply as much augmentation as possible,
regardless of whether the dataset is augmented with synthetic data or not.


---



