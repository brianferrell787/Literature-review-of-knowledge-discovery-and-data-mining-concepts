# Literature-review-of-knowledge-discovery-and-data-mining-concepts






## 1. A survey of data mining and knowledge discovery process models and methodologies
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

## 2. Map-Reduce for Machine Learning on Multicore
[Paper](https://proceedings.neurips.cc/paper/2006/file/77ee3bc58ce560b86c2b59363281e914-Paper.pdf)

Review #2
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


## 3. A Few Useful Things to Know About Machine Learning
[Paper](https://homes.cs.washington.edu/~pedrod/papers/cacm12.pdf)


## 4. A Survey of Discretization Techniques: Taxonomy and Empirical Analysis in Supervised Learning
[Paper](https://ieeexplore.ieee.org/document/6152258)


## 5. Data clustering: 50 years beyond K-means
[Paper](https://www.sciencedirect.com/science/article/abs/pii/S0167865509002323)


## 6. An introduction to ROC analysis
[Paper](https://www.sciencedirect.com/science/article/pii/S016786550500303X?casa_token=UDNHd1Fhnw4AAAAA:hoE5W_S_DlsrabMgWZYsGEpvzIcwIgWUi28xcnF483YAIon6Dh0Ql46bob74QOz3JhVjx45z)

## 7. An Empirical Comparison of Supervised Learning Algorithms
[Paper](https://www.cs.cornell.edu/~caruana/ctp/ct.papers/caruana.icml06.pdf)

## 8. Making machine learning trustworthy
[Paper](https://www.science.org/doi/10.1126/science.abi5052)
