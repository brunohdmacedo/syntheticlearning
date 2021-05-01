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

