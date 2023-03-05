# 中文摘要

危化品装配的智能化不仅是提升效率的问题，更大的意义在于拯救一线工人的生命。危化品装配设备中，待装工件的6D姿态估计是基于机器视觉的控制回路中的核心技术，其精度和鲁棒性决定了装备的可用性。实际的装配车间中，工件通常表面纹理较弱，且相互之间有遮挡，为特征提取和匹配代价计算带来了极大的困难，现有的6D姿态估计算法流程很难解决。本项目针对这些问题，分析危化品在不同光谱谱段的响应特性，研究光谱影像的特征图，利用多模态信息之间的互补性提升目标检测的精度；研究如何利用刚体的可见部分和掩膜对遮挡区域的检测框学习过程进行监督，实现刚体目标的鲁棒3D检测；分析如何将工件模型的几何特征引入目标图像和渲染图像的匹配计算过程，提升修正后位姿的精度。通过几项关键技术改进的组合，提高危化品智能装配中复杂场景下的工件6D姿态估计性能，解决智能装配设备的准确性和鲁棒性难题。

# 英文摘要

The intelligence of hazardous chemical assembly is not only a matter of improving efficiency but also has a greater significance in saving the lives of front-line workers. In dangerous chemical assembly equipment, 6D attitude estimation of the workpiece to be assembled is the core technology in the control loop based on machine vision, and its accuracy and robustness determine the availability of the equipment. In the actual assembly shop, the workpieces usually have soft surface textures and are occluded from each other, which brings great difficulties for feature extraction and matching cost calculation, and the existing 6D pose estimation algorithm process is difficult to solve. This project addresses these problems by analyzing the response characteristics of hazardous chemicals in different spectral bands, studying the feature maps of spectral images, using the complementarity between multimodal information to improve the accuracy of target detection; studying how to use the visible part of the rigid body and the mask to supervise the learning process of the detection frame in the occluded region to achieve robust 3D detection of the rigid body target; analyzing how to introduce the geometric features of the workpiece model into the target image and rendered images to improve the accuracy of the corrected pose. Through the combination of several critical technical improvements, the performance of 6D pose estimation of workpieces in complex scenarios in the intelligent assembly of hazardous chemicals is improved, and the accuracy and robustness challenges of intelligent assembly devices are solved.


# 科学问题属性
请阐明选择该科学问题属性的理由（800字以内，含标点符号）：
“需求牵引，突破瓶颈”：科学问题源于国家重大需求和经济主战场，且具有鲜明的需求导向、问题导向和目标导向特征，旨在通过解决技术瓶颈背后的核心科学问题，促使基础研究成果走向应用。

三年疫情使装备制造类企业意识到智能制造升级的迫切性，这一需求在危化品领域更为强烈。目前我国的危化品制造大量依赖技术工人的劳动力，对于工人的熟练程度和工作时间都有很高要求，导致疫情期间企业生产举步维艰。近几年我国航天科工集团和兵器工业集团相关研究所都出现过不同程度的生产事故，其中工人的疲劳误操作是主要原因之一。为了解决这些问题，相关企业都在寻求智能制造升级。然而，智能制造装备是半定制设备，需针对制造工艺流程进行部分定制化研发。

智能装配需通过机械臂相机捕获场景图像，进行工件和材料的检测、识别和姿态估计，然后驱动机械臂完成装配作业。相机捕获的图像中，工业零件的表面纹理较弱，且有相互遮挡的干扰，这些是智能制造定制化研发中要重点解决的问题。危化品的装配难度系数更高，含能部件装配有着小批量、多样化的特点，不同型号部件的尺寸和弹性模量差异较大，部分含能部件表面容易破损甚至变形碎裂，使用常规位置型机器人装配时，含能部件会使微小的位置偏差产生很大的作用力，导致含能部件装配失败，甚至损坏含能部件。而且，含能部件是一种亚稳态物质，含能高，对震动及压力极其敏感，不当的受力、受热、火花、摩擦、撞击、碰撞或针刺都可能导致危险事故的发生，造成严重的人员伤亡。

但由于危化品的成分特殊，物质辐射的光在全谱段有脉冲响应的特性，所采集的光谱图轮廓清晰，噪声小，这反而为提升检测和姿态估计的精度提供了另一条可行思路。我们将基于团队在光谱影像分析、深度图点云处理和6D姿态估计方面的基础，分析和研究深度学习网络的结构，对可见光图像、深度图和光谱影像的特征进行不同尺度和特征层次的交叉融合。同时，将利用工件的刚体特性，用未遮挡区域的掩膜监督物体完整3D边框的检测，并利用工件的CAD模型进行投影匹配，提高位姿修正的精度，最终输出高精度的目标工件6D姿态，解决危化品智能装配设备中的准确度和可靠性两个核心难题。

