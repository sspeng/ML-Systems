# Convolutional Neural Networks

- [ImageNet Models](#imagenet-models)  
- [Architecture Design](#architecture-design)
- [Activation Functions](#activation-functions)
- [Visualization](#visualization)
- [Fast Convolution](#fast-convolution)
- [Low-Rank Filter Approximation](#low-rank-filter-approximation)
- [Low Precision](#low-precision)  
- [Parameter Pruning](#parameter-pruning)  
- [Transfer Learning](#transfer-learning)  
- [Theory](#theory)
- [3D Data](#3d-data)
- [Hardware](#hardware)  

## ImageNet Models  
- 2017 CVPR [Xception: Deep Learning with Depthwise Separable Convolutions](http://openaccess.thecvf.com/content_cvpr_2017/papers/Chollet_Xception_Deep_Learning_CVPR_2017_paper.pdf)(Xception)  
- 2017 CVPR [Aggregated Residual Transformations for Deep Neural Networks](https://arxiv.org/pdf/1611.05431.pdf) (ResNeXt)  
- 2016 ECCV [Identity Mappings in Deep Residual Networks](https://arxiv.org/abs/1603.05027) (Pre-ResNet)   
- 2016 arXiv [Inception-v4, Inception-ResNet and the Impact of Residual Connections on Learning](http://arxiv.org/abs/1602.07261) (Inception V4)  
- 2016 CVPR [Deep Residual Learning for Image Recognition](http://arxiv.org/abs/1512.03385) (ResNet)     
- 2015 arXiv [Rethinking the Inception Architecture for Computer Vision](http://arxiv.org/abs/1512.00567) (Inception V3)  
- 2015 ICML [Batch Normalization: Accelerating Deep Network Training by Reducing Internal Covariate Shift](http://jmlr.org/proceedings/papers/v37/ioffe15.pdf) (Inception V2)  
- 2015 ICCV [Delving Deep into Rectifiers: Surpassing Human-Level Performance on ImageNet Classification](http://research.microsoft.com/en-us/um/people/kahe/publications/iccv15imgnet.pdf) (PReLU)  
- 2015 ICLR [Very Deep Convolutional Networks For Large-scale Image Recognition](http://arxiv.org/abs/1409.1556) (VGG)  
- 2015 CVPR [Going Deeper with Convolutions](http://static.googleusercontent.com/media/research.google.com/en//pubs/archive/43022.pdf) (GoogleNet/Inception V1)   
- 2012 NIPS [ImageNet Classification with Deep Convolutional Neural Networks](http://papers.nips.cc/paper/4824-imagenet-classification-with-deep-convolutional-neural-networks.pdf) (AlexNet)  

## Architecture Design
- 2017 arXiv [One Model To Learn Them All](https://arxiv.org/abs/1706.05137)  
- 2017 arXiv [MobileNets: Efficient Convolutional Neural Networks for Mobile Vision Applications](https://arxiv.org/abs/1704.04861)  
- 2017 ICML [AdaNet: Adaptive Structural Learning of Artificial Neural Networks](https://arxiv.org/pdf/1607.01097.pdf)  
- 2017 ICML [Large-Scale Evolution of Image Classifiers](https://arxiv.org/abs/1703.01041)  
- 2017 CVPR [Aggregated Residual Transformations for Deep Neural Networks](https://arxiv.org/pdf/1611.05431.pdf)  
- 2017 CVPR [Densely Connected Convolutional Networks](http://arxiv.org/abs/1608.06993)  
- 2017 ICLR [Outrageously Large Neural Networks: The Sparsely-Gated Mixture-of-Experts Layer](https://openreview.net/pdf?id=B1ckMDqlg)  
- 2017 ICLR [Neural Architecture Search with Reinforcement Learning](https://openreview.net/pdf?id=r1Ue8Hcxg)  
- 2017 ICLR [Designing Neural Network Architectures using Reinforcement Learning](https://openreview.net/pdf?id=S1c2cvqee)  
- 2017 ICLR [Do Deep Convolutional Nets Really Need to be Deep and Convolutional?](https://arxiv.org/abs/1603.05691)  
- 2017 ICLR [Highway and Residual Networks learn Unrolled Iterative Estimation](https://arxiv.org/pdf/1612.07771.pdf)  
- 2016 NIPS [Residual Networks Behave Like Ensembles of Relatively Shallow Networks](https://arxiv.org/abs/1605.06431)  
- 2016 BMVC [Wide Residual Networks](http://arxiv.org/abs/1605.07146)  
- 2016 arXiv [Benefits of depth in neural networks](http://arxiv.org/abs/1602.04485)  
- 2016 AAAI [On the Depth of Deep Neural Networks: A Theoretical View](http://arxiv.org/abs/1506.05232)  
- 2016 arXiv [SqueezeNet: AlexNet-level accuracy with 50x fewer parameters and <1MB model size](http://arxiv.org/abs/1602.07360)  
- 2015 ICMLW [Highway Networks](http://arxiv.org/pdf/1505.00387v2.pdf)  
- 2015 CVPR [Convolutional Neural Networks at Constrained Time Cost](http://www.cv-foundation.org/openaccess/content_cvpr_2015/papers/He_Convolutional_Neural_Networks_2015_CVPR_paper.pdf)   
- 2015 CVPR [Fully Convolutional Networks for Semantic Segmentation](https://people.eecs.berkeley.edu/~jonlong/long_shelhamer_fcn.pdf)  
- 2014 NIPS [Do Deep Nets Really Need to be Deep?](http://papers.nips.cc/paper/5484-do-deep-nets-really-need-to-be-deep.pdf)  
- 2014 ICLRW [Understanding Deep Architectures using a Recursive Convolutional Network](http://arxiv.org/abs/1312.1847)  
- 2013 ICML [Making a Science of Model Search: Hyperparameter Optimization in Hundreds of Dimensions for Vision Architectures](http://jmlr.org/proceedings/papers/v28/bergstra13.pdf)  
- 2009 ICCV [What is the Best Multi-Stage Architecture for Object Recognition?](http://yann.lecun.com/exdb/publis/pdf/jarrett-iccv-09.pdf)   
- 1995 NIPS [Simplifying Neural Nets by Discovering Flat Minima](https://papers.nips.cc/paper/899-simplifying-neural-nets-by-discovering-flat-minima.pdf)  
- 1994 T-NN [SVD-NET: An Algorithm that Automatically Selects Network Structure](http://ieeexplore.ieee.org/xpl/articleDetails.jsp?reload=true&arnumber=286929)  

## Activation Functions
- 2017 arXiv [Self-Normalizing Neural Networks](https://arxiv.org/abs/1706.02515) (SELU)  
- 2016 ICLR [Fast and Accurate Deep Network Learning by Exponential Linear Units (ELUs)](https://arxiv.org/pdf/1511.07289.pdf) (ELU)  
- 2015 arXiv [Empirical Evaluation of Rectified Activations in Convolutional Network](https://arxiv.org/pdf/1505.00853.pdf) (RReLU)
- 2015 ICCV [Delving Deep into Rectifiers: Surpassing Human-Level Performance on ImageNet Classification](http://research.microsoft.com/en-us/um/people/kahe/publications/iccv15imgnet.pdf) (PReLU)
- 2013 ICML [Rectifier Nonlinearities Improve Neural Network Acoustic Models](https://pdfs.semanticscholar.org/367f/2c63a6f6a10b3b64b8729d601e69337ee3cc.pdf)  
- 2010 ICML [Rectified Linear Units Improve Restricted Boltzmann Machines](http://www.cs.toronto.edu/~fritz/absps/reluICML.pdf) (ReLU)  

## Visualization  
- 2017 CVPR [Network Dissection: Quantifying Interpretability of Deep Visual Representations](http://netdissect.csail.mit.edu/final-network-dissection.pdf)  
- 2015 ICMLW [Understanding Neural Networks Through Deep Visualization](http://yosinski.com/media/papers/Yosinski__2015__ICML_DL__Understanding_Neural_Networks_Through_Deep_Visualization__.pdf)  
- 2014 ECCV [Visualizing and Understanding Convolutional Networks](https://www.cs.nyu.edu/~fergus/papers/zeilerECCV2014.pdf)  

## Fast Convolution
- 2017 ICML [Warped Convolutions: Efficient Invariance to Spatial Transformations](https://arxiv.org/pdf/1609.04382.pdf)  
- 2017 ICLR [Faster CNNs with Direct Sparse Convolutions and Guided Pruning](https://openreview.net/pdf?id=rJPcZ3txx)  
- 2016 NIPS [PerforatedCNNs: Acceleration through Elimination of Redundant Convolutions](http://arxiv.org/abs/1504.08362)  
- 2016 CVPR [Fast Algorithms for Convolutional Neural Networks](http://www.cv-foundation.org/openaccess/content_cvpr_2016/papers/Lavin_Fast_Algorithms_for_CVPR_2016_paper.pdf) (Winograd)  
- 2015 CVPR [Sparse Convolutional Neural Networks](http://www.cv-foundation.org/openaccess/content_cvpr_2015/papers/Liu_Sparse_Convolutional_Neural_2015_CVPR_paper.pdf)  

## Low-Rank Filter Approximation
- 2016 ICLR [Convolutional Neural Networks with Low-rank Regularization](https://arxiv.org/abs/1511.06067)  
- 2016 ICLR [Training CNNs with Low-Rank Filters for Efficient Image Classification](http://arxiv.org/abs/1511.06744)  
- 2016 TPAMI [Accelerating Very Deep Convolutional Networks for Classification and Detection](https://arxiv.org/abs/1505.06798)  
- 2015 CVPR [Efficient and Accurate Approximations of Nonlinear Convolutional Networks](http://www.cv-foundation.org/openaccess/content_cvpr_2015/papers/Zhang_Efficient_and_Accurate_2015_CVPR_paper.pdf)  
- 2015 ICLR [Speeding-up convolutional neural networks using fine-tuned cp-decomposition](https://arxiv.org/pdf/1412.6553v3.pdf)  
- 2014 NIPS [Exploiting Linear Structure Within Convolutional Networks for Efficient Evaluation](http://papers.nips.cc/paper/5544-exploiting-linear-structure-within-convolutional-networks-for-efficient-evaluation.pdf)  
- 2014 BMVC [Speeding up Convolutional Neural Networks with Low Rank Expansions](https://arxiv.org/abs/1405.3866)  
- 2013 NIPS [Predicting Parameters in Deep Learning](https://papers.nips.cc/paper/5025-predicting-parameters-in-deep-learning.pdf)  
- 2013 CVPR [Learning Separable Filters](http://cvlabwww.epfl.ch/~lepetit/papers/rigamonti_cvpr13.pdf)  

## Low Precision  
- 2017 arXiv [BitNet: Bit-Regularized Deep Neural Networks](https://arxiv.org/pdf/1708.04788.pdf)  
- 2017 arXiv [Gradient Descent for Spiking Neural Networks](https://arxiv.org/abs/1706.04698)  
- 2017 arXiv [ShiftCNN: Generalized Low-Precision Architecture for Inference of Convolutional Neural Networks](https://arxiv.org/abs/1706.02393)  
- 2017 arXiv [Gated XNOR Networks: Deep Neural Networks with Ternary Weights and Activations under a Unified Discretization Framework](https://arxiv.org/abs/1705.09283)  
- 2017 arXiv [The High-Dimensional Geometry of Binary Neural Networks](https://arxiv.org/pdf/1705.07199.pdf)  
- 2017 NIPS [Training Quantized Nets: A Deeper Understanding](https://arxiv.org/abs/1706.02379)  
- 2017 NIPS [TernGrad: Ternary Gradients to Reduce Communication in Distributed Deep Learning](https://arxiv.org/abs/1705.07878)  
- 2017 ICML [Analytical Guarantees on Numerical Precision of Deep Neural Networks](http://proceedings.mlr.press/v70/sakr17a/sakr17a.pdf)  
- 2017 arXiv [Deep Learning with Low Precision by Half-wave Gaussian Quantization](https://arxiv.org/abs/1702.00953)    
- 2017 CVPR [Network Sketching: Exploiting Binary Structure in Deep CNNs](https://arxiv.org/pdf/1706.02021.pdf)  
- 2017 CVPR [Local Binary Convolutional Neural Networks](http://openaccess.thecvf.com/content_cvpr_2017/papers/Juefei-Xu_Local_Binary_Convolutional_CVPR_2017_paper.pdf)  
- 2017 ICLR [Towards the Limit of Network Quantization](https://openreview.net/pdf?id=rJ8uNptgl)  
- 2017 ICLR [Loss-aware Binarization of Deep Networks](https://openreview.net/pdf?id=S1oWlN9ll)  
- 2017 ICLR [Trained Ternary Quantization](https://openreview.net/pdf?id=S1_pAu9xl)  
- 2017 ICLR [Incremental Network Quantization: Towards Lossless CNNs with Low-precision Weights](https://openreview.net/pdf?id=HyQJ-mclg)  
- 2016 arXiv [Quantized Neural Networks: Training Neural Networks with Low Precision Weights and Activations](https://arxiv.org/abs/1609.07061)  
- 2016 arXiv [Accelerating Deep Convolutional Networks using low-precision and sparsity](https://arxiv.org/abs/1610.00324)  
- 2016 arXiv [Deep neural networks are robust to weight binarization and other non-linear distortions](https://arxiv.org/pdf/1606.01981.pdf)  
- 2016 ECCV [XNOR-Net: ImageNet Classification Using Binary Convolutional Neural Networks](https://arxiv.org/pdf/1603.05279.pdf)  
- 2016 ICMLW [Overcoming Challenges in Fixed Point Training of Deep Convolutional Networks](https://arxiv.org/pdf/1607.02241.pdf)  
- 2016 ICML [Fixed Point Quantization of Deep Convolutional Networks](http://jmlr.org/proceedings/papers/v48/linb16.pdf)  
- 2016 NIPS [Binarized Neural Networks](https://papers.nips.cc/paper/6573-binarized-neural-networks.pdf)  
- 2016 arXiv [Binarized Neural Networks: Training Deep Neural Networks with Weights and Activations Constrained to +1 or -1](http://arxiv.org/abs/1602.02830)  
- 2016 CVPR [Quantized Convolutional Neural Networks for Mobile Devices](http://www.cv-foundation.org/openaccess/content_cvpr_2016/papers/Wu_Quantized_Convolutional_Neural_CVPR_2016_paper.pdf)  
- 2016 ICLR [Neural Networks with Few Multiplications](https://arxiv.org/abs/1510.03009)   
- 2015 arXiv [Resiliency of Deep Neural Networks under Quantization](https://arxiv.org/abs/1511.06488)  
- 2015 arXiv [Rounding Methods for Neural Networks with Low Resolution Synaptic Weights](https://arxiv.org/abs/1504.05767)  
- 2015 NIPS [Backpropagation for Energy-Efficient Neuromorphic Computing](https://papers.nips.cc/paper/5862-backpropagation-for-energy-efficient-neuromorphic-computing.pdf)  
- 2015 NIPS [BinaryConnect: Training Deep Neural Networks with Binary Weights during Propagations](https://papers.nips.cc/paper/5647-binaryconnect-training-deep-neural-networks-with-binary-weights-during-propagations.pdf)  
- 2015 ICMLW [Bitwise Neural Networks](http://minjekim.com/papers/icml2015_mkim.pdf)  
- 2015 ICML [Deep Learning with Limited Numerical Precision](http://www.jmlr.org/proceedings/papers/v37/gupta15.pdf)  
- 2015 ICLRW [Training deep neural networks with low precision multiplications](https://arxiv.org/abs/1412.7024)    
- 2015 arXiv [Training Binary Multilayer Neural Networks for Image Classification using Expectation Backpropagation](https://arxiv.org/abs/1503.03562)   
- 2014 NIPS [Expectation Backpropagation: Parameter-Free Training of Multilayer Neural Networks with Continuous or Discrete Weights](https://papers.nips.cc/paper/5269-expectation-backpropagation-parameter-free-training-of-multilayer-neural-networks-with-continuous-or-discrete-weights.pdf)  
- 2013 arXiv [Estimating or Propagating Gradients Through Stochastic Neurons for Conditional Computation](https://arxiv.org/pdf/1308.3432.pdf)  
- 2011 NIPSW [Improving the speed of neural networks on CPUs](http://static.googleusercontent.com/media/research.google.com/en//pubs/archive/37631.pdf)  
- 1987 Combinatorica [Randomized rounding: A technique for provably good algorithms and algorithmic proofs](https://www.cs.auckland.ac.nz/~cthombor/Pubs/RandomRounding/RandomRounding1987.pdf)  

## Parameter Pruning  
- 2017 ICML [Beyond Filters: Compact Feature Map for Portable Deep Model](http://proceedings.mlr.press/v70/wang17m/wang17m.pdf)  
- 2017 ICLR [Soft Weight-Sharing for Neural Network Compression](https://openreview.net/pdf?id=HJGwcKclx)  
- 2017 ICLR [Pruning Convolutional Neural Networks for Resource Efficient Inference](https://openreview.net/pdf?id=SJGCiw5gl)  
- 2017 ICLR [Pruning Filters for Efficient ConvNets](https://openreview.net/pdf?id=rJqFGTslg)  
- 2016 arXiv [Designing Energy-Efficient Convolutional Neural Networks using Energy-Aware Pruning](https://arxiv.org/abs/1611.05128)  
- 2016 arXiv [Network Trimming: A Data-Driven Neuron Pruning Approach towards Efficient Deep Architectures](https://arxiv.org/abs/1607.03250)  
- 2016 NIPS [Learning the Number of Neurons in Deep Networks](https://rsu.forge.nicta.com.au/people/jalvarez/LNN/AlvarezSalzmannNIPS16.pdf)  
- 2016 NIPS [Learning Structured Sparsity in Deep Learning](https://arxiv.org/abs/1608.03665) \[[code](https://github.com/wenwei202/caffe/tree/scnn)\]  
- 2016 NIPS [Dynamic Network Surgery for Efficient DNNs](http://128.84.21.199/abs/1608.04493)  
- 2016 ECCV [Less is More: Towards Compact CNNs](https://static-content.springer.com/esm/chp%3A10.1007%2F978-3-319-46493-0_40/MediaObjects/419976_1_En_40_MOESM1_ESM.pdf)  
- 2016 CVPR [Fast ConvNets Using Group-wise Brain Damage](http://www.cv-foundation.org/openaccess/content_cvpr_2016/papers/Lebedev_Fast_ConvNets_Using_CVPR_2016_paper.pdf)  
- 2016 ICLR [Deep Compression: Compressing Deep Neural Networks with Pruning, Trained Quantization and Huffman Coding](http://arxiv.org/abs/1510.00149)  
- 2016 ICLR [Compression of Deep Convolutional Neural Networks for Fast and Low Power Mobile Applications](http://arxiv.org/abs/1511.06530)
- 2015 arXiv [Structured Pruning of Deep Convolutional Neural Networks](http://arxiv.org/abs/1512.08571)  
- 2015 IEEE Access [Channel-Level Acceleration of Deep Face Representations](http://ieeexplore.ieee.org/document/7303876/)  
- 2015 BMVC [Data-free parameter pruning for Deep Neural Networks](http://arxiv.org/abs/1507.06149)
- 2015 ICML [Compressing Neural Networks with the Hashing Trick](http://jmlr.org/proceedings/papers/v37/chenc15.pdf)   
- 2015 ICCV [Deep Fried Convnets](http://www.cv-foundation.org/openaccess/content_iccv_2015/papers/Yang_Deep_Fried_Convnets_ICCV_2015_paper.pdf)  
- 2015 ICCV [An Exploration of Parameter Redundancy in Deep Networks with Circulant Projections](http://felixyu.org/pdf/ICCV15_circulant.pdf)  
- 2015 NIPS [Learning both Weights and Connections for Efficient Neural Networks](http://arxiv.org/abs/1506.02626)    
- 2015 ICLR [FitNets: Hints for Thin Deep Nets](http://arxiv.org/pdf/1412.6550v4.pdf)  
- 2014 arXiv [Compressing Deep Convolutional Networks using Vector Quantization](http://arxiv.org/abs/1412.6115)  
- 2014 NIPSW [Distilling the Knowledge in a Neural Network](https://arxiv.org/abs/1503.02531)   
- 1995 ISANN [Evaluating Pruning Methods](http://publications.idiap.ch/downloads/papers/1995/thimm-pruning-hop.pdf)  
- 1993 T-NN [Pruning Algorithms--A Survey](http://axon.cs.byu.edu/~martinez/classes/678/Papers/Reed_PruningSurvey.pdf)  
- 1989 NIPS [Optimal Brain Damage](http://yann.lecun.com/exdb/publis/pdf/lecun-90b.pdf)  

## Transfer Learning  
- 2016 arXiv [What makes ImageNet good for transfer learning?](https://arxiv.org/abs/1608.08614)  
- 2014 NIPS [How transferable are features in deep neural networks?](https://arxiv.org/pdf/1411.1792v1.pdf)  
- 2014 CVPR [CNN Features off-the-shelf: an Astounding Baseline for Recognition](http://www.cv-foundation.org/openaccess/content_cvpr_workshops_2014/W15/papers/Razavian_CNN_Features_Off-the-Shelf_2014_CVPR_paper.pdf)  
- 2014 ICML [DeCAF: A Deep Convolutional Activation](http://proceedings.mlr.press/v32/donahue14.pdf)  

## Theory
- 2017 ICML [On the Expressive Power of Deep Neural Networks](https://arxiv.org/pdf/1606.05336v6.pdf)  
- 2017 ICML [A Closer Look at Memorization in Deep Networks](https://arxiv.org/pdf/1706.05394.pdf)  
- 2017 ICML [An Analytical Formula of Population Gradient for two-layered ReLU network and its Applications in Convergence and Critical Point Analysis](https://arxiv.org/pdf/1703.00560.pdf)  
- 2016 NIPS [Exponential expressivity in deep neural networks through transient chaos](https://papers.nips.cc/paper/6322-exponential-expressivity-in-deep-neural-networks-through-transient-chaos.pdf)  
- 2016 arXiv [Understanding Deep Convolutional Networks](https://arxiv.org/pdf/1601.04920.pdf)  
- 2014 NIPS [On the number of linear regions of deep neural networks](http://papers.nips.cc/paper/5422-on-the-number-of-linear-regions-of-deep-neural-networks.pdf)
- 2014 ICML [Provable Bounds for Learning Some Deep Representations](http://proceedings.mlr.press/v32/arora14.pdf)  
- 2014 ICLR [On the number of response regions of deep feed forward networks with piece-wise linear activations](https://arxiv.org/pdf/1312.6098.pdf)   
- 2014 ICLR [Revisiting natural gradient for deep networks](https://arxiv.org/pdf/1301.3584.pdf)  

## 3D Data
- 2017 NIPS [PointNet++: Deep Hierarchical Feature Learning on Point Sets in a Metric Space](https://arxiv.org/pdf/1706.02413.pdf)  
- 2017 ICCV [Octree Generating Networks: Efficient Convolutional Architectures for High-resolution 3D Outputs](https://arxiv.org/pdf/1703.09438.pdf)  
- 2017 SIGGRAPH [O-CNN: Octree-based Convolutional Neural Network for Understanding 3D Shapes](http://wang-ps.github.io/O-CNN_files/CNN3D.pdf)  
- 2017 CVPR [PointNet: Deep Learning on Point Sets for 3D Classification and Segmentation](https://arxiv.org/pdf/1612.00593.pdf)  
- 2017 CVPR [OctNet: Learning Deep 3D Representations at High Resolutions](https://arxiv.org/pdf/1611.05009.pdf)  
- 2016 NIPS [FPNN: Field Probing Neural Networks for 3D Data](https://papers.nips.cc/paper/6416-fpnn-field-probing-neural-networks-for-3d-data.pdf)  
- 2016 NIPS [Learning a Probabilistic Latent Space of Object Shapes via 3D Generative-Adversarial Modeling](https://jiajunwu.com/papers/3dgan_nips.pdf)  
- 2015 ICCV [Multi-view Convolutional Neural Networks for 3D Shape Recognition](http://www.cv-foundation.org/openaccess/content_iccv_2015/papers/Su_Multi-View_Convolutional_Neural_ICCV_2015_paper.pdf)  
- 2015 BMVC [Sparse 3D convolutional neural networks](http://www.bmva.org/bmvc/2015/papers/paper150/paper150.pdf)  
- 2015 CVPR [3D ShapeNets: A Deep Representation for Volumetric Shapes](http://3dshapenets.cs.princeton.edu/paper.pdf)  

## Hardware
- 2017 ISVLSI [YodaNN: An ultra-low power convolutional neural network accelerator based on binary weights](https://arxiv.org/pdf/1606.05487.pdf)  
- 2017 ASPLOS [SC-DCNN: Highly-Scalable Deep Convolutional Neural Network using Stochastic Computing](https://arxiv.org/pdf/1611.05939.pdf)  
- 2017 FPGA [Can FPGAs Beat GPUs in Accelerating Next-Generation Deep Neural Networks](http://jaewoong.org/pubs/fpga17-next-generation-dnns.pdf)  
- 2015 NIPS Tutorial [High-Performance Hardware for Machine Learning](https://media.nips.cc/Conferences/2015/tutorialslides/Dally-NIPS-Tutorial-2015.pdf)  
