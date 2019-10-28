# Detection LiDAR
<a id="bck" href="/index.html#introtab"><b>Back to index</b></a> &nbsp; &nbsp;
<a href="/detection.html#bck"><b>Back to Detection</b></a> &nbsp; &nbsp;
<a href="/detection/detection_2d.html#bck"><img src="/img/2D.png" alt="2D" width="50"/></a> &nbsp; 
<a href="/detection/detection_3d.html#bck"><img src="/img/3D.png" alt="3D" width="50"/></a> &nbsp; 
<a href="/detection/detection_thermal.html#bck"><img src="/img/Thermal.png" alt="Thermal" width="50"/></a> &nbsp;
<a href="/detection/detection_lidar.html#bck"><img src="/img/LiDAR.png" alt="LiDAR" width="50"/></a> &nbsp;
<a href="/detection/detection_radar.html#bck"><img src="/img/Radar.png" alt="Radar" width="50"/></a>

<table id="commontab">
<tr><th> Reference </th><th> Sensors </th><th> Object Type </th><th> Sensing Modality Representations and Processing </th><th> Network Pipeline </th><th> How to generate Region Proposals (RP) </th><th> When to fuse </th><th> Fusion Operation and Method </th><th> Fusion Level </th><th> Dataset(s) used </th></tr>

<tr><td valign="top"> Chadwick <i>et al.</i>, 2019 
    <a href="https://arxiv.org/pdf/1901.10951">[pdf]</a><a href="./ref/chadwick2019distant.bib">[ref]</a>
    </td><td valign="top"> Radar, visual camera </td><td valign="top"> 2D Vehicle </td><td valign="top"> Radar range and velocity maps, RGB image. Each processed by ResNet </td><td valign="top"> One stage detector </td><td valign="top"> Predictions with fused features </td><td valign="top"> Before RP </td><td valign="top"> Addition, feature concatenation </td><td valign="top"> Middle </td><td valign="top"> Self-recorded </td></tr>

</table>