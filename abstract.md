# 中文摘要

危化品装配的智能化不仅是提升效率的问题，更大的意义在于拯救一线工人的生命。智能装配机械臂的控制依赖于机器视觉反馈的精准定位，而其中待装工件的6D姿态估计是核心算法，其精度和鲁棒性决定了智能装备能否完全替代人工。实际的装配车间中，工件通常表面纹理较弱，且相互之间有遮挡，这为特征提取和匹配代价计算带来了极大的困难，现有的6D姿态估计算法流程很难解决。本项目针对这些问题，研究多源融合估计的解决方法。通过分析危化品的光谱响应特性，利用多模态信息之间的互补性提升目标检测的精度；研究如何利用刚体的可见部分和掩膜对遮挡区域的检测框学习过程进行监督，提高刚体目标3D检测的鲁棒性；分析如何将工件模型的几何特征引入目标图像和渲染图像的匹配计算过程，提升修正后位姿的精度。通过几项关键技术改进的组合，提高危化品智能装配中复杂场景下的工件6D姿态估计性能，解决智能装配设备的准确性和鲁棒性难题。

# 英文摘要

The intellectualization of hazardous chemical assembly is not only a matter of improving efficiency but also has a greater significance in saving the lives of front-line workers. The robotic arm control relies on the accurate positioning of machine vision feedback. Within this, the 6D pose estimation of the workpiece is the core algorithm, whose accuracy and robustness determine whether the intelligent equipment can completely replace human labor. In the actual assembly line, the workpieces usually have weak surface textures and are occluded from each other, which brings lots of difficulties for feature extraction and matching cost calculation. The existing 6D pose estimation algorithm can hardly solve this problem. In this project, we will investigate multi-source fusion algorithms to address these problems. We will improve the target detection accuracy by analyzing the spectral response characteristics of the hazardous chemical and fusing the complementary information among multimodal sources. We will also study how to improve the robustness of 3D detection of the rigid target by supervising the learning process of the detection frame in the occluded region using the visible part and the mask. Furthermore, we will analyze how to introduce the geometric features of the workpiece model into the matching calculation process of the target image and the rendered image to improve the accuracy of the corrected poses. By combining the technical improvements, we can improve the performance of 6D pose estimation in complex scenarios to a great extent. We aim to solve the accuracy and robustness challenges of intelligent assembly devices with the support of this project.




# 科学问题属性
请阐明选择该科学问题属性的理由（800字以内，含标点符号）：
“需求牵引，突破瓶颈”：科学问题源于国家重大需求和经济主战场，且具有鲜明的需求导向、问题导向和目标导向特征，旨在通过解决技术瓶颈背后的核心科学问题，促使基础研究成果走向应用。

三年疫情使装备制造类企业意识到智能制造升级的迫切性，这一需求在危化品领域更为强烈。目前我国的危化品制造大量依赖技术工人的劳动力，对于工人的熟练程度和工作时间都有很高要求，导致疫情期间企业生产举步维艰。近几年我国某几个重要研究所都出现过不同程度的生产事故，其中工人的疲劳误操作是主要原因之一。为了解决这些问题，相关企业都在寻求智能制造升级。然而，智能制造装备是半定制设备，需针对制造工艺流程进行部分定制化研发。

智能装配需通过机械臂相机捕获场景图像，进行工件和材料的检测、识别和姿态估计，然后驱动机械臂完成装配作业。相机捕获的图像中，工业零件的表面纹理较弱，且有相互遮挡的干扰，这些是智能制造定制化研发中要重点解决的问题。危化品的装配难度系数更高，含能部件装配有着小批量、多样化的特点，不同型号部件的尺寸和弹性模量差异较大，部分含能部件表面容易破损甚至变形碎裂，使用常规位置型机器人装配时，含能部件会使微小的位置偏差产生很大的作用力，导致含能部件装配失败，甚至损坏含能部件。而且，含能部件是一种亚稳态物质，含能高，对震动及压力极其敏感，不当的受力、受热、火花、摩擦、撞击、碰撞或针刺都可能导致危险事故的发生，造成严重的人员伤亡。

但由于危化品的成分特殊，物质辐射的光在特定谱段有脉冲响应的特性，所采集的光谱图轮廓清晰，噪声小，这反而为提升检测和姿态估计的精度提供了另一条可行思路。我们将基于团队在光谱影像分析、深度图点云处理和6D姿态估计方面的基础，分析和研究对应的深度学习网络结构，对可见光图像、深度图和光谱影像的特征进行不同尺度和特征层次的交叉融合。同时，将利用工件的刚体特性，用未遮挡区域的掩膜监督物体完整3D边框的检测，并利用工件的CAD模型进行投影匹配，提高位姿修正的精度，最终输出高精度的目标工件6D姿态，解决危化品智能装配设备中的准确度和可靠性两个核心难题。

# 附件

Structure-Aware Graph Convolution Network for Point Cloud Parsing
附件名称：面向深度图点云解析的结构感知图卷积神经网络
备注：2022年发表在《IEEE Transactions on Multimedia》，中科院一区，影响因子8.182，本人通信作者，一作为申请人指导的博士生。该工作针对点云解析问题，提出了结构感知的图卷积神经网络方法，为本项目的第一个研究内容奠定基础。

ASFM-Net: Asymmetrical Siamese Feature Matching Network for Point Completion
附件名称：面向点云补全的非对称孪生特征匹配网络
备注：2021年发表在ACM Multimedia会议，CCF-A类会议，做大会报告，在21年斯坦福3D点云补全算法国际排行榜排名第一，本人为通信作者，一作为申请人指导的硕士生。该工作针对点云补全问题提出了一种非对称孪生特征匹配网络，该工作为为本项目第一个研究内容奠定基础。

A Stepwise Domain Adaptive Segmentation Network With Covariate Shift Alleviation for Remote Sensing Imagery
附件名称：一种减弱方差漂移的步进式域自适应分割网络
备注：2022年发表在《IEEE Transactions on Geoscience and Remote Sensing》，中科院一区，影响因子8.125，本人为通信作者。该工作提出了一种减弱方差漂移的步进式域自适应分割网络，提升了图像分割精度，为本项目第一个研究内容奠定基础

Structure-Guided Feature Transform Hybrid Residual Network for Remote Sensing Object Detection
附件名称：面向遥感物体检测的结构引导特征变形混合残差网络
备注：2022年发表在《IEEE Transactions on Geoscience and Remote Sensing》，中科院一区，影响因子8.125，本人为通信作者。该工作的结构引导transformer残差网络为本项目的第二部分研究内容奠定了基础

Cao et al. - 2023 - HE2LM-AD Hierarchical and efficient attitude determination framework with adaptive error compensation module based o_(Optimized).pdf
附件名称：HE2LM-AD：基于极限学习机自适应误差补偿的层次化高效定姿框架
备注：2023年发表在《ISPRS Journal of Photogrammetry and Remote Sensing》，中科院一区，影响因子11.774，本人为通信作者，一作为申请人指导的博士生。该工作提出了一种基于极限学习机的误差补偿思路，该思路框架为本项目第三个研究内容奠定了基础
