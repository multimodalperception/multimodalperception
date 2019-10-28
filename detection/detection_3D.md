# Detection 3D
<a id="bck" href="/index.html#introtab"><b>Back to index</b></a> &nbsp; &nbsp;
<a href="/detection.html#bck"><b>Back to Detection</b></a> &nbsp; &nbsp;
<a href="/detection/detection_2d.html#bck"><img src="/img/2D.png" alt="2D" width="50"/></a> &nbsp; 
<a href="/detection/detection_3d.html#bck"><img src="/img/3D.png" alt="3D" width="50"/></a> &nbsp; 
<a href="/detection/detection_thermal.html#bck"><img src="/img/Thermal.png" alt="Thermal" width="50"/></a> &nbsp;
<a href="/detection/detection_lidar.html#bck"><img src="/img/LiDAR.png" alt="LiDAR" width="50"/></a> &nbsp;
<a href="/detection/detection_radar.html#bck"><img src="/img/Radar.png" alt="Radar" width="50"/></a>

<table id="commontab">
<tr><th> Reference </th><th> Sensors </th><th> Object Type </th><th> Sensing Modality Representations and Processing </th><th> Network Pipeline </th><th> How to generate Region Proposals (RP) </th><th> When to fuse </th><th> Fusion Operation and Method </th><th> Fusion Level </th><th> Dataset(s) used </th></tr>

<tr><td valign="top">Liang <i>et al.</i>, 2019
    <a href="http://openaccess.thecvf.com/content_CVPR_2019/papers/Liang_Multi-Task_Multi-Sensor_Fusion_for_3D_Object_Detection_CVPR_2019_paper.pdf">[pdf]</a><a href="./ref/liang2019multi.bib">[ref]</a>
    </td><td valign="top">LiDAR, visual camera</td><td valign="top">3D Car, Pedestrian, Cyclist </td><td valign="top">LiDAR BEV maps, RGB image. Each processed by a ResNet with auxiliary tasks: depth estimation and ground segmentation</td><td valign="top">Faster R-CNN</td><td valign="top">Predictions with fused features</td><td valign="top">Before RP</td><td valign="top">Addition, continuous fusion layer</td><td valign="top">Middle</td><td valign="top">KITTI, self-recorded </td></tr>

<tr><td valign="top">Wang <i>et al.</i>, 2019
    <a href="https://arxiv.org/pdf/1903.01864">[pdf]</a><a href="./ref/wang2019frustum.bib">[ref]</a>
    </td><td valign="top">LiDAR, visual camera</td><td valign="top">3D Car, Pedestrian, Cyclist, Indoor objects</td><td valign="top">LiDAR voxelized frustum (each frustum processed by the PointNet), RGB image (using a pre-trained detector).</td><td valign="top">R-CNN</td><td valign="top">Pre-trained RGB image detector</td><td valign="top">After RP</td><td valign="top">Using RP from RGB image detector to build LiDAR frustums</td><td valign="top">Late</td><td valign="top">KITTI, SUN-RGBD </td></tr>

<tr><td valign="top">Dou <i>et al.</i>, 2019
    <a href="https://ieeexplore.ieee.org/abstract/document/8793492">[pdf]</a><a href="./ref/dou2019seg.bib">[ref]</a>
    </td><td valign="top">LiDAR, visual camera</td><td valign="top">3D Car</td><td valign="top">LiDAR voxel (processed by VoxelNet), RGB image (processed by a FCN to get semantic features)</td><td valign="top">Two stage detector</td><td valign="top">Predictions with fused features</td><td valign="top">Before RP</td><td valign="top">Feature concatenation</td><td valign="top">Middle</td><td valign="top">KITTI  </td></tr>

<tr><td valign="top">Sindagi <i>et al.</i>, 2019
    <a href="https://arxiv.org/pdf/1904.01649">[pdf]</a><a href="./ref/sindagi2019mvx.bib">[ref]</a>
    </td><td valign="top">LiDAR, visual camera</td><td valign="top">3D Car</td><td valign="top">LiDAR voxel (processed by VoxelNet), RGB image (processed by a pre-trained 2D image detector).</td><td valign="top">One stage detector</td><td valign="top">Predictions with fused features</td><td valign="top">Before RP</td><td valign="top">Feature concatenation</td><td valign="top"><b>Early</b>, Middle</td><td valign="top">KITTI  </td></tr>

