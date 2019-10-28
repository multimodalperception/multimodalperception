# Segmentation Thermal
<a id="bck" href="/index.html#introtab"><b>Back to index</b></a> &nbsp; &nbsp;
<a href="/segmentation.html#bck"><b>Back to Segmentation</b></a> &nbsp; &nbsp;
<a href="/segmentation/segmentation_2d.html#bck"><img src="/img/2D.png" alt="2D" width="50"/></a> &nbsp; 
<a href="/segmentation/segmentation_3d.html#bck"><img src="/img/3D.png" alt="3D" width="50"/></a> &nbsp; 
<a href="/segmentation/segmentation_thermal.html#bck"><img src="/img/Thermal.png" alt="Thermal" width="50"/></a> &nbsp;
<a href="/segmentation/segmentation_lidar.html#bck"><img src="/img/LiDAR.png" alt="LiDAR" width="50"/></a>

<table id="commontab">
<tr><th id="segmentation"> Reference </th><th id="segmentation"> Sensors </th><th id="segmentation"> Semantics </th><th id="segmentation"> Sensing Modality Representations </th><th id="segmentation"> Fusion Operation and Method </th><th id="segmentation"> Fusion Level </th><th> Dataset(s) used </th></tr>

<tr><td valign="top">Valada <i>et al.</i>, 2019
    <a href="https://arxiv.org/pdf/1808.03833">[pdf]</a><a href="./ref/valada2018self.bib">[ref]</a>
    </td><td valign="top"> Visual camera, depth camera, thermal camera  </td><td valign="top"> Multiple 2D objects </td><td valign="top"> RGB image, thermal image, depth image. Each processed by FCN with ResNet backbone (Adapnet++ architecture) </td><td valign="top"> Extension of Mixture of Experts </td><td valign="top"> Middle </td><td valign="top"> Six datasets, including Cityscape, Sun RGB-D, etc. </td></tr>

<tr><td valign="top">Sun <i>et al.</i>, 2019
    <a href="https://ieeexplore.ieee.org/abstract/document/8666745">[pdf]</a><a href="./ref/sun2019rtfnet.bib">[ref]</a>
    </td><td valign="top"> Visual camera, thermal camera </td><td valign="top"> Multiple 2D objects in campus environments </td><td valign="top"> RGB image, thermal image. Each processed by a base network built on ResNet </td><td valign="top"> Element-wise summation in the encoder networks </td><td valign="top"> Middle </td><td valign="top"> Datasets published by <a href="../ref/ha2017mfnet.bib">[ref]</a> </td></tr>

<tr><td valign="top"> Guan <i>et al.</i>, 2018 
    <a href="https://arxiv.org/abs/1802.09972">[pdf]</a><a href="./ref/guan2018fusion.bib">[ref]</a>
    </td><td valign="top"> Vision camera, thermal camera </td><td valign="top"> 2D Pedestrian </td><td valign="top"> RGB image, thermal image. Each processed by a base network built on VGG16 </td><td valign="top"> Feature concatenation, Mixture of Experts </td><td valign="top"> Early, Middle, Late </td><td valign="top"> KAIST Pedestrian Dataset </td></tr>

<tr><td valign="top"> Ha <i>et al.</i>, 2017 
    <a href="https://ieeexplore.ieee.org/abstract/document/8206396/">[pdf]</a><a href="./ref/ha2017mfnet.bib">[ref]</a>
    </td><td valign="top"> Vision camera, thermal camera </td><td valign="top"> Multiple 2D objects in campus environments </td><td valign="top"> RGB image, thermal image. Each processed by a FCN and mini-inception block </td><td valign="top"> Feature concatenation, addition (``short-cut fusion'') </td><td valign="top"> Middle </td><td valign="top"> self-recorded data </td></tr>

<tr><td valign="top"> Valada <i>et al.</i>, 2017 
    <a href="http://ais.informatik.uni-freiburg.de/publications/papers/valada17icraa.pdf">[pdf]</a><a href="./ref/valada2017adapnet.bib">[ref]</a>
    </td><td valign="top"> Vision camera, thermal camera </td><td valign="top"> Multiple 2D objects </td><td valign="top"> RGB image, thermal image, depth image. Each processed by FCN with ResNet backbone </td><td valign="top"> Mixture of Experts </td><td valign="top"> Late </td><td valign="top"> Cityscape, Freiburg Multispectral Dataset, Synthia </td></tr>

<tr><td valign="top"> Valada <i>et al.</i>, 2016 
    <a href="https://link.springer.com/chapter/10.1007/978-3-319-50115-4_41">[pdf]</a><a href="./ref/valada2016deep.bib">[ref]</a>
    </td><td valign="top"> Vision camera, thermal camera </td><td valign="top"> Multiple 2D objects in forested environments </td><td valign="top"> RGB image, thermal image, depth image. Each processed by the UpNet (built on VGG16 and up-convolution) </td><td valign="top"> Feature concatenation, addition </td><td valign="top"> Early, Late </td><td valign="top"> self-recorded data </td></tr>

</table>