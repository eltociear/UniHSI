
<br>
<p align="center">
<h1 align="center"><img src="assets/unihsi_icon.png" align="center" width="6.5%"><strong>Unified Human-Scene Interaction 
  via Prompted Chain-of-Contacts</strong></h1>
  <p align="center">
    <a href='https://github.com/xizaoqu/' target='_blank'>Zeqi Xiao</a>&emsp;
    <a href='https://tai-wang.github.io/' target='_blank'>Tai Wang</a>&emsp;
    <a href='https://scholar.google.com/citations?user=GStTsxAAAAAJ&hl=zh-CN&oi=ao/' target='_blank'>Jingbo Wang</a>&emsp;
    <a href='https://www.jinkuncao.com/' target='_blank'>Jinkun Cao</a>&emsp;
    <a href='http://zhangwenwei.cn/' target='_blank'>Wenwei Zhang</a>&emsp;
    <a href='https://daibo.info/' target='_blank'>Bo Dai</a>&emsp;
    <a href='http://dahua.site/' target='_blank'>Dahua Lin</a>&emsp;
    <a href='https://oceanpang.github.io/' target='_blank'>Jiangmiao Pang*</a>&emsp;
    <br>
    Shanghai AI Laboratory&emsp;Nanyang Technological University&emsp;Carnegie Mellon University
  </p>
</p>

<p align="center">
  <a href="https://arxiv.org/abs/2309.07918" target='_blank'>
    <img src="https://img.shields.io/badge/arXiv-2308.16911-blue?">
  </a> 
  <a href="./assets/UniHSI.pdf" target='_blank'>
    <img src="https://img.shields.io/badge/Paper-📖-blue?">
  </a> 
  <a href="https://xizaoqu.github.io/unihsi" target='_blank'>
    <img src="https://img.shields.io/badge/Project-&#x1F680-blue">
  </a>
</p>

## 🏠 About
<!-- ![Teaser](assets/teaser.jpg) -->
<div style="text-align: center;">
    <img src="assets/teaser.png" alt="Dialogue_Teaser" width=100% >
</div>
This paper presents <b>a UNIfied HSI framework, UniHSI, which supports unified control of diverse interactions through language commands</b>. This framework is built upon the definition of interaction as <b>Chain of Contacts</b> (CoC): steps of human joint-object part pairs, which is inspired by the strong correlation between interaction types and human-object contact regions.
Based on the definition, UniHSI constitutes a <b>Large Language Model (LLM) Planner</b> to translate language prompts into task plans in the form of CoC, and a <b>Unified Controller</b> that turns CoC into uniform task execution. To facilitate training and evaluation, we collect a new dataset named <b>ScenePlan</b> that encompasses thousands of task plans generated by LLMs based on diverse scenarios. Comprehensive experiments demonstrate the effectiveness of our framework in versatile task execution and generalizability to real scanned scenes.

## 🔥 News
- [2023-08] We release the [paper](https://arxiv.org/abs/2309.07918) of UniHSI. Please check the :point_right: [webpage](https://xizaoqu.github.io/unihsi) :point_left: and view our demos! :sparkler:;

## 🔍 Overview

### Model
<p align="center">
  <img src="assets/main_figure.jpg" align="center" width="100%">
</p>
The whole pipeline consists of two major components: the LLM Planner and the Unified Controller. The LLM planner takes language inputs and background scenario information as inputs and outputs multi-step plan in the form of a Chain of Contacts. The Unified Controller then executes task plans step-by-step and output interaction movements.

### [Demo](https://xizaoqu.github.io/unihsi)
<!-- <div style="text-align: center;">
    <img src="assets/demo_fig.png" alt="Dialogue_Teaser" width=100% >
</div> -->
[![demo](assets/demo_fig.png "title")](https://xizaoqu.github.io/unihsi)
<!-- #### Pipeline Flow
<video src="assets/scannet_long_demo.mp4" controls>
</video>

#### Multi-objects Interaction
<video src="assets/multiobj_multistep_1.mp4" controls>
</video>
<video src="assets/multiobj_multistep_2.mp4" controls>
</video>

#### Diverse Interactions with the Same Object
<video src="assets/multistep_sit_demo.mp4" controls>
</video>
<video src="assets/multistep_bed_demo.mp4" controls>
</video>

#### ''Multi-agent'' Interaction Planned by LLMs
<video src="assets/scannet_two_bed_demo.mp4" controls>
</video> -->

## 🔗 Citation

If you find our work helpful, please cite:

```bibtex
@article{xiao2023unified,
  author    = {Xiao, Zeqi and Wang, Tai and Wang, Jingbo and Cao, Jinkun and Dai, Bo and Lin, Dahua and Pang, Jiangmiao},
  title     = {Unified Human-Scene Interaction via Prompted Chain-of-Contacts},
  journal   = {Arxiv},
  year      = {2023},
}
```

## 📄 License
<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/80x15.png" /></a>
<br />
This work is under the <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a>.

## 👏 Acknowledgements
- [ASE](https://github.com/nv-tlabs/ASE): Our codebase is built upon the AMP implementation in ASE.
- [PartNet](https://partnet.cs.stanford.edu/): We use objects from PartNet for training and evaluation.
- [ScanNet](http://www.scan-net.org/): We use scenatios from ScanNet for evaluation.
- [SAMP](https://github.com/mohamedhassanmus/SAMP): We use motion clips from SAMP for training.
- [CIRCLE](https://stanford-tml.github.io/circle_dataset): We use motion clips from CIRCLE for training.
