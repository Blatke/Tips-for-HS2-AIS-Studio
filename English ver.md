#Tips on HS2 and AI Girl Studio


**Bl@ke/Wen**


（[http://www.blatke.cc](http://www.blatke.cc/)）


Honey Select 2- hereinafter referred to as HS2; 


AI Shojo, AI Girl or AI Girl - hereinafter referred to as AI; 


In addition to the default graphics mode, Studio Studio also has two other graphics modes provided by third-party plugins: DHH and Graphics, which can be switched on the startup interface (InitSetting. exe). 


##Plugin directory

HS2：[https://github.com/ManlyMarco/HS2-HF_Patch/blob/master/Plugin%20Readme.md](https://github.com/ManlyMarco/HS2-HF_Patch/blob/master/Plugin%20Readme.md)


AI：[https://github.com/ManlyMarco/AI-HF_Patch/blob/master/Plugin%20Readme.md](https://github.com/ManlyMarco/AI-HF_Patch/blob/master/Plugin%20Readme.md) 

##Where can I find Mods?

The mods for HS2 and AI are basically universal. 


### Discord

[https://discord.gg/illusionsoft](https://discord.gg/illusionsoft)


This is the Discord server for the folk I Society game, where you can search for mods on the hs2 mod sharing and old-hs2-mod sharing channels. 


### Betterrepack Mods Server

[https://sideload.betterrepack.com/download/AISHS2/](https://sideload.betterrepack.com/download/AISHS2/) 


This list regularly compiles and updates mods from Discord above, but my personal suggestion is to look for them on Discord because when the author publishes mods, they also write some usage instructions on Discord posts, and this list only includes mod files without accompanying instructions. 


It is also recommended to make good use of Google to search for the website, such as adding site: sidiload.betterrepack.com after the search keyword

##How does the body reflect light

Select the character, open the Material Editor, and search for "body" or "body". 


Find the following under this material: 


-Glossiness, controlling the effect of material reflection of light sources; 

-Metallic texture controls the contrast between highlights and non highlights when the material reflects light sources. Non highlights reflect the surrounding environment. 


Adjusting the above two values appropriately, my general gloss is 0.8 and metal is 0.75. 


When the metal value increases, you may find that the human body becomes darker. This is because the surrounding environment is dark or there are no reflection probes, so the human body cannot reflect even if it wants to. 


The solution is to add a Reflection Probe, which is a studio item that players who integrate packages may find directly in the studio item search. Not installed, can be downloaded here:[https://drive.google.com/file/d/1B7cn4FXdYTGE4W96rVcL5jmbHJ3JOjnq/view](https://drive.google.com/file/d/1B7cn4FXdYTGE4W96rVcL5jmbHJ3JOjnq/view) 


After adding, this item takes a panoramic screenshot with itself as the center, and attaches the screenshot to items with high gloss and metallic values in the scene, achieving a smooth reflection or even mirror reflection effect. 


Both DHH and Graphics modes support its functionality, but Graphics has better support. 


![K2SF@FMNODG%~{PM5(XTJH9](https://github.com/user-attachments/assets/ccda59fd-eb64-4cab-b86a-a30a8fb22462)


This is the addition of a skybox as the background in the studio, a plain spherical sphere, and finally a Reflection Probe. 


![_ZX}YQSPQ@DIR5KDJJCOQF](https://github.com/user-attachments/assets/6e7ebace-4715-4a45-89df-8f89f9e71d1e)


In DHH mode, fully fill the metal and luster of the sphere, and fully fill the "texture metal reflection" in the DHH interface to achieve the effect shown in the picture. Note: The content reflected by the Reflection Probe in DHH is only the environment at the moment it is added to the scene and does not change in real-time. You can delete and then add again to refresh the reflected content. 


![R0QF@{LYHHOHTD @7TGXLG](https://github.com/user-attachments/assets/446035a2-d443-4012-b305-b9d2b3c35d61)


In Graphics mode, select Reflection Probes, fully increase the importance of Reflection Probes, and adjust the intensity appropriately to achieve the above effect. You can also check "Real time Reflection Probe" in the Settings to adjust the reflection content according to the scene changes. 


Please note that regardless of the mode, the content reflected by the Reflection Probe is related to its location. 

##Export character as FBX file

**Grey. MeshExporter * * is a character export plugin designed for Illusion games, which can export characters (including their clothes and accessories) from Lovelife, HS, HS2, AI Girls, and PH studios as FBX model files and related textures, making it easier for users to import and edit them into 3D modeling software. 


Discord original author message:[https://discord.com/channels/446784086539763712/715932300382044170/858707187203309629](https://discord.com/channels/446784086539763712/715932300382044170/858707187203309629)


Baidu Cloud Download Address

Link:[https://pan.baidu.com/s/18YqOwisEjaWXN-WxiMUaEw?pwd=2024](https://pan.baidu.com/s/18YqOwisEjaWXN-WxiMUaEw?pwd=2024)

Extraction code: 2024


After downloading, unzip and find the folder with the corresponding name according to your game. Drag the BepInEx folder into your game root directory to complete the installation. 


After installation, start the game's Studio mode. Add any character and make sure to select it in the workspace of the workspace. Press the minus key on the keypad to call GreyOn the MeshExporter control panel, press the Export button to export the character model and related textures to the Export folder in the game root directory. 


If you have any other questions, you can read the READ ME - Seriously included in the folder of the pluginTxt help document. 


### Grey. MeshExporter Shortcut Key Settings

If there is no response when pressing the minus key, you need to try modifying GreyUse the ini/cfg file of MeshExporter to reset shortcut keys. 


1. Ensure that Grey is installedAfter MeshExporter, start StudioNeo at least once, so that the corresponding folder will generate setting files as StudioNeo starts. 


2. When StudioNeo is turned off, find this settings file. There are two possibilities here: 


This file is located in: your game root directory/BepInEx/Config/directory; The file name is usually GreyMeshExporter. Game name. cfg. For example, I am using an AI girl with the file name GreyMeshExporter.AI.cfg。As shown in the following figure: 


![image](https://github.com/user-attachments/assets/e3b2d3ad-dd49-43df-a303-3a6ca2b59d9d)


Game root directory/BepInEx/Config/GreyMeshExporter. Game name.cfg

Alternatively, the file can be located in: your game root directory/UserData/directory; The file name is usually ModPrefs.ini. 


3. Open this file with Notepad or code editing software, find the lines of code that start with the words EportKey=or ExportShortcut=, and use shortcut key keywords (see comments at the end of the text) to change the code after the equal sign to the shortcut key name you want to reset. For example, I changed it to LeftShift+Minus here, which means calling up the plugin panel by pressing the left Shift+minus key (note: the key order may also be reversed, that is, pressing the minus key first, then pressing the left Shift key. Anyway, try it all). As shown in the following figure: 


![image](https://github.com/user-attachments/assets/6f4a8967-28bb-4bf5-8dd5-ee1dea90575c)


4. Save the file. Start StudioNeo. Press the shortcut key you set to call up the plugin panel. 


![image](https://github.com/user-attachments/assets/01399f27-88b9-4ad9-b670-dcf9fd437cb1)


According to the READ ME - Seriously! Included with the pluginThe keywords that can be used for shortcut keys in a txt file are as follows: 


_ _None, Backspace, Tab, Clear, Return, Pause, Escape, Space, Exclaim, DoubleQuote, Hash, Dollar, Ampersand, Quote, LeftParen, RightParen, Asterisk, Plus, Comma, Minus, Period, Slash, Colon, Semicolon, Less, Equals, Greater, Question, At, LeftBracket, Backslash, RightBracket, Caret, Underscore, BackQuote, Delete, KeypadPeriod, KeypadDivide, KeypadMultiply, KeypadMinus, KeypadPlus, KeypadEnter, KeypadEquals, UpArrow, DownArrow, RightArrow, LeftArrow, Insert, Home, End, PageUp, PageDown, Numlock, CapsLock, ScrollLock, RightShift, LeftShift, RightControl, LeftControl, RightAlt, LeftAlt, RightApple, RightCommand, LeftCommand, LeftApple, LeftWindows, RightWindows, AltGr, Help, Print, SysReq, Break, Menu, Mouse0 to Mouse6, A through Z, Alpha0 through Alpha9, Keypad0 through Keypad9, F1 through F15, JoystickButton0 to JoystickButton19, Joystick1Button0 to Joystick8Button19_ _


###Take GreyModel files exported by MeshExporter, imported into Blender

You can use Blender auxiliary tools such as * * hs2/blender-export * * to convert GreyThe FBX and other files (as well as textures) generated by MeshExporter are imported into Blender at once. Refer to:[https://github.com/veryfancypants/hs2_blender_export](https://github.com/veryfancypants/hs2_blender_export)


be careful: 

1. After exporting the character in the studio, put it back in a T-shaped pose, call up the Runtime Unity Editor plugin interface (press F1 to set its shortcut key), find "Common Space" in the list of the "Scene Unity Editor" panel, select it, and click "dump". Subsequently, a. txt document opened with Notepad popped up, which recorded the skeletal and other data of the character. Open the subfolders where you previously imported the character into the Export folder (e.g. \ Export \ 20221213104852_Kazumi \), and then save this document to that folder. 

2. When using hs_2blenderexport, it is necessary to open its prefabmaterials_ceshexporter.blend file and perform various operations in this file, rather than operating in a newly created blank blend file or adding the py file in its folder as an add-on to the Blender plugin panel. 

3. Enter prefaf_materials_ceshexporter.blend, press the N key to call up the plugin bar on the right, and click on the rig. 


![image](https://github.com/user-attachments/assets/1414ba9e-61ed-4612-b137-74b1b3b8c2f7)


4. Click<New>in the Preset section to create a new preset. Copy and paste the * * full path * * of the folder containing the. txt document we mentioned earlier (e.g. C: \ HS2 \ Export \ 20221213104852_Kazumi \) into the Char directory text box. Finally, click on import model to complete the model import. 


![image](https://github.com/user-attachments/assets/3b783218-7e71-4ede-aafa-2b1573b1603d)