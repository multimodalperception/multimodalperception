# Segmentation 2D
<a id="bck" href="/index.html#introtab"><b>Back to index</b></a> &nbsp; &nbsp;
<a href="/segmentation.html#bck"><b>Back to Segmentation</b></a> &nbsp; &nbsp;
<a href="/segmentation/segmentation_2d.html#bck"><img src="/img/2D.png" alt="2D" width="50"/></a> &nbsp; 
<a href="/segmentation/segmentation_3d.html#bck"><img src="/img/3D.png" alt="3D" width="50"/></a> &nbsp; 
<a href="/segmentation/segmentation_thermal.html#bck"><img src="/img/Thermal.png" alt="Thermal" width="50"/></a> &nbsp;
<a href="/segmentation/segmentation_lidar.html#bck"><img src="/img/LiDAR.png" alt="LiDAR" width="50"/></a>

<table id="commontab">
<tr><th id="segmentation"> Reference </th><th id="segmentation"> Sensors </th><th id="segmentation"> Semantics </th><th id="segmentation"> Sensing Modality Representations </th><th id="segmentation"> Fusion Operation and Method </th><th id="segmentation"> Fusion Level </th><th> Dataset(s) used </td></tr>

<tr><td valign="top">Chen <i>et al.</i>, 2019
    <a href="https://arxiv.org/pdf/1904.01206">[pdf]</a><a href="./ref/chen2019progressive.bib">[ref]</a>
    </td><td valign="top"> LiDAR, visual camera </td><td valign="top"> Road segmentation </td><td valign="top"> RGB image, altitude difference image. Each processed by a CNN </td><td valign="top"> Feature adaptation module, modified concatenation. </td><td valign="top"> Middle </td><td valign="top"> KITTI </td></tr>

<tr><td valign="top">Valada <i>et al.</i>, 2019
    <a href="https://arxiv.org/pdf/1808.03833">[pdf]</a><a href="./ref/valada2018self.bib">[ref]</a>
    </td><td valign="top"> Visual camera, depth camera, thermal camera  </td><td valign="top"> Multiple 2D objects </td><td valign="top"> RGB image, thermal image, depth image. Each processed by FCN with ResNet backbone (Adapnet++ architecture) </td><td valign="top"> Extension of Mixture of Experts </td><td valign="top"> Middle </td><td valign="top"> Six datasets, including Cityscape, Sun RGB-D, etc. </td></tr>

<tr><td valign="top">Sun <i>et al.</i>, 2019
    <a href="https://ieeexplore.ieee.org/abstract/document/8666745">[pdf]</a><a href="./ref/sun2019rtfnet.bib">[ref]</a>
    </td><td valign="top"> Visual camera, thermal camera </td><td valign="top"> Multiple 2D objects in campus environments </td><td valign="top"> RGB image, thermal image. Each processed by a base network built on ResNet </td><td valign="top"> Element-wise summation in the encoder networks </td><td valign="top"> Middle </td><td valign="top"> Datasets published by <a href="../ref/ha2017mfnet.bib">[ref]</a>  </td></tr>

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

<tr><td valign="top"> Guan <i>et al.</i>, 2018 
    <a href="https://arxiv.org/abs/1802.09972">[pdf]</a><a href="./ref/guan2018fusion.bib">[ref]</a>
    </td><td valign="top"> Vision camera, thermal camera </td><td valign="top"> 2D Pedestrian </td><td valign="top"> RGB image, thermal image. Each processed by a base network built on VGG16 </td><td valign="top"> Feature concatenation, Mixture of Experts </td><td valign="top"> Early, Middle, Late </td><td valign="top"> KAIST Pedestrian Dataset </td></tr>

<tr><td valign="top"> Yang <i>et al.</i>, 2018 
    <a href="https://ieeexplore.ieee.org/abstract/document/8428696/">[pdf]</a><a href="./ref/yang2018fusion.bib">[ref]</a>
    </td><td valign="top"> LiDAR, vision camera </td><td valign="top"> Road segmentation </td><td valign="top"> LiDAR points (processed by PointNet++), RGB image (processed by FCN with VGG16 backbone) </td><td valign="top"> Optimizing Conditional Random Field (CRF) </td><td valign="top"> Late </td><td valign="top"> KITTI </td></tr>

