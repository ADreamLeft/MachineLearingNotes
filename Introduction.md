# What is Machine Learning?
Learning from experiences(especially data)
最初AI用来完成人们的指令
# A brief history of ML
## Neural Networks
1940s biologists M.P. Model of neurour
1950s Perception
1960s XOR(异或问题)
1980s BP
2012   DP
## Generalization
### VC Theory(60 ~ 70s)
### PAC Learning (1984, Leslie Valiant)
采用相似概率估计，统计部分类似于VC Theory
## SVM(基本退出历史舞台), Boosting(90s ~ 2010) 
Learning algs, 偏理论
## Reinforcement Learning (80s ~ 90s)
## Graphical Models (80s ~ , Pearl)
# Subfields of ML
## Supervised Learning
## Unsupervised Learning / Self - Supervised Learning
## Online learning
## RL
## Generative Models
## PGM
# Perspectives
## Representations
Deep learning > Linear models
## Optimizations
training data
## Generadization
gaps between the performance of training data and test data
# A Foundation of (Supervised) Learning
## Supervised learning
### Collect Data
#### label and data
### Training: Learning a mapping (classifier)  $\hat{f}:x \to y$

#### Define a loss func
#### Minimize training loss
#### Get  $\hat{f}$
### Inference
#### Test data $x_{n+1} \to \hat{f}(x_{n+1})$
*assumption:* $(x, y) \overset{iid}{\sim} D(x, y)(unknown)$

#### If D is known, $f^\star = \underset y{argmax} P(y|x)$ ($f^\star$ is the Bayes classfier)
# Books
## Learnings
- Foundations of Machine Learning
- Understanding of Machine Learning from Theory to Algorithm
## Optimization(Theory)
- Combinational Optimization: Algorithms and Complexity
- Convex Optimization Algorithms
## Reinforcement Learning
- (Online Course) Reinforcement Learning. David Silver(UCL $\to$ DM)
- Reinforcement Learning. An Introduction
## Probability Graphical Models
- Coursera Online course D. Koller




