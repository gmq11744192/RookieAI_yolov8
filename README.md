# RookieAI_yolov8   日志  
## 使用方法：  
为维护环境作者不提供直接打包成型的软件，但我开源代码鼓励自学。  

### 针对开发者：
1. #### 使用以下代码获取本代码需要的包：  
`pip install -r requirements.txt`   
2. #### 你还需要一个自己的模型（目前只支持.pt模型），如果没有可暂时使用ultralytics官方模型。  
**当未找到模型时会自动下载YOLOv8n模型，你也可以 ⬇️**  
_访问[YOLOv8 GitHub界面](https://docs.ultralytics.com/)获取更多官方yolov8模型以快速开始  
访问[ultralytics官网](https://docs.ultralytics.com/)查看官方网站帮助文档_  
3. #### 使用你的模型  
打开软件---选择模型文件---保存设置---点击左下角关闭软件，重启软件。  
即可加载上选择的模型文件  
或者：  
修改默认文件地址：  
`# 默认的模型文件地址`  
`default_model_file = "yolov8n.pt"`

1. #### 使用以下代码获取本代码需要的包：  
`pip install -r requirements.txt` 
2. #### 下载pyinstaller包
`pip install pyinstaller`
3. #### 使用pyinstaller打包代码
`pyinstaller xxxxx.py`  
将xxxxx替换为代码实际名称。  
更多打包参数介绍：[Python pyinstaller打包exe最完整教程](https://blog.csdn.net/qq_48979387/article/details/132359366)  
4. #### 文件整理
将  
'_internal'(包含软件环境)  
'Apex_logo.png'（软件背景图片）  
'程序.exe'（主程序）  
'settings.json'(参数保存)  
'模型文件.pt'（模型文件）  
放在同一目录下，直接运行exe文件即可。


❗❗❗注意❗❗❗  
目前只能通过红色按钮关闭程序，右上角的x无法完全结束程序！！！！！



更新日志：
 -------------------------------------------------------------  
 4/1/2024更新：  
 ✨改进：自瞄偏差。（之前只使用固定像素偏移达到垂直瞄准位置的效果，没有考虑敌人的远近距造成的影响， 近距离偏移过低，远距离偏移过高。
 现改为计算目标中心点到上边框的距离乘以用户设置倍数的方式使远近距离偏移量都能在合适位置）。   
 🛠️优化：优化代码量，去除暂时未启用功能代码，加入更多批注方便阅读。
 ➖移除：暂时移除压枪功能，测试不出意外中断原因，考虑独立出来。  
 🕳️未来计划：1.支持其他格式文件，例如ONNX。2.独立出"侧键触发"开关。  
 -------------------------------------------------------------  
 3/19/2024更新：  
 ➕新增：自定义压枪（经常失灵，就当没有，后面修）  
 ➕新增：新增侧键鼠标下侧键触发,贴脸腰射好用。（需选择"shift+按下"触发方式）  
 🎛️测试：经测试，支持最新YOLOv9,YOLOv5,YOLOv8。可自行训练YOLO模型并使用  
 📑创建：添加鼠标压枪参数文件,可自行调整。（只能垂直压枪，分为三段，可自己改更多段。有BUG用着用着压枪就没了...）  
 🕳️未来计划：1.支持其他格式文件，例如ONNX。2.独立出"侧键触发"开关。  
 -------------------------------------------------------------
 2/27/2024更新：  
 ➕新增：自定义微调自瞄位置（自瞄偏差）  
 ➕新增：可手动选择模型文件，应用范围更广   
 ✨改进：半透明UI界面  
 ✨改进：调参页面置顶  
 ❗注意：配置文件内容已更改，需替换为最新版
 -------------------------------------------------------------
 2/4/2024更新：  
 🛠️修复：文件无法手动选择，进程冲突导致的参数调整面板失效  
 📑创建：创建更新日志，从此开始记录每次的更新内容  
 -------------------------------------------------------------  
 2/25/2024更新：  
 📢立项：基于yolov8的FPS游戏自瞄软件  
 🤖更新：实现基本的自瞄功能等。
 -------------------------------------------------------------
 1/28/2024发布：  
 👼初次创建基于yolov8实现本地视频预处理项目
 -------------------------------------------------------------
