<p align="center">
  <img src = "./imgs/logo.png" width="60%">
</p>

# M<sup>2</sup>DSet: A Novel Multi-view and Multimodal dataset for Long-range and Robust Perception
We develop and release an innovative multi-view and multimodal dataset, dubbed M<sup>2</sup>DSet. M<sup>2</sup>DSet surpasses existing datasets with higher-resolution, longer-range, and more robust multimodal sensors (Fig. 1c). It provides 360° image data, 4D radar data, and LiDAR data, enabling a comprehensive perception capability. As an emerging range sensor, 4D radar can offer complete measurement of 3D position, as well as denser point clouds than 3D radar. These enhancements are particularly valuable in complex driving conditions, especially under adverse weather conditions. Importantly, M2DSet incorporates high-precision and long-range annotations up to 210 meters, significantly extending the practical range for 3D object detection. Another distinctive aspect of M<sup>2</sup>DSet is the inclusion of three front-view cameras with varying focal lengths. This deliberate design significantly enhances both the perceptual range and accuracy of the vision system. Additionally, this design can improve the image feature extraction of distant objects, thus facilitating more effective fusion with long-range sensor data, such as LiDAR or 4D radar. To the best of our knowledge, M<sup>2</sup>DSet is the first publicly available AD dataset that incorporates LiDAR, cameras with various focal lengths, and 4D radar, uniquely designed to simultaneously support long-range, robust, and panoramic perception. 
</p>

<p align="center">
  <img src = "./imgs/scene.png" width="100%">
</p>

# News

[2024.05.10] Our Code currently supports some baselines including PETR, Pointpillars, and Second. 

# 1. Introduction
<p style=""text-align:justify; text-justify:interideograph;">
  In pursuit of a diverse and comprehensive dataset, extensive data collection is conducted in the cities of Zhuzhou and Changsha, China. The M2DSet dataset encompasses approximately 8 hours of meticulously gathered data, covering a broad spectrum of driving conditions. Data collection spans multiple time periods to capture the diverse traffic dynamics at different times of the day, thus enhancing the dataset's generalization capability. The dataset includes typical autonomous driving scenarios such as urban roads, suburban roads, highways, and tunnels, with additional nighttime data collections to further expand dataset diversity. Adverse weather conditions such as fog and rain scenarios are also incorporated. Following the data collection phase, manual processing is undertaken to curate a set of 17.2K key frames, selected at regular 0.5-second intervals. These frames are organized into 430 sequences, each depicting a unique driving scenario. Data capture is comprehensively executed using eight cameras, a top-mounted LiDAR, and a frontal 4D radar, ensuring 360° environmental coverage around the ego-vehicle.  This strategic assembly of data not only facilitates a robust and extensive coverage but also significantly enhances the dataset’s utility in developing advanced autonomous driving algorithms.
</p>

# Overall architecture of the data collection platform
To enhance the long-range and multi-view capabilities essential for autonomous driving perception, we have developed an advanced multimodal perception system, as presented in Fig. 2a. This system comprises eight high-resolution cameras, a front-mounted 4D radar, and a top-mounted 80-line LiDAR. In autonomous driving scenarios, perception requirements vary with the ego-vehicle orientation. The frontal direction, being critical for navigation and safety, is often prioritized to achieve enhanced perception capabilities 30, 39. Accordingly, our platform incorporates three front-view cameras with varying focal lengths and field-of-view (FOV) characteristics. The remaining five cameras are strategically distributed around the vehicle to work in conjunction with the front-view cameras, providing comprehensive panoramic coverage. This configuration enables our vision system to achieve a detailed understanding of the surrounding environment while maintaining long-range detection capabilities. Additionally, a high-resolution and long-range LiDAR is mounted on the vehicle’s roof, which can significantly enhance the 3D perception capability by providing accurate location and geometric information of surrounding objects. Robustness in autonomous driving systems is essential, particularly under adverse driving conditions. While LiDAR is effective across various lighting conditions, it has limitations in adverse weather due to point cloud degradation. To address these challenges, a 4D radar is integrated into the system, bolstering the overall robustness of the perception mechanisms. 
</p>

<div align=center>
<img src="./imgs/platform.png"  width="60%"/>
</div>
<p align="center"><font face="Helvetica" size=3.><b>Fig. 2 | Sensor Configuration and Specifications of the M2DSet Data Collection Platform.</b></font></p>
