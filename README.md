# NeFL: Nested Federated Learning

<p align="center">
  <span style="font-size:24px">
    <a href="https://honggkang.github.io/about/" style="text-decoration:none;">Honggu Kang</a>&nbsp;&nbsp;&nbsp;&nbsp;
    <a href="https://seohyeon-cha.github.io/" style="text-decoration:none;">Seohyeon Cha</a>&nbsp;&nbsp;&nbsp;&nbsp;
    <a href="https://alinlab.kaist.ac.kr/shin.html" style="text-decoration:none;">Jinwoo Shin</a>&nbsp;&nbsp;&nbsp;&nbsp;
    Jongmyeong Lee&nbsp;&nbsp;&nbsp;&nbsp;
    <a href="https://artlab.kaist.ac.kr/bbs/board.php?bo_table=sub1_1" style="text-decoration:none;">Joonhyuk Kang</a><br>
    <a href="https://www.kaist.ac.kr/en/" style="text-decoration:none;">KAIST</a><br>
  </span>
  <span style="font-size:16px">
    <a href="https://arxiv.org/abs/2308.07761" style="text-decoration:none;">[Paper]</a>&nbsp;&nbsp;&nbsp;
    <a href="https://github.com/honggkang/nested-federated-learning" style="text-decoration:none;">[Code]</a>
  </span>
</p>

## Abstract
During the training pipeline of FL, slow or incapable clients (i.e., stragglers) slow down the total training time and degrade performance. System heterogeneity, including heterogeneous computing and network bandwidth, has been addressed to mitigate the impact of stragglers. Previous studies tackle the system heterogeneity by splitting a model into submodels, but with less degree-of-freedom in terms of model architecture. We propose *nested federated learning (NeFL)*, a generalized framework that efficiently divides a model into submodels using both depthwise and widthwise scaling. NeFL is implemented by interpreting forward propagation of models as solving ordinary differential equations (ODEs) with adaptive step sizes. To address the *inconsistency* that arises when training multiple submodels of different architecture, we decouple a few parameters from parameters being trained for each submodel. NeFL enables resource-constrained clients to effectively join the FL pipeline and the model to be trained with a larger amount of data. Through a series of experiments, we demonstrate that NeFL leads to significant performance gains, especially for the worst-case submodel. Furthermore, we demonstrate NeFL aligns with recent studies in FL, regarding pre-trained models of FL and the statistical heterogeneity.

## Main Results
**Results of NeFL for CIFAR-10 dataset under IID (left) and non-IID (right) settings are presented: Top-1 classification accuracies (%) for the worst-case submodel and the average of the performance of five submodels.**

| **Model**  | **Method**        | **IID Worst** | **IID Avg** | **non-IID Worst** | **non-IID Avg** |
|------------|-------------------|---------------|-------------|-------------------|-----------------|
| ResNet18   | HeteroFL          | 80.62 (± 0.24)| 84.26 (± 1.95)| 76.25 (± 1.05)    | 80.11 (± 2.03)  |
| ResNet18   | FjORD             | 85.12 (± 0.22)| 87.32 (± 1.21)| 75.81 (± 5.65)    | 77.99 (± 6.50)  |
| ResNet18   | DepthFL           | 64.80 (± 10.49)| 82.44 (± 10.17)| 59.61 (± 5.16)    | 76.89 (± 9.60)  |
| ResNet18   | **NeFL (ours)**   | **86.86 (± 0.22)**| **87.88 (± 0.68)**| **81.26 (± 2.44)**  | **81.71 (± 3.14)**|
| ResNet34   | HeteroFL          | 79.51 (± 0.44)| 83.16 (± 1.96)| 76.03 (± 1.34)    | 79.63 (± 5.24)  |
| ResNet34   | FjORD             | 85.12 (± 0.25)| 87.36 (± 1.19)| 74.70 (± 3.66)    | 76.01 (± 5.24)  |
| ResNet34   | DepthFL           | 25.73 (± 4.25)| 75.30 (± 24.88)| 30.42 (± 9.34)    | 70.76 (± 21.04) |
| ResNet34   | **NeFL (ours)**   | **87.71 (± 0.37)**| **89.02 (± 0.80)**| **80.76 (± 2.82)**  | **83.31 (± 2.94)**|