<tr><td valign="top"> Liang <i>et al.</i>, 2018 
    <a href="http://openaccess.thecvf.com/content_ECCV_2018/papers/Ming_Liang_Deep_Continuous_Fusion_ECCV_2018_paper.pdf">[pdf]</a><a href="./ref/liang2018deep.bib">[ref]</a>
    </td><td valign="top"> LiDAR, vision camera </td><td valign="top"> 3D Car, Pedestrian, Cyclist </td><td valign="top"> LiDAR BEV maps, RGB image. Each processed by ResNet </td><td valign="top"> One stage detector </td><td valign="top"> Predictions with fused features. </td><td valign="top"> Before RP </td><td valign="top"> Addition, continuous fusion layer </td><td valign="top"> Middle </td><td valign="top"> KITTI, self-recorded </td></tr>

<tr><td valign="top"> Du <i>et al.</i>, 2018 
    <a href="https://arxiv.org/abs/1803.00387">[pdf]</a><a href="./ref/du2018general.bib">[ref]</a>
    </td><td valign="top"> LiDAR, vision camera </td><td valign="top"> 3D Car </td><td valign="top"> LiDAR voxel (processed by RANSAC and model fitting), RGB image (processed by VGG16 and GoogLeNet) </td><td valign="top"> R-CNN </td><td valign="top"> Pre-trained RGB image detector produces 2D bounding boxes to crop LiDAR points, which are then clustered </td><td valign="top"> Before and at RP </td><td valign="top"> Ensemble: use RGB image detector to regress car dimensions for a model fitting algorithm. </td><td valign="top"> Late </td><td valign="top"> KITTI, self-recorded data </td></tr>

<tr><td valign="top"> Yang <i>et al.</i>, 2018 
    <a href="https://ieeexplore.ieee.org/abstract/document/8428696/">[pdf]</a><a href="./ref/yang2018fusion.bib">[ref]</a>
    </td><td valign="top"> LiDAR, HD-map </td><td valign="top"> 3D Car </td><td valign="top"> LiDAR BEV maps, Road mask image from HD map. Inputs processed by PIXOR++ <a href="/ref/yang2018pixor.bib">[ref]</a> with the backbone similar to FPN </td><td valign="top"> One stage detector </td><td valign="top"> Detector predictions </td><td valign="top"> Before RP </td><td valign="top"> Feature concatenation </td><td valign="top"> Early </td><td valign="top"> KITTI, TOR4D Dataset~<a href="/ref/yang2018pixor.bib">[ref]</a></td></tr>

<tr><td valign="top"> Casas <i>et al.</i>, 2018 
    <a href="http://proceedings.mlr.press/v87/casas18a.html">[pdf]</a><a href="./ref/casas2018intentnet.bib">[ref]</a>
    </td><td valign="top"> LiDAR, HD-map </td><td valign="top"> 3D Car </td><td valign="top"> sequential LiDAR BEV maps, sequential several road topology mask images from HD map. Each input processed by a base network with residual blocks </td><td valign="top"> One stage detector </td><td valign="top"> Detector predictions </td><td valign="top"> Before RP </td><td valign="top"> Feature concatenation </td><td valign="top"> Middle </td><td valign="top"> self-recorded data </td></tr>

<tr><td valign="top"> Shin <i>et al.</i>, 2018 
    <a href="https://arxiv.org/abs/1811.03818">[pdf]</a><a href="./ref/shin2018roarnet.bib">[ref]</a>
    </td><td valign="top"> LiDAR, vision camera </td><td valign="top"> 3D Car </td><td valign="top"> LiDAR point clouds, (processed by PointNet <a href="/ref/qi2017pointnet.bib">[ref]</a>); RGB image (processed by a 2D CNN) </td><td valign="top"> R-CNN </td><td valign="top"> A 3D object detector for RGB image </td><td valign="top"> After RP </td><td valign="top"> Using RP from RGB image detector to search LiDAR point clouds </td><td valign="top"> Late </td><td valign="top"> KITTI </td></tr>

