# Places2-CNNs

Li Shen ([VGG, University of Oxford](http://www.robots.ox.ac.uk/~vgg/)), 
[Zhouchen Lin](http://www.cis.pku.edu.cn/faculty/vision/zlin/zlin.htm) (Peking University), 
Gang Sun ([Momenta](http://momenta.ai)), Jie Hu ([Momenta](http://momenta.ai)).

Email: lishen@robots.ox.ac.uk; sungang@momenta.ai

### Table of Contents
0. [Introduction](#introduction)
0. [Citation](#citation)
0. [Model performance](#model-performance)
0. [Acknowledgements and License](#acknowledgements-and-license)

### Introduction

This repository contains the two models (Places2-401-CNN and Places2-365-CNN). Places2-401-CNN is described in the paper "Relay Backpropagation for Effective Learning of Deep Convolutional Neural Networks", which is referred as "Model B". This model is trained for 401 scene categories in Places2 Challenge 2015. Places2-365-CNN is a ResNet-like model that we respectively add 5 and 4 building blocks on 56x56 and 28x28 feature maps and remove 13 building blocks on 14x14 feature map of ResNet-152. This model is trained for 365 categories in Places2 Chanllenge 2016. These two models are used in [ILSVRC 2015 competitions](http://image-net.org/challenges/LSVRC/2015/) and [ILSVRC 2016 competitions](http://image-net.org/challenges/LSVRC/2016/). Our WM & MW team won the [1st place](http://places2.csail.mit.edu/results2015.html) and the [2nd place](http://places2.csail.mit.edu/results2016.html) in the Scene Classification Challenge, respectively.

### Citation

If you use these models in your research, please cite:

    @inproceedings{Li2016,
        author = {Li Shen and Zhouchen Lin and Qingming Huang},
        title = {Relay Backpropagation for Effective Learning of Deep Convolutional Neural Networks},
        booktitle = {European Conference on Computer Vision (ECCV)},
        year = {2016}
    }
	@article{Xudong2014,
		author = {Xudong Cao},
		title = {A Practical Theory for Designing Very Deep Convolutional Neural Networks},
		journal = {Technical Report},
		year = {2014}
	} 

### Model Performance

0. 1-crop validation error (center 224x224 crop from resized 256x256 image):

	Model|Challenge|Top-1|Top-5
    :---:|:---:|:---:|:---:|
    Places2-401-CNN|Places2 challenge 2015|49.74%|17.83%|
    Places2-365-CNN|Places2 challenge 2016|41.07%|11.48%|

1. Model ensemble test error:

    Model|Challenge|Rank|Top-5
    :---:|:---:|:---:|:---:|
    Places2-401-CNNs|Places2 challenge 2015|1st|16.87%|
    Places2-365-CNNs|Places2 challenge 2016|2nd|10.19%|
	
### Acknowledgements and License

We would like to thank [Xudong Cao](https://scholar.google.com/citations?user=H6E_VnoAAAAJ&hl=zh-CN) for the helpful discussion on network architectures.

Models are released under the Simplified BSD License for non-commercial use (refer to the LICENSE file for details).
