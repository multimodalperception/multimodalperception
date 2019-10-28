# Segmentation LiDAR
<a id="bck" href="/index.html#introtab"><b>Back to index</b></a> &nbsp; &nbsp;
<a href="/segmentation.html#bck"><b>Back to Segmentation</b></a> &nbsp; &nbsp;
<a href="/segmentation/segmentation_2d.html#bck"><img src="/img/2D.png" alt="2D" width="50"/></a> &nbsp; 
<a href="/segmentation/segmentation_3d.html#bck"><img src="/img/3D.png" alt="3D" width="50"/></a> &nbsp; 
<a href="/segmentation/segmentation_thermal.html#bck"><img src="/img/Thermal.png" alt="Thermal" width="50"/></a> &nbsp;
<a href="/segmentation/segmentation_lidar.html#bck"><img src="/img/LiDAR.png" alt="LiDAR" width="50"/></a>

<table id="commontab">
<tr><th id="segmentation"> Reference </th><th id="segmentation"> Sensors </th><th id="segmentation"> Semantics </th><th id="segmentation"> Sensing Modality Representations </th><th id="segmentation"> Fusion Operation and Method </th><th id="segmentation"> Fusion Level </th><th> Dataset(s) used </th></tr>

<tr><td valign="top">Chen <i>et al.</i>, 2019
    <a href="https://arxiv.org/pdf/1904.01206">[pdf]</a><a href="./ref/chen2019progressive.bib">[ref]</a>
    </td><td valign="top"> LiDAR, visual camera </td><td valign="top"> Road segmentation </td><td valign="top"> RGB image, altitude difference image. Each processed by a CNN </td><td valign="top"> Feature adaptation module, modified concatenation. </td><td valign="top"> Middle </td><td valign="top"> KITTI </td></tr>

<tr><td valign="top"> Caltagirone <i>et al.</i>, 2019 
    <a href="https://arxiv.org/pdf/1809.07941">[pdf]</a><a href="./ref/caltagirone2019lidar.bib">[ref]</a>
    </td><td valign="top"> LiDAR, vision camera </td><td valign="top"> Road segmentation </td><td valign="top"> LiDAR front-view depth images, RGB image. Each input processed by a FCN </td><td valign="top"> Feature concatenation (For early and late fusion), weighted addition similar to gating network (for middle-level cross fusion) </td><td valign="top"> Early, Middle, Late </td><td valign="top"> KITTI </td></tr>

<tr><td valign="top">Erkent <i>et al.</i>, 2018
    <a href="https://ieeexplore.ieee.org/abstract/document/8593434">[pdf]</a><a href="./ref/erkent2018semantic.bib">[ref]</a>
    </td><td valign="top"> LiDAR, visual camera </td><td valign="top"> Multiple 2D objects </td><td valign="top"> LiDAR BEV occupancy grids (processed based on Bayesian filtering and tracking), RGB image (processed by a FCN with VGG16 backbone) </td><td valign="top"> Feature concatenation </td><td valign="top"> Middle </td><td valign="top"> KITTI, self-recorded </td></tr>

<tr><td valign="top"> Lv <i>et al.</i>, 2018 
    <a href="https://ieeexplore.ieee.org/abstract/document/8500551/">[pdf]</a><a href="./ref/lv2018novel.bib">[ref]</a>
    </td><td valign="top"> LiDAR, vision camera </td><td valign="top"> Road segmentation </td><td valign="top"> LiDAR BEV maps, RGB image. Each input processed by a FCN with dilated convolution operator. RGB image features are alo projected onto LiDAR BEV plane before fusion </td><td valign="top"> Feature concatenation  </td><td valign="top"> Middle </td><td valign="top"> KITTI </td></tr>

<tr><td valign="top"> Wulff <i>et al.</i>, 2018 
    <a href="https://ieeexplore.ieee.org/abstract/document/8500549">[pdf]</a><a href="./ref/wulff2018early.bib">[ref]</a>
    </td><td valign="top"> LiDAR, vision camera </td><td valign="top"> Road segmentation. Alternatives: freespace, ego-lane detection </td><td valign="top"> LiDAR BEV maps, RGB image projected onto BEV plane. Inputs processed by a FCN with UNet </td><td valign="top"> Feature concatenation </td><td valign="top"> Early </td><td valign="top"> KITTI </td></tr>

<tr><td valign="top"> Kim <i>et al.</i>, 2018 
    <a href="https://arxiv.org/abs/1807.06233">[pdf]</a><a href="./ref/kim2018robust.bib">[ref]</a>
    </td><td valign="top"> LiDAR, vision camera </td><td valign="top"> 2D Off-road terrains  </td><td valign="top"> LiDAR voxel (processed by 3D convolution), RGB image (processed by ENet) </td><td valign="top"> Addition </td><td valign="top"> Early, Middle, Late </td><td valign="top"> self-recorded </td></tr>

<tr><td valign="top"> Yang <i>et al.</i>, 2018 
    <a href="https://ieeexplore.ieee.org/abstract/document/8428696/">[pdf]</a><a href="./ref/yang2018fusion.bib">[ref]</a>
    </td><td valign="top"> LiDAR, vision camera </td><td valign="top"> Road segmentation </td><td valign="top"> LiDAR points (processed by PointNet++), RGB image (processed by FCN with VGG16 backbone) </td><td valign="top"> Optimizing Conditional Random Field (CRF) </td><td valign="top"> Late </td><td valign="top"> KITTI </td></tr>

<tr><td valign="top">Gu <i>et al.</i>, 2018
    <a href="https://ieeexplore.ieee.org/abstract/document/8370690">[pdf]</a><a href="./ref/gu20183d.bib">[ref]</a>
    </td><td valign="top"> LiDAR, visual camera </td><td valign="top"> Road segmentation </td><td valign="top"> LiDAR front-view depth and height maps (processed by a inverse-depth histogram based line scanning strategy), RGB image (processed by a FCN). </td><td valign="top"> Optimizing Conditional Random Field </td><td valign="top"> Late </td><td valign="top"> KITTI </td></tr>

</table>