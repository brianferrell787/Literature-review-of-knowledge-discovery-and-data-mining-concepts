# Survey-of-data-mining-concepts

Below describes a survey of literature surrounding knowledge discovery and data mining concepts, tools and methods. 
Major Topics Covered: 
 
- Knowledge discovery process 
- Data 
- Data preprocessing 
- Unsupervised data analysis 
- Supervised data analysis 

# Table of contents

<!--ts-->

- [A survey of data mining and knowledge discovery process models and methodologies](#a-survey-of-data-mining-and-knowledge-discovery-process-models-and-methodologies)
- [Map-Reduce for Machine Learning on Multicore](#Map-Reduce-for-Machine-Learning-on-Multicore)
- [A Few Useful Things to Know About Machine Learning](#A-Few-Useful-Things-to-Know-About-Machine-Learning)
- [A Survey of Discretization Techniques: Taxonomy and Empirical Analysis in Supervised Learning](#A-Survey-of-Discretization-Techniques-Taxonomy-and-Empirical-Analysis-in-Supervised-Learning)
- [Data clustering: 50 years beyond K-means](#Data-clustering-50-years-beyond-K-means)
- [An introduction to ROC analysis](#An-introduction-to-ROC-analysis)
- [An Empirical Comparison of Supervised Learning Algorithms](#An-Empirical-Comparison-of-Supervised-Learning-Algorithms)
- [Making machine learning trustworthy](#Making-machine-learning-trustworthy)

<!--te-->




## A survey of data mining and knowledge discovery process models and methodologies
[Paper](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/C2EC780B41545D44AB7F8F7BCBA8D982/S0269888910000032a.pdf/div-class-title-a-survey-of-data-mining-and-knowledge-discovery-process-models-and-methodologies-div.pdf)

1: This paper presents descriptions, advantages, and disadvantages of 14 popular data
mining and knowledge discovery methodologies, showing each method’s evolution as
well as the history of these techniques and what is considered to be state of the art. It
begins with an introduction to what data mining and knowledge discovery (KDD) is as
well as a brief history of the KDD process and how it has progressed. After that they
define basic terms in regards to process models, paradigms, methodologies,
techniques, and tools; followed by a review of the models as well as a comparative
study between them. Finally, they conclude with their own newly proposed methodology
and conclusions about the specific steps conducted. The paper divides the 14 data
mining and knowledge discovery methods and approaches into three subsections: KDD
related approaches, CRISP-DM related approaches, and other approaches. Most of the
approaches described in this paper are based on the first two subsections; therefore,
those main approaches are described in more detail. The KDD approach involves 9
steps in regards to discovering useful knowledge from data, whereas the CRISP-DM
approach is more of a life cycle overview containing phases, tasks, and relationships
within those tasks that move back and forth between phases. Other approaches include
the automation of data mining processes, Six-Sigma, etc.. Based on a comparative
analysis of all the approaches, the authors create a newly refined data mining process
that includes more specific phases than other approaches to avoid overlap (17
subprocesses).  

2.1: Authors claim that CRISP-DM is not mature enough to deal with the complexity of
today's problems. They emphasize the need for it to address growing problems in
relation to project management, organization, and quality.


2.2: Authors claim that approaches involving automated data mining processes are,
although helpful for non-expert data mining users, excluding the data understanding
step. They say this step is considered to be essential if you want to assess potential
problems and test improvements.


2.3: Authors claim that their refined data mining process can be used for developing any
kind of data mining and knowledge discovery project.


3: In support of 2.1 there are other papers that also focus on the ease of data mining
processes for Big Data projects that are transferable to today’s complexities. Dutta, et
al. [1] explored a Big Data project at a manufacturing company, and in their
consideration of the CRISP-DM approach, they seemed weary of the fact that it is
unknown if the framework could even be applied to their complex project. In addition,
Plumed et al. [2] claim CRISP-DM is too restrictive and needs to include exploratory
activities such as goal exploration, data source exploration and data value exploration.
Both support the claim that CRISP-DM is not suitable for Big Data projects.


[1] Dutta, Debprotim, and Indranil Bose. "Managing a big data project: the case of ramco cements
limited." International Journal of Production Economics 165 (2015): 293-306.

[2] Martínez-Plumed, Fernando, et al. "CRISP-DM twenty years later: From data mining processes to data
science trajectories." IEEE Transactions on Knowledge and Data Engineering (2019).

## Map-Reduce for Machine Learning on Multicore
[Paper](https://proceedings.neurips.cc/paper/2006/file/77ee3bc58ce560b86c2b59363281e914-Paper.pdf)

1: The main motivation from this paper begins with the problem of there not being any
good frameworks for machine learning to take advantage of an increasing number of
cores (processors) per chip. Authors point out that there are many parallel programming
languages but none are generalizable enough to parallelize a widespread of machine
learning algorithms. This paper presents a pragmatic and general framework for parallel
programming on a large class of machine learning algorithms (10 of them) for multicore
processors. One of the main contributions of the paper is to allow future programmers to
speed up their machine learning processes and applications by simply just adding on
more cores towards their projects rather than looking for specialized implementations.
The authors fit these algorithms into what is called the Statistical Query Model to which
gets computed into summation form, and then they attempt to express these
summations in a map-reduce framework to achieve linear speed-up with the number of
cores. Each algorithm from these experiments had two different versions: map-reduce
and then a serial implementation without the framework. They conducted extensive
experiments to compare the “speed-up” on eight commonly used machine learning
datasets. One dataset was derived from the UCI Machine Learning repository whereas
the other two were from an anonymous research group (Helicopter Control and sensor
data). The authors have demonstrated a general framework for speeding up machine
learning code by implementing the summation form of these algorithms in a map-reduce
framework.


2.1: Authors show that most of the algorithms achieved more than 1.9x times
performance improvement, and some even obtained greater than 2x speedup.


2.2: Authors claim the summation form in a map-reduce framework can parallelize a
wide range of machine learning algorithms and achieve much higher speedup on a dual
processor on up to 54 times speedup on 64 cores.


2.3: Authors make the claim that the map-reduce framework is easy to program and
that their experimental results increase speedup linearly with the increasing number of
processors


3: Al-Amin et al. 's [1] claims are not in support of claim 2.2. They mention that the
MapReduce (MR) technique used above is not a suitable or generalizable choice
because not every algorithm can be implemented as an MR program and also when
data is in need to be processed through iterations such as K-means. They mention that
their summarization matrix is even more generalized. Another paper [2] proposes a
method “Cocktail”, which is an incrementally enabled learning framework within a
reference 5G network architecture. They used stochastic gradient descent to design an
online asymptotically optimal algorithm. They too are not fully in support of claim 2.2; in
fact, they make the claim that the framework above is inefficient when used for
in-network training, since the data collection and distribution would lead to great
transmission overhead.


[1] Al-Amin, Sikder Tahsin, and Carlos Ordonez. "Efficient machine learning on data science languages with parallel
data summarization." Data & Knowledge Engineering 136 (2021): 101930.


[2] Pu, Lingjun, et al. "Cost-efficient and Skew-aware Data Scheduling for Incremental Learning in 5G Networks."
IEEE Journal on Selected Areas in Communications (2021)


## A Few Useful Things to Know About Machine Learning
[Paper](https://homes.cs.washington.edu/~pedrod/papers/cacm12.pdf)

1: The main motivation of this article is to summarize sound wisdom and beliefs
surrounding machine learning. The author gives 12 insights and lessons on machine
learning algorithms concerning their pitfalls, things we should focus on, as well as
answers to common questions. It starts out by elaborating on classification models;
what they are, examples, etc. Then it goes into how the concept of learning is broken
down into three components: Representation, Evaluation, and Optimization. These
components are the key to figuring out which algorithms to use since there are
thousands. In addition, since it is not easy to figure out each of these components, the
author touches on key issues, as the choices involving a machine learning project are at
times even more important than the choice of learner. The key things touched on in this
article are the following: size is not the only thing that matters when it comes to your
dataset, the issues with overfitting, the curse of dimensionality, theoretical woes,
importance of feature engineering, your training set size, importance of training multiple
models, how correlation does not imply causation, and more. In conclusion, this useful
article gives a review of some of the best practices when it comes to machine learning.


2.1: Authors claim that a dumb algorithm with tons of data beats a clever one with
modest amounts of data.


2.2: Authors claim that one model is not enough, and that it is always best to test
multiple random variations of different models and compare the performances of them.


2.3: Authors claim that just because a function can be represented does not mean it can
be learned.


3: In slight disagreement with the first claim, the authors (Radja et. al) compare
performances from four different algorithms across four datasets of varying sizes,
classifying the diagnosis of diabetes. They trained an SVM model, Naive Bayes, J48
tree, a Decision Table Algorithm, and found that no matter the size of the dataset, the
SVM model did best, which would be a far more complex model in comparison to Naive
Bayes. However, it is possible that the dataset sizes they are comparing are not
“different” enough to really see any significant changes. On the other hand, Barbedo et
al. are in agreement that the size of the dataset matters a lot when it comes to using
more advanced algorithms; in fact, it is necessary to yield solid results. This is why
when attempting to classify plant diseases using transfer learning and CNN models,
they had to use techniques to augment more training data in order to fit the complexities
of the models used. Without these techniques and additional robust tooling, a simpler
model like Support Vector Machine, Multilayer Perceptron Neural Network or Decision
Tree would most likely be best.


[1] Radja, Melky, and Andi Wahju Rahardjo Emanuel. "Performance evaluation of supervised machine
learning algorithms using different data set sizes for diabetes prediction." 2019 5th international
conference on science in information technology (ICSITech). IEEE, 2019.


[2] Barbedo, Jayme Garcia Arnal. "Impact of dataset size and variety on the effectiveness of deep learning
and transfer learning for plant disease classification." Computers and electronics in agriculture 153
(2018): 46-53.


## A Survey of Discretization Techniques: Taxonomy and Empirical Analysis in Supervised Learning
[Paper](https://ieeexplore.ieee.org/document/6152258)

1: Discretization techniques transform continuous/numerical attributes to
discrete/nominal ones in order to represent the data in a simplified concise manner. The
main motivation of this paper is to survey these methods in order to reduce issues and
confusion found in defining discretization properties as well as establishing a formal
categorization method. The author's provide a theoretical approach by classifying
properties pointed out in previous research, as well as an empirical one where they
conduct supervised classification experiments with the most representative and newest
discretizers, different classifiers, and a large number of data sets. For the experimental
part of the paper, they use 30 discretizers, 6 classification methods, 40 datasets, and
compare accuracy and Cohen’s kappa measures across all of the classification
problems. The authors provide related work on improving and analyzing discretization
techniques, a review of the criteria for building a discretization method, a discussion of
their experimental framework and the results found within them. Their experiment was
setup such that the discretization methods would be used on the 40 datasets, and then
to evaluate the differences in performances they used the six classifiers (C4.5,
DataSqueezer, KNN, Naive Bayes, PUBLIC, and Ripper) to measure the
successfulness of the application. In conclusion, the authors observe they cannot label
a single discretizer as the “best” because it depends on the problem at hand; however,
this study gives the tools to help researchers find the most appropriate approach for
their problem.


2.1: Authors claim that classic discretizers such as EqualWidth, EqualFrequency, 1R,
ID3, CADD, Bayesian, and Cluster Analysis are not as good as they should be,
considering the improvements made on them over the years.


2.2: Authors claim that FUSINTER, ChiMerge, CAIM, and Modified Chi2 offer excellent
performances considering all types of classifiers.


2.3: Authors claim that PKID, FFD are suitable methods for lazy and Bayesian learning
and CACC, Distance, and MODL are good choices in rule induction learning.


3: In agreement with claim 2.2 the authors (Tari et. al) compare various discretization
techniques and their impact on a different type of classifier than the ones in the
summarized paper above (Multi-Objective Classification Algorithm for Imbalanced data).
The main objective was to determine which discretization technique helped with
predicting bronchopulmonary cancer. They found ID3 seemed to be better suited for
their problem (which is in disagreement with claim 2.1) but that FUSINTER and CAIM
were still leading performers for at least 2 of their datasets. In addition, Thaiphan et. al
ran a similar study as the proposed review paper on 20 data sets but just for decision
trees and found that MDLP was the best overall followed by ChiMerge, FUSINTER;
however, they found that Modified Chi2 and CAIM are not really suitable for Decision
Trees.


[1] Tari, Sara, et al. "Impact of the Discretization of VOCs for Cancer Prediction Using a Multi-Objective Algorithm."
International Conference on Learning and Intelligent Optimization. Springer, Cham, 2020.


[2] Thaiphan, Rattayagon, and Thimaporn Phetkaew. "Comparative analysis of discretization algorithms on decision
tree." 2018 IEEE/ACIS 17th International Conference on Computer and Information Science (ICIS). IEEE, 2018.

## Data clustering: 50 years beyond K-means
[Paper](https://www.sciencedirect.com/science/article/abs/pii/S0167865509002323)

1: Clustering methods are unsupervised techniques that wish to group data according to
their measured distance and/or perceived similarities in order to be understood,
processed, and summarized. The main motivation of this paper is to give an overview of
these methods as well as the major challenges and issues associated with designing
such algorithms. The authors also bring light to the emerging methods in this field as
well as their useful research direction. The paper starts by giving a historical overview
and purpose of clustering, followed by a review of the most well-known hierarchical
algorithms of them all (k-means clustering) along with the parameters, computations,
and extensions involved. Additionally, they briefly discuss major approaches to
clustering methods considering there are thousands of these algorithms. Finally, the
authors review the difficulties and challenges with data representation, the purpose of
grouping, the number of clusters to use and their validity as well as any up and coming
trends that are emerging in this field. The authors conclude that there is a need for
benchmark data for the research community to test and evaluate, a clustering’s purpose
for its respective application, stable and consistent solutions, and more semi-supervised
clustering techniques.


2.1: Authors claim that there is no single clustering algorithm that has been shown to
dominate the rest across all problem sets and domains.


2.2: Authors claim that in most applications, it’s not necessarily about picking the “best”
clustering algorithm that matters most but rather about the feature extraction methods
that identify the underlying clustering structure of the data.


2.3: Authors claim that objects need to have a natural representation and not just be a
pooled feature vector of components, otherwise it may result in poor clustering
performance.


3: In agreement with claim 2.1, Morissette et. al present a tutorial on the k-means
clustering technique through three different algorithms. Authors conclude that no
clustering algorithm is the best, and that whatever choice you make as the optimal
algorithm depends solely on the characteristics of the dataset (size, number of variables
in the cases). Additionally, Jain et. al are similarly in agreement with claim 2.1 and
suggest working out multiple clustering algorithms that are different in order to gain the
best understanding possible about the dataset.


[1] Morissette, Laurence, and Sylvain Chartier. "The k-means clustering technique: General considerations
and implementation in Mathematica." Tutorials in Quantitative Methods for Psychology 9.1 (2013): 15-24.


[2] Jain, Anil K., Robert P. W. Duin, and Jianchang Mao. "Statistical pattern recognition: A review." IEEE
Transactions on pattern analysis and machine intelligence 22.1 (2000): 4-37.


## An introduction to ROC analysis
[Paper](https://www.sciencedirect.com/science/article/pii/S016786550500303X?casa_token=UDNHd1Fhnw4AAAAA:hoE5W_S_DlsrabMgWZYsGEpvzIcwIgWUi28xcnF483YAIon6Dh0Ql46bob74QOz3JhVjx45z)

1: A receiver operating characteristic (ROC curve) graph is a simple plot that illustrates
the performances of a true and false positive rate for diagnostic systems, and has been
gaining more popularity within the machine learning and data mining research fields.
The main motivation of this paper is to give an introduction to these graphs as well as a
guide for using them in research in order to bring light to some of the common
misconceptions and pitfalls seen in practice. The paper starts by giving an overview of
ROC graphs including their space, how performances are distinguished (random vs.
curves, relative vs. absolute scores), as well as the area under an ROC curve (AUC).
Additionally, they briefly discuss the importance of averaging ROC curves through
vertical averaging or threshold averaging. Finally, the authors review problems that have
more than two classes which includes the complexities of multi-class ROC and AUC
graphs, and interpolating multiple classifiers to get the desired outcome by using linear
interpolation. The authors conclude that ROC graphs are a very useful and powerful tool
for visualizing and evaluating classifiers that, if used properly, can promote and
generate a healthier evaluation research practice.


2.1: The authors claim that ROC graphs provide a richer measure of classification
performance than accuracy, error rate, or error cost.


2.2: The authors claim that it is misleading to use the ROC graph as a way to choose
the best classifier, because it is no different from just looking at the max accuracy.
Without a measure of variance, there is no proper evaluation technique in comparing
classifiers.


2.3: The authors claim that because ROC graphs decouple classifier performance from
class skew and error costs, they have all the advantages over precision-recall graphs
and lift curves.


3: In disagreement with claim 2.3 Ozenne et. al present a simulation study considering
different sizes of diseased and nondiseased groups. Authors claim that the ROC curve’s
relevance is heavily debatable for rare events. They found that in uncommon and rare
diseases, the area under the precision-recall curve (AUPRC) should be preferred
because it summarizes the biomarker’s performance better. Although, I am not sure if
their results are relevant to using classifiers within the machine learning and data mining
field as opposed to these “biomarkers”. However, in agreement with claim 2.3,
Brodersen et. al, who created over 1000 simulations comparing two models, claim that
the precision-recall curve is a “highly imprecise” estimate of the true curve, especially in
the case of a small sample size and class imbalance in favor of negative examples.


[1] Ozenne, Brice, Fabien Subtil, and Delphine Maucort-Boulch. "The precision–recall curve overcame the
optimism of the receiver operating characteristic curve in rare diseases." Journal of clinical epidemiology
68.8 (2015): 855-859.


[2] Brodersen, Kay Henning, et al. "The binormal assumption on precision-recall curves." 2010 20th
International Conference on Pattern Recognition. IEEE, 2010.

## An Empirical Comparison of Supervised Learning Algorithms
[Paper](https://www.cs.cornell.edu/~caruana/ctp/ct.papers/caruana.icml06.pdf)

1: Since there have been a number of supervised learning methods introduced in the
last decade there has been a need for an up-to-date (according to this time)
comprehensive evaluation study comparing various methods at a larger scale. The main
motivation of this paper is to present popular learning algorithms as well as inspect an
exhaustive list of performance metrics using 10 different supervised learning methods
such as SVMs, neural nets, logistic regression, naive bayes, random forest, etc.. The
authors also examine the effects of calibration methods for these models by using
Isotonic Regression and Platt Scaling. The paper starts by exploring each learning
algorithm, as well as a review of each performance metric they are using to compare
the models with. The study compares the algorithms on 11 binary classification
problems, and the authors give a description of each dataset in the paper in terms of
how they split their data, etc. The authors conclude that there is significant variability
across the problems and metrics, and that occasionally you have the “best” models
sometimes not performing well whereas the “worse” models randomly performing
exceptionally well; however, for the most part the field has progressed substantially
within the last 15 years.


2.1: The authors claim that using calibrated boosted trees was the best learning
algorithm overall followed by Random forests.


2.2: The authors claim that the calibration techniques used were highly effective on the
probability metrics from learning algorithms that also performed well on the
ranking/ordering metrics.


2.3: The authors claim that the worst models were naive bayes, logistic regression,
decision trees, and boosted stumps.


3: In agreement with claim 2.1, Sanderson et. al present a study on predicting suicide
by comparing calibrated boosted trees, recurrent neural networks, and convolutional
neural networks. Their dataset comprised of almost 4000 examples of deaths by suicide
and a little over 35,000 examples of deaths that did not happen by suicide. It was found
that the optimal method was the calibrated boosted trees; in addition, the authors noted
that this model was also the least computationally expensive one out of the three model
types. Additionally, in agreement with claim 2.1, Fonseca et. al present a study where
they cover best practices in regards to calibration techniques for binary classification
problems, as well as compare three supervised learning methods on real world credit
scoring data. The authors found that on most datasets, the Random Forest
outperformed the other models after calibration.


[1] Sanderson, Michael, et al. "Predicting death by suicide using administrative health care system data:
Can recurrent neural network, one-dimensional convolutional neural network, and gradient boosted trees
models improve prediction performance?." Journal of affective disorders 264 (2020): 107-114.


[2] Fonseca, Pedro G., and Hugo D. Lopes. "Calibration of Machine Learning Classifiers for Probability of
Default Modelling." arXiv preprint arXiv:1710.08901 (2017).

## Making machine learning trustworthy
[Paper](https://www.science.org/doi/10.1126/science.abi5052)


1: Although research in the field of machine learning has advanced dramatically over
the years, there is still a need for improved safety, security, transparency, and fairness
when implementing these models in actual practice, especially when it comes to
powering high-stake applications that affect human beings. The main motivation of this
article is to provide an overview of adversarial threats to machine learning which helps
ensure models are not just “memorizing” certain parts of their training data, and can be
confident/not easily be fooled when there are slight changes in input data. The paper
starts by exploring how easy it can be to throw a model prediction off by giving it slightly
manipulated data to make it seem like it is something completely different. In addition,
the author also mentions strategies that can be used to improve this issue, issues of
biases when it comes to labeling datasets, and other pitfalls of ML in order to
counterattack the blindspots that come with ML model configuring. The author
concludes that as a society we need to embrace these ethical norms and that there is a
dire need for insights from users across all domains when it comes to not only using
these ML models but trusting them.


2.1: The authors claim that ML models can easily be victims of malicious attacks during
training and deployment.


2.2: Authors claim that the most important advancement for ML models now is whether
or not it can be protected against several types of adversarial attacks.


2.3: Authors claim that there is a lack of broadly accepted definitions, transferability, and
formulations of adversarial robustness and privacy-preserving ML.


3: In agreement with claim 2.1, Garg et. al and Li et. al both present attack methods for
generating adversarial examples for NLP models by inserting contextual manipulations
derived from the BERT language model. Authors claim that recent studies have easily
exposed ML model’s vulnerabilities, and that these are easily identifiable by humans.
Both authors conclude that small perturbations in original inputs can mislead neural
networks to incorrect predictions. In addition, as a bonus they agree with claim 2.2 that
it is essential to explore these advancements to ensure reliability and robustness.


[1] Garg, Siddhant, and Goutham Ramakrishnan. "Bae: Bert-based adversarial examples for
text classification." arXiv preprint arXiv:2004.01970 (2020).


[2] Li, Linyang, et al. "Bert-attack: Adversarial attack against bert using bert." arXiv preprint
arXiv:2004.09984 (2020).
