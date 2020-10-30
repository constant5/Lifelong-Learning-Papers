# Continual Lifelong Learning Papers

Contributed by Constant Marks. 

## [Content](#content)

<table>
<tr><td colspan="2"><a href="#survey-papers">1. Survey</a></td></tr> 
<tr><td colspan="2"><a href="#models">2. Models</a></td></tr>
<tr>
    <td>&emsp;<a href="#Regularization-Approach">2.1 Regularization Approach</a></td>
</tr>
    <td>&emsp;<a href="#Dynamic-Architecture">2.4 Dynamic Architecture</a></td>
</tr>
<tr>
    <td>&emsp;<a href="#Complementary-System-and-Replay">2.5 Complementary System and Replay</a></td>
    <td>&ensp;<a href="#placeholder"></a></td>
</tr>

<tr><td colspan="2"><a href="#datasets">3. Datasets</a></td></tr> 
<tr>
    <td>&emsp;<a href="#MNIST">3.1 MNIST</a></td>
    <td>&ensp;<a href="#CUB-200">3.2 CUB-200</a></td>
</tr>
<tr>
    <td>&emsp;<a href="#AudioSet">3.3 AudioSet</a></td>
    <td>&ensp;<a href="#Core50">3.4 Core50</a></td>
</tr>
<tr>
    <td>&emsp;<a href="#AudioSet">3.5 iCIFAR-100</a></td>
    <td>&ensp;<a href="#"></a></td>
</tr> 

<tr><td colspan="2"><a href="#applications">4. Applications</a></td></tr> 
<tr>
    <td>&emsp;<a href="#placeholder2">4.1 placeholder2</a></td>
    <td>&ensp;<a href="#placeholder3">4.2 placeholder3</a></td>
</tr> 
</table>

