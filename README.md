# NeFL: Nested Federated Learning

<p align="center">
  <span style="font-size:24px">
    <a href="https://honggkang.github.io/about/" style="text-decoration:none;">Honggu Kang</a>,&nbsp;&nbsp;&nbsp;&nbsp;
    <a href="https://seohyeon-cha.github.io/" style="text-decoration:none;">Seohyeon Cha</a>,&nbsp;&nbsp;&nbsp;&nbsp;
    <a href="https://alinlab.kaist.ac.kr/shin.html" style="text-decoration:none;">Jinwoo Shin</a>,&nbsp;&nbsp;&nbsp;&nbsp;
    Jongmyeong Lee,&nbsp;&nbsp;&nbsp;&nbsp;
    <a href="https://artlab.kaist.ac.kr/bbs/board.php?bo_table=sub1_1" style="text-decoration:none;">Joonhyuk Kang</a><br><br>
    <a href="https://www.kaist.ac.kr/en/" style="text-decoration:none;">KAIST</a><br><br>
  </span>
</p>

<p align="center">
  <span style="font-size:16px">
    <a href="https://arxiv.org/abs/2308.07761" style="text-decoration:none;">[Paper]</a>&nbsp;&nbsp;&nbsp;
    <a href="https://github.com/honggkang/nested-federated-learning" style="text-decoration:none;">[Code]</a>
  </span>
</p>

## Abstract
During the training pipeline of FL, slow or incapable clients (i.e., stragglers) slow down the total training time and degrade performance. System heterogeneity, including heterogeneous computing and network bandwidth, has been addressed to mitigate the impact of stragglers. Previous studies tackle the system heterogeneity by splitting a model into submodels, but with less degree-of-freedom in terms of model architecture. We propose *nested federated learning (NeFL)*, a generalized framework that efficiently divides a model into submodels using both depthwise and widthwise scaling. NeFL is implemented by interpreting forward propagation of models as solving ordinary differential equations (ODEs) with adaptive step sizes. To address the *inconsistency* that arises when training multiple submodels of different architecture, we decouple a few parameters from parameters being trained for each submodel. NeFL enables resource-constrained clients to effectively join the FL pipeline and the model to be trained with a larger amount of data. Through a series of experiments, we demonstrate that NeFL leads to significant performance gains, especially for the worst-case submodel. Furthermore, we demonstrate NeFL aligns with recent studies in FL, regarding pre-trained models of FL and the statistical heterogeneity.

## Main Results

