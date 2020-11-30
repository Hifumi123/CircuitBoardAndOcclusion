# 电路板和遮挡

引擎原理课第五次作业。

作业中包含两个项目，CircuitBoard是电路板作业，Occlusion是遮挡作业。

在电路板作业中，使用所给的贴图实现了一个PBR材质，并用这个材质制作了一个电路板。然后使用Shader Graph插件制作了一个电流效果Shader并放在了电路板上。

在遮挡作业中，未开启遮挡剔除时，DC为816（运行时为793），如图：

![遮挡剔除](/README_IMG/OC_001.PNG)

![遮挡剔除](/README_IMG/OC_002.PNG)

Overdraw如图：

![遮挡剔除](/README_IMG/OC_003.PNG)

开启遮挡剔除后，DC为630（运行时为393），如图：

![遮挡剔除](/README_IMG/OC_004.PNG)

![遮挡剔除](/README_IMG/OC_005.PNG)

Overdraw如图：

![遮挡剔除](/README_IMG/OC_006.PNG)

通过调整Occlusion Area和烘培参数来减少烘培数据大小，默认参数产生的烘培数据的大小为18.4KB，如图：

![遮挡剔除](/README_IMG/OC_007.PNG)

调整后为12.0KB，如图：

![遮挡剔除](/README_IMG/OC_008.PNG)

开发环境为Unity 2019.4，CircuitBoard项目需要High Definition RP插件和Shader Graph插件。

CircuitBoard项目的主场景在Assets\Scenes目录下，Occlusion项目的主场景在Assets\Occlusion目录下。