#### 前言

关于郊狼与vrc联动的程序已经有很多大佬做过了，而且大佬们的程序也比较稳定，所以优先推荐大佬们的工具。

郊狼2.0用户可以参考：[Sakura0721/osc-toys: Integrates toys to VRChat using OSC. (github.com)](https://github.com/Sakura0721/osc-toys)

郊狼3.0用户可以参考：[amoeet/VRChat_X_DGLAB: 这是一个小工具，用于实现在VRChat里进行游戏互动，从而操控郊狼3.0主机输出波形。基于DG-LAB-OPENSOURCE 开源的蓝牙协议V3，使用OSC连接，获取VRChat的角色参数，用于控制郊狼3.0主机 (github.com)](https://github.com/amoeet/VRChat_X_DGLAB)

上述实现方案均基于蓝牙协议，直接与郊狼主机建立连接，没有过多转发所以延时方面应该还可以。

#### 如何部署

**环境:**

python(建议>3.10)

nodejs(请根据官方手册指导选择版本)

官方后端:[DG-LAB-OPENSOURCE/socket/BackEnd(Node) at main · DG-LAB-OPENSOURCE/DG-LAB-OPENSOURCE (github.com)](https://github.com/DG-LAB-OPENSOURCE/DG-LAB-OPENSOURCE/tree/main/socket/BackEnd(Node))

之后请使用python运行脚本，使用nodejs运行官方后端，并根据提示安装所需模块

环境齐全后请修改脚本中的**dglabA**为你的OSC参数，之后请按照如下步骤操作

**启动VRC--运行后端服务--运行该脚本--打开郊狼3.0 APP连接郊狼3.0--选择socket控制并扫描二维码**

脚本运行后会于与该脚本相同的路径内生成连接用的二维码。

app内A通道强度变为35后代表连接成功，本人只对A通道进行了处理，如果需要两个通道，请自行修改代码，连接后的强度可以与代码中修改，具体json位于**data_to_send**变量中，如何修改请参考官方socket开源文档。

**注意**：

该实现方案可能会存在延时，由于本人实力有限暂时没法处理

#### 之后的打算

由于本人设备原因前言中的方案本人无法使用，后续打算在继续等大佬们开发新工具的同时缓慢完善自己的代码。

初步打算根据官方的socket后端的例子来使用python实现socket后端从而减少一次数据转发

不过最希望的还是有大佬能开发出更好的工具

#### 相关参考

[VRChat](https://docs.vrchat.com/)

[DG-LAB-OPENSOURCE/DG-LAB-OPENSOURCE: The Bluetooth Protocol Of DG-LAB Devices (github.com)](https://github.com/DG-LAB-OPENSOURCE/DG-LAB-OPENSOURCE)

[T-Rex Runner (dungeon-lab.com)](https://www.dungeon-lab.com/t-rex-runner/index.html)









