# Github 相关操作

根据“一生一芯”的讲义，获取框架代码主要分为两步：先在GitHub上配置SSH密钥，然后通过`git clone`命令克隆代码仓库。

>什么是SSH协议?
>

### 📝 操作步骤

1.  **在GitHub上添加SSH Key**
    这是为了让你能用SSH协议安全地连接GitHub，从而拉取代码。
    
    *   **生成SSH密钥**：在终端中输入以下命令（请将邮箱换成你的GitHub注册邮箱）：
        ```bash
        ssh-keygen -t ed25519 -C "your_email@example.com"
        ```
        之后一路按回车，使用默认设置即可。密钥会生成在`~/.ssh/`目录下。
    *   **复制公钥**：用以下命令显示公钥内容并复制：
        ```bash
        cat ~/.ssh/id_ed25519.pub
        ```
    *   **添加到GitHub**：
        1.  登录GitHub，点击右上角头像，进入 **Settings**。
        2.  在左侧菜单找到 **SSH and GPG keys** 并点击。
        3.  点击绿色的 **New SSH key** 按钮。
        4.  在"Title"处为钥匙起个名（如"My PC"），在"Key"处粘贴刚刚复制的公钥，最后点击 **Add SSH key**。
    
2.  **获取框架代码**
    *   **克隆仓库**：配置好SSH Key后，在终端中执行以下命令：
        ```bash
        git clone -b ysyx2204 git@github.com:OSCPU/ysyx-workbench.git
        ```
        > **注意**：命令中的分支是`ysyx2204`，请以你查阅的最新官方讲义为准。

### ⚠️ 克隆后的重要事项

代码下载成功后，有几点需要注意：

* **项目目录**：请将克隆下来的`ysyx-workbench`文件夹，当作“一生一芯”讲义中提到的项目目录（即PA讲义里的`ics2022`）。

* **修改个人信息**：根据讲义，你需要修改`ysyx-workbench/Makefile`中的学号和姓名。讲义提到，学号可以先不修改，等完成预学习后再处理。

* **环境配置**：进入`ysyx-workbench`目录后，通常还需要运行初始化脚本（如`bash init.sh nemu`等）来拉取子项目和配置环境变量。请务必仔细阅读“一生一芯”官方讲义的后续步骤。

* **回归PA讲义**：完成上述所有操作后，就可以回到PA讲义的相应位置继续学习了。

  # Linux 系统安装

  >本文档借鉴了 迅为电子的Linux入门教程， 这是一本非常好的学习文档。
  >
  >我的观点是，实际上使用物理主机的Linux环境，实际上对于学生党来说，是十分不方便的。我参考的是北京迅为电子采用的方案 - 即windows虚拟机 + Tabby 方案。 由于我没有做过一生一芯项目。所以我想，就不采用wsl方案了。

## 下载VM

本人使用的是 VMware-workstation Pro 17.5 虚拟机环境。

搭建虚拟机环境有一个非常重要的常识 ：越新的虚拟机版本，实际运行地越流畅。

## 下载 ubantu iso

>你可以很容易的在官网上找到ubantu镜像，但是不幸的是，这玩意儿的服务器在国外。 下载速度贼慢，完美还是用国内的镜像网站吧。镜像网站地址 ：https://mirrors.tuna.tsinghua.edu.cn/ubuntu-releases/22.04/

## 在虚拟机安装Ubantu系统

 [ubuntu-22.04.5-desktop-amd64.iso](..\..\..\Downloads\ubuntu-22.04.5-desktop-amd64.iso)  这里为了稳定性选择ubantu22.4的版本

然后更着教程进行安装即可 ： https://www.bilibili.com/video/BV1Ff421X719?spm_id_from=333.788.videopod.sections&vd_source=8d902b1f75a3ffcba03abe99895c1cd3&p=6

## 对Ubantu系统的软件进行更新

# Tabby 软件扩展

>

# 后续需要完成的任务

![image-20260723184316139](./Linux%E7%B3%BB%E7%BB%9F%E5%AE%89%E8%A3%85%E5%92%8C%E5%9F%BA%E6%9C%AC%E4%BD%BF%E7%94%A8.assets/image-20260723184316139.png)

链接 ：https://missing-semester-cn.github.io/

# [MIT]计算机科学课堂中学不到的知识 The Missing Semester of Your CS Education(2020)

## 课程内容