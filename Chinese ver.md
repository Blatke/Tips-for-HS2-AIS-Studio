# 关于HS2和AI少女的小贴士 
Bl@ke/文
（[http://www.blatke.cc](http://www.blatke.cc/)）

Honey Select 2 - 以下简称HS2；
AI-Shoujo、AI-Girl或AI少女 - 以下简称AI；
工作室Studio除了默认画面模式外，还有两种第三方插件提供的画面模式：DHH和Graphics，可在启动界面（InitSetting.exe）切换模式。
-----

1. 插件目录
HS2：[https://github.com/ManlyMarco/HS2-HF_Patch/blob/master/Plugin%20Readme.md](https://github.com/ManlyMarco/HS2-HF_Patch/blob/master/Plugin%20Readme.md)
AI：[https://github.com/ManlyMarco/AI-HF_Patch/blob/master/Plugin%20Readme.md](https://github.com/ManlyMarco/AI-HF_Patch/blob/master/Plugin%20Readme.md) 
2. Mods哪里找？
HS2和AI的mods基本是通用的。
-Discord：[https://discord.gg/illusionsoft](https://discord.gg/illusionsoft)
	这是民间I社游戏的discord服务器，可以在hs2-mod-sharing和old-hs2-mod-sharing这两个频道里寻找mods。

-Betterrepack mods：[https://sideload.betterrepack.com/download/AISHS2/](https://sideload.betterrepack.com/download/AISHS2/) 
	该列表定期从上面的discord上整理更新mods，但我个人建议还是在discord上找，因为作者发布mods的同时，也会把一些使用说明写在discord帖子上，而这个列表只有mod文件，不附带说明。
	另建议善用Google搜索该网址，例如在搜索关键字后面加site:sideload.betterrepack.com 
3. 女奥皮肤贴图
详见本群（904857543）群文件的HS2文件夹。

4. 身体如何反光
选择人物角色，打开材质编辑器MaterialEditor，搜索“身体”或“body”。
找到该材质下有：
- 光泽glossiness，控制材质反射光源的效果；
- 金属感metallic，控制材质反射光源时的高光与非高光部分的对比度，非高光部分会反射周边环境。
适当调整上述两个数值，我一般光泽是0.8，金属是0.75。

金属值拉高时，你可能会发现，人体变暗了。这是因为周边环境是暗的，或没有反射探针（reflection probe），所以人体想反射也反射不了。
解决办法是添加一个Reflection Probe，这是工作室的物品，整合包的玩家可能直接在工作室物品搜索中找到。没有安装的，可在这里下载：https://drive.google.com/file/d/1B7cn4FXdYTGE4W96rVcL5jmbHJ3JOjnq/view 
添加后，这个物品以自己为圆心做全景截图，并将截图贴到场景中光泽和金属数值较大的物品上，达成光滑反射甚至镜面反射的效果。
DHH和Graphics两种模式均支持其功能，不过Graphics支持度更好。
这是在工作室里添加了一个天空盒skybox作为背景，又添加了一个平平无奇的球体Sphere，最后添加了Reflection Probe。

在DHH模式下，将球体的金属和光泽拉满，并把DHH界面中的“贴图金属反射”拉满，就实现了上图效果。注意：DHH下Reflection Probe反射的内容只是它被添加到场景那一刻的环境，并不会实时变化。可删除再重新添加来刷新反射内容。

在Graphics模式下，勾选Reflection Probes，将Reflection Probe的重要性importance拉满，适当调整强度intensity，就是上述效果。还可以在设置Settings里，勾选“实时反射探头”，即可使反射内容根据场景变化而调整。

同时注意，无论哪个模式，Reflection Probe反射的内容都跟它的所在位置有关。

