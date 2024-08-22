# 关于HS2和AI少女工作室的小贴士 

**Bl@ke/文**

（[http://www.blatke.cc](http://www.blatke.cc/)）

Honey Select 2 - 以下简称HS2；

AI-Shoujo、AI-Girl或AI少女 - 以下简称AI；

工作室Studio除了默认画面模式外，还有两种第三方插件提供的画面模式：DHH和Graphics，可在启动界面（InitSetting.exe）切换模式。

## 插件目录
HS2：[https://github.com/ManlyMarco/HS2-HF_Patch/blob/master/Plugin%20Readme.md](https://github.com/ManlyMarco/HS2-HF_Patch/blob/master/Plugin%20Readme.md)

AI：[https://github.com/ManlyMarco/AI-HF_Patch/blob/master/Plugin%20Readme.md](https://github.com/ManlyMarco/AI-HF_Patch/blob/master/Plugin%20Readme.md) 
## Mods哪里找？
HS2和AI的mods基本是通用的。

### Discord
[https://discord.gg/illusionsoft](https://discord.gg/illusionsoft)

这是民间I社游戏的discord服务器，可以在hs2-mod-sharing和old-hs2-mod-sharing这两个频道里寻找mods。

### Betterrepack Mods Server
[https://sideload.betterrepack.com/download/AISHS2/](https://sideload.betterrepack.com/download/AISHS2/) 

该列表定期从上面的discord上整理更新mods，但我个人建议还是在discord上找，因为作者发布mods的同时，也会把一些使用说明写在discord帖子上，而这个列表只有mod文件，不附带说明。
 
另建议善用Google搜索该网址，例如在搜索关键字后面加site:sideload.betterrepack.com 
## 身体如何反光
选择人物角色，打开材质编辑器MaterialEditor，搜索“身体”或“body”。

找到该材质下有：

- 光泽glossiness，控制材质反射光源的效果；
- 金属感metallic，控制材质反射光源时的高光与非高光部分的对比度，非高光部分会反射周边环境。

适当调整上述两个数值，我一般光泽是0.8，金属是0.75。

金属值拉高时，你可能会发现，人体变暗了。这是因为周边环境是暗的，或没有反射探针（reflection probe），所以人体想反射也反射不了。

解决办法是添加一个Reflection Probe，这是工作室的物品，整合包的玩家可能直接在工作室物品搜索中找到。没有安装的，可在这里下载：[https://drive.google.com/file/d/1B7cn4FXdYTGE4W96rVcL5jmbHJ3JOjnq/view](https://drive.google.com/file/d/1B7cn4FXdYTGE4W96rVcL5jmbHJ3JOjnq/view) 

添加后，这个物品以自己为圆心做全景截图，并将截图贴到场景中光泽和金属数值较大的物品上，达成光滑反射甚至镜面反射的效果。

DHH和Graphics两种模式均支持其功能，不过Graphics支持度更好。

![K2SF@FMNODG%~{PM5(XTJH9](https://github.com/user-attachments/assets/ccda59fd-eb64-4cab-b86a-a30a8fb22462)

这是在工作室里添加了一个天空盒skybox作为背景，又添加了一个平平无奇的球体Sphere，最后添加了Reflection Probe。

![_ZX}YQSPQ@DIR5 KDJJCOQF](https://github.com/user-attachments/assets/6e7ebace-4715-4a45-89df-8f89f9e71d1e)

在DHH模式下，将球体的金属和光泽拉满，并把DHH界面中的“贴图金属反射”拉满，就实现了上图效果。注意：DHH下Reflection Probe反射的内容只是它被添加到场景那一刻的环境，并不会实时变化。可删除再重新添加来刷新反射内容。

![R0QF@{LYHHOHTD @7TGXLG](https://github.com/user-attachments/assets/446035a2-d443-4012-b305-b9d2b3c35d61)

在Graphics模式下，勾选Reflection Probes，将Reflection Probe的重要性importance拉满，适当调整强度intensity，就是上述效果。还可以在设置Settings里，勾选“实时反射探头”，即可使反射内容根据场景变化而调整。

同时注意，无论哪个模式，Reflection Probe反射的内容都跟它的所在位置有关。
## 将角色人物导出为FBX文件
**Grey.MeshExporter**是一款为Illusion游戏设计的角色导出插件，能够将恋活、HS、HS2、AI少女、PH工作室中的角色（及其衣服和配饰）导出为FBX模型文件和相关贴图，便于用户进一步导入3D建模软件中编辑。

Discord原作者消息：[https://discord.com/channels/446784086539763712/715932300382044170/858707187203309629](https://discord.com/channels/446784086539763712/715932300382044170/858707187203309629)

百度网盘下载地址
链接：[https://pan.baidu.com/s/18YqOwisEjaWXN-WxiMUaEw?pwd=2024](https://pan.baidu.com/s/18YqOwisEjaWXN-WxiMUaEw?pwd=2024)
提取码：2024

下载后解压，按自己的游戏找到相应名称的文件夹，将里面的BepInEx文件夹拖入你的游戏根目录，即可完成安装。

安装后，启动游戏的工作室Studio模式。添加任一人物角色，并确保在工作面板Workspace中选择该角色。按小键盘减号键 “-” 呼出Grey.MeshExporter操作面板，按Export按钮导出角色，即可将角色模型连带有关贴图一并导出至游戏根目录中的Export文件夹。

如有其它问题，可阅读该插件的文件夹里附带的READ ME - SERIOUSLY!.txt帮助文档。

### Grey.MeshExporter快捷键设置
若按减号键无反应，则需尝试通过修改Grey.MeshExporter的ini/cfg文件来重新设置快捷键。

1. 确保在安装Grey.MeshExporter后，至少启动过一次StudioNeo，这样，相应文件夹下将随着StudioNeo的启动而生成设置文件。

2. 在StudioNeo关闭的情况下，找到这个设置文件，此处有两种可能：

该文件位于：你的游戏根目录/BepInEx/Config/ 目录中；文件名一般为：Grey.MeshExporter.游戏名称.cfg。例如我使用的是AI少女，文件名为Grey.MeshExporter.AI.cfg。如下图：

![image](https://github.com/user-attachments/assets/e3b2d3ad-dd49-43df-a303-3a6ca2b59d9d)

游戏根目录/BepInEx/Config/Grey.MeshExporter.游戏名称.cfg
或者，该文件位于：你的游戏根目录/UserData/ 目录中；文件名一般为：ModPrefs.ini。

3. 用记事本或代码编辑软件打开此文件，找到以EportKey=或ExportShortcut=字样开头的代码行，使用快捷键关键词（见文末注释）将等号后面的代码改为你想要重新设置的快捷键名称。例如我这里改为：LeftShift + Minus ，也就是通过按左侧Shift+减号键（注意：按键顺序也可能是颠倒的，即先按减号键，再按左侧Shift键。总之都试试）来呼出插件面板。如下图：

![image](https://github.com/user-attachments/assets/6f4a8967-28bb-4bf5-8dd5-ee1dea90575c)

4. 保存文件。启动StudioNeo。按下你设置的快捷键，呼出插件面板。

![image](https://github.com/user-attachments/assets/01399f27-88b9-4ad9-b670-dcf9fd437cb1)

根据插件附带的READ ME - SERIOUSLY!.txt文件，可用于快捷键的关键字如下：

_ _None, Backspace, Tab, Clear, Return, Pause, Escape, Space, Exclaim, DoubleQuote, Hash, Dollar, Ampersand, Quote, LeftParen, RightParen, Asterisk, Plus, Comma, Minus, Period, Slash, Colon, Semicolon, Less, Equals, Greater, Question, At, LeftBracket, Backslash, RightBracket, Caret, Underscore, BackQuote, Delete, KeypadPeriod, KeypadDivide, KeypadMultiply, KeypadMinus, KeypadPlus, KeypadEnter, KeypadEquals, UpArrow, DownArrow, RightArrow, LeftArrow, Insert, Home, End, PageUp, PageDown, Numlock, CapsLock, ScrollLock, RightShift, LeftShift, RightControl, LeftControl, RightAlt, LeftAlt, RightApple, RightCommand, LeftCommand, LeftApple, LeftWindows, RightWindows, AltGr, Help, Print, SysReq, Break, Menu, Mouse0 to Mouse6, A through Z, Alpha0 through Alpha9, Keypad0 through Keypad9, F1 through F15, JoystickButton0 to JoystickButton19, Joystick1Button0 to Joystick8Button19_ _