<tr><td valign="top">Gu <i>et al.</i>, 2018
    <a href="https://ieeexplore.ieee.org/abstract/document/8370690">[pdf]</a><a href="./ref/gu20183d.bib">[ref]</a>
    </td><td valign="top"> LiDAR, visual camera </td><td valign="top"> Road segmentation </td><td valign="top"> LiDAR front-view depth and height maps (processed by a inverse-depth histogram based line scanning strategy), RGB image (processed by a FCN). </td><td valign="top"> Optimizing Conditional Random Field </td><td valign="top"> Late </td><td valign="top"> KITTI </td></tr>

<tr><td valign="top">Cai <i>et al.</i>, 2018
    <a href="https://www.mdpi.com/1424-8220/18/12/4158">[pdf]</a><a href="./ref/cai2018robust.bib">[ref]</a>
    </td><td valign="top"> Satellite map with route information, visual camera </td><td valign="top"> Road segmentation </td><td valign="top"> Route map image, RGB image. Images are fused and processed by a FCN </td><td valign="top"> Overlaying the line and curve segments in the route map onto the RGB image to generate the Map Fusion Image (MFI) </td><td valign="top"> Early </td><td valign="top"> self-recorded data </td></tr>

<tr><td valign="top"> Ha <i>et al.</i>, 2017 
    <a href="https://ieeexplore.ieee.org/abstract/document/8206396/">[pdf]</a><a href="./ref/ha2017mfnet.bib">[ref]</a>
    </td><td valign="top"> Vision camera, thermal camera </td><td valign="top"> Multiple 2D objects in campus environments </td><td valign="top"> RGB image, thermal image. Each processed by a FCN and mini-inception block </td><td valign="top"> Feature concatenation, addition (``short-cut fusion'') </td><td valign="top"> Middle </td><td valign="top"> self-recorded data </td></tr>

<tr><td valign="top"> Valada <i>et al.</i>, 2017 
    <a href="http://ais.informatik.uni-freiburg.de/publications/papers/valada17icraa.pdf">[pdf]</a><a href="./ref/valada2017adapnet.bib">[ref]</a>
    </td><td valign="top"> Vision camera, thermal camera </td><td valign="top"> Multiple 2D objects </td><td valign="top"> RGB image, thermal image, depth image. Each processed by FCN with ResNet backbone </td><td valign="top"> Mixture of Experts </td><td valign="top"> Late </td><td valign="top"> Cityscape, Freiburg Multispectral Dataset, Synthia </td></tr>

<tr><td valign="top"> Schneider <i>et al.</i>, 2017 
    <a href="https://arxiv.org/pdf/1707.03167">[pdf]</a><a href="./ref/schneider2017regnet.bib">[ref]</a>
    </td><td valign="top"> Vision camera </td><td valign="top"> Multiple 2D Objects  </td><td valign="top"> RGB image, depth image </td><td valign="top"> Feature concatenation </td><td valign="top"> Early, Middle, Late </td><td valign="top"> Cityscape </td></tr>

<tr><td valign="top"> Schneider <i>et al.</i>, 2017 
    <a href="https://arxiv.org/pdf/1707.03167">[pdf]</a><a href="./ref/schneider2017regnet.bib">[ref]</a>
    </td><td valign="top"> Vision camera </td><td valign="top"> Multiple 2D Objects  </td><td valign="top"> RGB image (processed by GoogLeNet), depth image from stereo camera (processed by NiN net) </td><td valign="top"> Feature concatenation </td><td valign="top"> Early, Middle, Late </td><td valign="top"> Cityscape </td></tr>

<tr><td valign="top"> Valada <i>et al.</i>, 2016 
    <a href="https://link.springer.com/chapter/10.1007/978-3-319-50115-4_41">[pdf]</a><a href="./ref/valada2016deep.bib">[ref]</a>
    </td><td valign="top"> Vision camera, thermal camera </td><td valign="top"> Multiple 2D objects in forested environments </td><td valign="top"> RGB image, thermal image, depth image. Each processed by the UpNet (built on VGG16 and up-convolution) </td><td valign="top"> Feature concatenation, addition </td><td valign="top"> Early, Late </td><td valign="top"> self-recorded data </td></tr>

</table>