<tr><td valign="top"> Chen <i>et al.</i>, 2017 
    <a href="http://openaccess.thecvf.com/content_cvpr_2017/papers/Chen_Multi-View_3D_Object_CVPR_2017_paper.pdf">[pdf]</a><a href="./ref/chen2017multi.bib">[ref]</a>
    </td><td valign="top"> LiDAR, vision camera </td><td valign="top"> 3D Car </td><td valign="top"> LiDAR BEV and spherical maps, RGB image. Each processed by a base network built on VGG16 </td><td valign="top"> Faster-RCNN </td><td valign="top"> A RPN from LiDAR BEV map </td><td valign="top"> After RP </td><td valign="top"> average mean, deep fusion </td><td valign="top"> Early, Middle, Late </td><td valign="top"> KITTI </td></tr>

<tr><td valign="top"> Wang <i>et al.</i>, 2017 
    <a href="https://arxiv.org/pdf/1711.06703">[pdf]</a><a href="./ref/wang2017fusing.bib">[ref]</a>
    </td><td valign="top"> LiDAR, vision camera </td><td valign="top"> 3D Car, Pedestrian  </td><td valign="top"> LiDAR BEV map, RGB image. Each processed by a RetinaNet <a href="/ref/lin2018focal.bib">[ref]</a> </td><td valign="top"> One stage detector </td><td valign="top"> Fused LiDAR and RGB image features extracted from CNN </td><td valign="top"> Before RP </td><td valign="top"> Sparse mean manipulation </td><td valign="top"> Middle </td><td valign="top"> KITTI </td></tr>

<tr><td valign="top"> Ku <i>et al.</i>, 2017 
    <a href="https://arxiv.org/abs/1712.02294">[pdf]</a><a href="./ref/ku2017joint.bib">[ref]</a>
    </td><td valign="top"> LiDAR, vision camera </td><td valign="top"> 3D Car, Pedestrian, Cyclist  </td><td valign="top"> LiDAR BEV map, RGB image. Each processed by VGG16 </td><td valign="top"> Faster-RCNN </td><td valign="top"> Fused LiDAR and RGB image features extracted from CNN </td><td valign="top"> Before and after RP </td><td valign="top"> Average mean </td><td valign="top"> Early, Middle, Late </td><td valign="top"> KITTI </td></tr>

<tr><td valign="top"> Xu <i>et al.</i>, 2017 
    <a href="http://openaccess.thecvf.com/content_cvpr_2018/CameraReady/0766.pdf">[pdf]</a><a href="./ref/xu2017pointfusion.bib">[ref]</a>
    </td><td valign="top"> LiDAR, vision camera </td><td valign="top"> 3D Car, Pedestrian, Cyclist, Indoor objects  </td><td valign="top"> LiDAR points (processed by PointNet), RGB image (processed by ResNet) </td><td valign="top"> R-CNN </td><td valign="top"> Pre-trained RGB image detector </td><td valign="top"> After RP </td><td valign="top"> Feature concatenation for local and global features </td><td valign="top"> Middle </td><td valign="top"> KITTI, SUN-RGBD </td></tr>

<tr><td valign="top"> Qi <i>et al.</i>, 2017 
    <a href="http://openaccess.thecvf.com/content_cvpr_2018/papers/Qi_Frustum_PointNets_for_CVPR_2018_paper.pdf">[pdf]</a><a href="./ref/qi2017frustum.bib">[ref]</a>
    </td><td valign="top"> LiDAR, vision camera </td><td valign="top"> 3D Car, Pedestrian, Cyclist, Indoor objects  </td><td valign="top"> LiDAR points (processed by PointNet), RGB image (using a pre-trained detector) </td><td valign="top"> R-CNN </td><td valign="top"> Pre-trained RGB image detector </td><td valign="top"> After RP </td><td valign="top"> Feature concatenation </td><td valign="top"> Middle, Late </td><td valign="top"> KITTI, SUN-RGBD </td></tr>
</table>