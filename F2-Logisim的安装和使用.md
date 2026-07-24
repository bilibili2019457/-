# F2 Logisim的安装和使用

## 1.下载和安装

>推荐使用国内的百度网盘地址 ： 
>
>```text
>链接: https://pan.baidu.com/s/19yEaTn2saNsXxEhqjFqSLw?pwd=ju56
>提取码: ju56
>```

<img src="https://gitee.com/alps-chenyu/typora/raw/master/image/image-20260714215730659.png" alt="Logisim界面" style="zoom: 50%;" />

## 2.切换Logisim为中文界面

<img src="https://gitee.com/alps-chenyu/typora/raw/master/image/image-20260714215855747.png" alt="中文界面" style="zoom:50%;" />

## 3.  根据 Logisim 教程 创建第一个逻辑电路

### 第0步 ：整体概论

>当您启动 Logisim-evolution时，您将看到类似于以下内容的窗口。

<img src="https://gitee.com/alps-chenyu/typora/raw/master/image/image-20260714220657239.png" alt="Logisim界面" style="zoom:50%;" />

### 第1步 :  添加门 + 第2步 ：添加导线      

![画图](https://gitee.com/alps-chenyu/typora/raw/master/image/image-20260714221122256.png)

### 第3步 ： 添加文本

![异或](https://gitee.com/alps-chenyu/typora/raw/master/image/image-20260714221351955.png)

### 第4步 ： 测试电路

![选择poke](https://gitee.com/alps-chenyu/typora/raw/master/image/image-20260714221502113.png)

![测试电路](https://gitee.com/alps-chenyu/typora/raw/master/image/image-20260714222011781.png)

|  A   |  B   |  Y   |
| :--: | :--: | :--: |
|  0   |  0   |  0   |
|  0   |  1   |  1   |
|  1   |  0   |  1   |
|  1   |  1   |  0   |

>Tips ： 异或门的逻辑大致可以归纳为相同为0， 相异为1

### 第5步 ： 单步测试

#### **1. 为什么要用“单步模式”？**

在现实中，信号通过逻辑门需要时间（传播延迟）。虽然 Logisim 简化了模型（所有门延迟相同），但依然会出现“竞争冒险”现象。单步模式能让你像看慢动作回放一样，一步步观察信号是怎么在门电路里“跑”的，从而发现某些瞬间的错误脉冲。

#### **2. 具体操作步骤（跟着做）**

>**准备状态**：先把电路中的输入 `e` 设为 `0`。
>
>**暂停模拟**：按 **Ctrl+E**，这会关闭自动仿真，让电路“冻结”在当前状态。
>
>**触发变化**：把输入 `e` 从 `0` 切换到 `1`。因为模拟暂停了，屏幕上看起来没有任何反应（这是正常的）。
>
>**单步执行**：多次按组合键 **Ctrl+I**（菜单栏 `Simulate` 下的“单步”功能）。每按一次，电路就向前推进一个“时间单位”。

#### **3. 你会观察到什么？**

>某些元件的输出端会出现**蓝色圆圈**，这表示“**在这一步，这个元件的输出值刚刚发生了改变**”。
>
>你会看到**与门（AND gate）**的输出端短暂地出现了一个 `1`（高电平），但很快又变回 `0`。
>
>**重点来了**：这个短暂的 `1` 就是**毛刺**。理论上输入 `e` 变化后，触发器（D flip-flop）不该被干扰，但因为信号到达与门两个输入端的“时间有先后”，导致与门误输出了一个短暂的“1”脉冲，这个脉冲可能会错误地触发 D 触发器。

#### **4. 这个功能的实际用途**

>除了观察这个简单的毛刺，这种方法也常用于调试**异步计数器**（可能出现乱序）或**加法器**（观察进位信号是如何像多米诺骨牌一样逐级传递的）。

## 探索Logisim的图形界面

![image-20260715120648604](./F2-Logisim%E7%9A%84%E5%AE%89%E8%A3%85%E5%92%8C%E4%BD%BF%E7%94%A8.assets/image-20260715120648604.png)
