# 贪吃蛇游戏 机器学习AI
使用神经网络训练一个可以玩贪吃蛇游戏的AI。

Python版本 Python3.6

依赖库

- pygame 1.9.5
- tensorflow

## 游戏部分说明

#### Snacky_UI.py
![游戏开始界面](https://github.com/cstrikest/ML_Snakey/blob/master/images/gamestart_image.png?raw=true)

提供了一个可以供人类游玩的贪吃蛇游戏UI。游戏素材图片比较简陋。游戏内容设有等级划分，随着获取食物的数量上升，蛇前进的速度会变快。

同时每增加一个难度会多出现一个触碰到便会游戏结束的炸弹。

游戏在一个200×200像素的平面中运行，每10×10个像素作为一个单元。 右侧有计分面板。

游戏右侧是一个100×200像素的信息面板。主要用到的信息会在右侧给出

使用WSAD控制移动方向，任何时候都可以使用Q键退出。

游戏结束画面按R重新开始，按S则会跳出计分板。

![游戏面板](https://github.com/cstrikest/ML_Snakey/blob/master/images/game_image.png?raw=true)

#### Snacky_core.py

为了给模型训练加快速度的游戏核心逻辑类。只保留游戏规则，舍弃所有UI相关，提升训练时的速度。

#### Snacky_UI_AI_interface.py

非人类玩家的游戏UI，通过AI_core_logic.py中get_next_direction()来获取下一步的方向信息。

之后还会使用通过神经网络训练出的模型进行游戏控制。

#### AI_core_logic.py

一个简单的演示用AI，完全无视炸弹与自身碰撞，只吃食物。

#### AI_core_ML.py

基于tensorflow的机械学习AI。详细内容将在后文说明。

#### AI_test.py

测试Snacky_core的小脚本。

## ML部分

...