## [Survey papers](#content)
1. **Continual Lifelong Learning with Neural Networks: A Review.** arXiv 2018. 
\
*Parisi, G. et al.* [paper](https://arxiv.org/pdf/1802.07569.pdf)

1. **Lifelong Machine Learning Systems: Beyond Learning Algorithms** AAAI 2013 
\
*Silver, D., Yang, Q., Li, L.* [paper](https://www.researchgate.net/profile/Daniel_Silver/post/Lifelong_Machine_Learning-how_important_do_you_feel_it_will_be_to_AI/attachment/59d61d9d79197b80779788c9/AS:271835600490496@1441822065030/download/Silver_Yang_AAAI_LML_Symposium.pdf)

1. **Learning in nonstationary environments:A survey** IEEE Computational Intelligence Magazine 2015. 
\
*Ditzler, G. et al.* [paper](https://www.academia.edu/download/45784580/2015_-_Learning_in_Nonstationary_Environments_-_A_Survey_-_IEEE_CIM.pdf)

1. **The stability-plasticity dilemma: Investigating the continuum from catastrophic forgetting to age-limited learning effects** Frontiers in Psychology 2013. 
\
*Mermillod, M. et al* [paper]()

## [Models](#content)


### [Lifelong Learning Models](#content) to be sorted

1. **ELLA: An Efficient Lifelong Learning Algorithm** PMLR 2013. [paper](http://proceedings.mlr.press/v28/ruvolo13.pdf)

1. **Selective Experience Replay for Lifelong Learning** arXiv 2018. [paper](https://arxiv.org/pdf/1802.10269.pdf)
)

### [Regularization Approach](#content)

#### These may be further divided into architectural, functional, and structural (see Zenke et al.)

#### **Architectural**

*Alter architecture to reduce interference between tasks (w/o altering the objective function) i.e. freezing certain weights, reducing lr for shared layers, using different nonlinearities, injecting noise, save and copy. These techniques have the inherent feature that they do not forget previously acquired knowledge but they have little capability to adapt to new domains.* 

1. **CNN features off-the-shelf: An astounding baseline for recognition** CVPR 2014. \
\
*Razavian, A. S, et al.* [paper](https://www.cv-foundation.org/openaccess/content_cvpr_workshops_2014/W15/papers/Razavian_CNN_Features_Off-the-Shelf_2014_CVPR_paper.pdf)

1. **Decaf: A deep convolutional activation feature for generic visual recognition.** ICML 2014. \
\
*Donahue, J. et al.* [paper](http://www.jmlr.org/proceedings/papers/v32/donahue14.pdf) 

#### **Functional**

*Add a regularization term to the objective function that penalizes changes from old to new. Typically some version of L2 regularization.*

1. **LwF Model - Learning without Forgetting**  IEEE Transactions on Pattern Analysis and Machine Intelligence 2018.
\
*Li, Z. & Hoiem, D* [paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8107520)

1. **LF Model - Less-forgetting learning in deep neural networks.** AAAI 2018.
\
*Jung, H. et al.* [paper](https://arxiv.org/pdf/1607.00122)


#### **Structural**
*Penalty on the parameters to encourage them to stay close to values for old task.  Usually based on stability plasticity model of to preserve "important" weights.* 


1. **EWC Model - Overcoming catastrophic forgetting in neural networks.** PNAS 2017 TNN 1997. 
\
*Kirkpatrick, J. et al.* [paper](https://www.pnas.org/content/pnas/114/13/3521.full.pdf)

1. **SI Model - Continual learning through synaptic intelligence.** ICML 2017.
\
*Zenke, F., Poole, B. & Ganguli, S.* [paper](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6944509/)


#### **Feature Extraction Models**

1. **Continuous learning in single-incremental-task scenarios.** arXiv 2018. 
\
*Maltoni, D. & Lomonaco, V.* [paper](https://arxiv.org/pdf/2005.04167)

#### **Ensemble Models**

1.  **Life-long learning based on dynamic combination model.** Applied Soft Computing 2017.\
This paper is a good example of an ensemble approach that combines the results of multiple sub-classifiers using a fixed size decision tree to create a non-linear combination of sub-classifiers.  This approach is similar to other boosting models (Learn++, TradaBoots, AWE) and can in thoery be applied to any base classifier. 
\
*Ren, B. et al.* [paper](https://www.sciencedirect.com/science/article/abs/pii/S156849461730128X)

1. **Ensemble learning in fixed expansion layer networks for mitigating catastrophic forgetting** IEEE Transactions on Neural Networks and Learning Systems 2013. 
\
*Coop, R., Mishtal, A. & Arel, I.* [paper](http://web.eecs.utk.edu/~ielhanan/Papers/TNNLS_Coop_2013.pdf)

#### **Genetic Algorithm**

1. **Pathnet: Evolution channels gradient descent in super neural networks** arXiv 2017.\
Pathnet guides the training of a NN with a genetic algorithm that initializes a population of weight parameters and then after training for some epochs selects the best model, and then creates another population by perturbing the weights of unimportant parameters. \
\
I think this could be any interesting approach to effectively explore the loss function and retain information about other suitable local minima. 
\
*Fernando, C. st al.* [paper](https://arxiv.org/pdf/1701.08734)


### [Dynamic Architecture](#content)

#### Static Image Classification

1. **Progressive neural networks** arXiv 2016. *Rusu et al.*\
Block any changes to the network trained on previous
knowledge and expand the architecture by allocating novel sub-networks with fixed capacity to be
trained with the new information.

1. **Online incremental feature learning with denoising autoencoders** ICAIS 2012. *Zhou et al.*\
Proposes incremental training of a denoising autoencoder that adds neurons for samples with high loss and subsequently merges these neurons with  existing ones to prevent redundancy. 

1. **AdaNet: Adaptive structural
learning of artificial neural networks** arXiv 2016. *Cortes et al.*\
Adapts both the structure of the network and its weights by balancing the model complexity and empirical risk minimization.

1. **Error-driven incremental learning in
deep convolutional neural network for large-scale image classification** ACM ICM 2014. *Xiao et al.*\
Proposes a network that incrementally grows in capacity and also in hierarchical fashion. Classes are grouped according to their similarity and self-organized into multiple levels, with models inheriting features from existing ones to speed up the learning.

1. **Neurogenesis deep learning** IJCNN 2017. *Draelos et al.*\
Their model adds new neural units to an autoencoder to facilitate the addition of new MNIST digits, and uses **intrinsic replay** (gen model) to preserve the weights required to retain older information.

1. **Lifelong learning with dynamically expandable
networks** ICLR 2018. *Yoon et al.* [paper](https://arxiv.org/abs/1708.01547) \
Proposes a dynamically expanding network (DEN) that increases the number of trainable parameters to incrementally learn new tasks. DEN is trained in an online manner by performing selective retraining which expands the network capacity using group sparse regularization to decide how many neurons to add at each layer. 


1. **Incremental on-line learning of object classes using a combination of
self-organizing incremental neural networks and deep convolutional neural networks** IROS’16 *Part, J. L. & Lemon, O.*

1. **Incremental online learning of objects for robots operating in real
environments** *ICDL-EPIROB’17. *Part, J. L. & Lemon, O.*\
Part and Lemon propose combining a pre-trained CNN with a self-organizing incremental neural network (SOINN) that allows the classification network to grow according to the task requirements. An issue that arises from these types of approaches is scalability since the classification network grows with the number of classes that have been learned. Another problem that was identified is that by relying on fixed representations, e.g., pre-trained CNNs, the discrimination power will be conditioned by the dataset used to train the feature extractor.

1. **iCaRL: Incremental classifier
and representation learning** arXiv 2016. *Rebuffi et al.*\
Proposes an approcach simlar to Part and Lemon but makes use of example data points that are used along with the new data to dynamically adapt the weights of the feature extractor, a technique that is referred to as **rehearsal**. By combining new and old data, they prevent catastrophic forgetting but at the expense of a higher memory footprint. 

#### Dynamic Image Classification







### [Complementary System and Replay](#content)

### [Analysis]

1. **Learning multiple layers of features from tiny images** Master’s thesis, University
of Toronto 2009. *Krizhevsky, A.* [paper]()
1. **Measuring catastrophic forgetting in neural networks** AAAI 2018. *Kemker, R.* [paper]()

## [Datasets](#content)

1. **[MNIST](#content)** [dataset](http://yann.lecun.com/exdb/mnist/)

1. **[CUB-200](#content)** [dataset](http://www.vision.caltech.edu/visipedia/CUB-200.html)

1. **[AudioSet](#content)** [dataset](https://research.google.com/audioset/)

1. **[Core50](#content)** [dataset](https://vlomonaco.github.io/core50//)

1. **[iCIFAR-100](#content)** [dataset]


## [Applications](#content)  
