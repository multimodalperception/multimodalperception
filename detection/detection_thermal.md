# Detection Thermal 
<a id="bck" href="/index.html#introtab"><b>Back to index</b></a> &nbsp; &nbsp;
<a href="/detection.html#bck"><b>Back to Detection</b></a> &nbsp; &nbsp;
<a href="/detection/detection_2d.html#bck"><img src="/img/2D.png" alt="2D" width="50"/></a> &nbsp; 
<a href="/detection/detection_3d.html#bck"><img src="/img/3D.png" alt="3D" width="50"/></a> &nbsp; 
<a href="/detection/detection_thermal.html#bck"><img src="/img/Thermal.png" alt="Thermal" width="50"/></a> &nbsp;
<a href="/detection/detection_lidar.html#bck"><img src="/img/LiDAR.png" alt="LiDAR" width="50"/></a> &nbsp;
<a href="/detection/detection_radar.html#bck"><img src="/img/Radar.png" alt="Radar" width="50"/></a>

<table id="commontab">
<tr><th> Reference </th><th> Sensors </th><th> Object Type </th><th> Sensing Modality Representations and Processing </th><th> Network Pipeline </th><th> How to generate Region Proposals (RP) </th><th> When to fuse </th><th> Fusion Operation and Method </th><th> Fusion Level </th><th> Dataset(s) used </th></tr>

<tr><td valign="top"> Guan <i>et al.</i>, 2018 
    <a href="https://arxiv.org/abs/1802.09972">[pdf]</a><a href="./ref/guan2018fusion.bib">[ref]</a>
    </td><td valign="top"> Vision camera, thermal camera </td><td valign="top"> 2D Pedestrian </td><td valign="top"> RGB image, thermal image. Each processed by a base network built on VGG16 </td><td valign="top"> Faster-RCNN </td><td valign="top"> RPN with fused features </td><td valign="top"> Before and after RP </td><td valign="top"> Feature concatenation, Mixture of Experts </td><td valign="top"> Early,  Middle, Late </td><td valign="top"> KAIST Pedestrian Dataset </td></tr>

<tr><td valign="top"> Takumi <i>et al.</i>, 2017 
    <a href="https://dl.acm.org/citation.cfm?id=3126727">[pdf]</a><a href="./ref/takumi2017multispectral.bib">[ref]</a>
    </td><td valign="top"> Vision camera, thermal camera </td><td valign="top"> Multiple 2D objects </td><td valign="top"> RGB image, NIR, FIR, FIR image. Each processed by YOLO </td><td valign="top"> YOLO </td><td valign="top"> YOLO predictions for each spectral image </td><td valign="top"> After RP </td><td valign="top"> Ensemble: ensemble final predictions for each YOLO detector </td><td valign="top"> Late </td><td valign="top"> self-recorded data</td></tr>

<tr><td valign="top"> Wagner <i>et al.</i>, 2016 
    <a href="https://www.elen.ucl.ac.be/Proceedings/esann/esannpdf/es2016-118.pdf">[pdf]</a><a href="./ref/wagner2016multispectral.bib">[ref]</a>
    </td><td valign="top"> Vision camera, thermal camera </td><td valign="top"> 2D Pedestrian </td><td valign="top"> RGB image, thermal image. Each processed by CaffeeNet </td><td valign="top"> R-CNN </td><td valign="top"> ACF+T+THOG detector </td><td valign="top"> After RP </td><td valign="top"> Feature concatenation </td><td valign="top"> Early, Late </td><td valign="top"> KAIST Pedestrian Dataset </td></tr>

<tr><td valign="top"> Liu <i>et al.</i>, 2016 
    <a href="https://dx.doi.org/10.5244/C.30.73">[pdf]</a><a href="./ref/liu2016bmvc.bib">[ref]</a>
    </td><td valign="top"> Vision camera, thermal camera </td><td valign="top"> 2D Pedestrian </td><td valign="top"> RGB image, thermal image. Each processed by NiN network </td><td valign="top"> Faster-RCNN </td><td valign="top"> RPN with fused (or separate) features </td><td valign="top"> Before and after RP </td><td valign="top"> Feature concatenation, average mean, Score fusion (Cascaded CNN) </td><td valign="top"> Early, Middle, Late </td><td valign="top"> KAIST Pedestrian Dataset </td></tr>
</table>