## 1 Ledock的安装
![[Pasted image 20251128211044.png]]
得到一个Ledock.win32.zip文件（这个Ledock就很小巧，不用那种加载式的安装，仅仅下载后解压就能用了）
![[Pasted image 20251128211352.png]]

![[Pasted image 20251128211522.png]]
就这样一个小巧的界面，可以进行一个盲性的分子对接  
（盲性对接：不人为设定对接的活性位置去对接）

![[Pasted image 20251128212419.png]]


*注：Ledock也可以去使用软件指令去操作分子对接，包括设置活性位置去做活性对接。在此主要为了让你有一个对分子对接的步骤认识，仅介绍Ledock提供的界面。指令式操作使用autodock vina来讲解*

## 2 PyMol的安装
参考帖子：
[入门教程 — PyMOL中文教程 2022.09 文档](http://pymol.chenzhaoqiang.com/intro/startManual.html)
[PyMOL初级教程——2.PyMOL软件安装_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1Av411572j/?spm_id_from=333.788.recommend_more_video.-1&trackid=web_related_0.router-related-2206419-7v86w.1763635440732.251&vd_source=d12751ffe8ab8667758565f5d2fe2f66)
我们这里安装的是PyMol的开源版本（这个版本更新少，但是免费且操作简便，更流畅，教程多）
[GitHub - cgohlke/pymol-open-source-wheels: Pymol-open-source wheels for Python on Windows.](https://github.com/cgohlke/pymol-open-source-wheels)
[(2 封私信) 分子模拟||Pymol开源版安装步骤及教程 - 知乎](https://zhuanlan.zhihu.com/p/445485729)


***上面的安装流程都不如我的简单***

### 1、下载Miniconda
conda是一个管理虚拟环境的软件，就理解成，一个下载软件的软件就行了，应用商店（差不多）
Miniconda是anaconda的占内存小的版本，这里用来下载开源版pymol非常合适

[Free Download | Anaconda](https://www.anaconda.com/download)
![[Pasted image 20251128224128.png]]

一直点下去，记住路径方便找
![[Pasted image 20251128224207.png]]
记不住路径也没关系，可以直接搜到
![[Pasted image 20251128224339.png]]
打开后是这样的
![[Pasted image 20251128224404.png]]
### 2、下载开源版Pymol
[Releases · cgohlke/pymol-open-source-wheels · GitHub](https://github.com/cgohlke/pymol-open-source-wheels/releases)
![[Pasted image 20251128224514.png]]
复制下下载的文件的路径
![[Pasted image 20251128224648.png]]

输入下面的代码（注：这里的#，不能被conda识别或者忽略，就一行的粘贴进去运行）
``` 
#创建环境
conda create -n pymol_evn python=3.11 -y
#激活并安装
conda activate pymol_evn
conda install numpy pyqt pillow -y
pip install "C:\Users\ansg2\Downloads\pymol-3.2.0a0-cp311-cp311-win_amd64.whl"
#这里替换成刚刚复制的自己下载文件的路径
#测试
pymol
```
然后我们为了下次方便打开到虚拟环境的路径'pymol_evn'的文件夹
找到这个文件，建一个快捷方式
大概在这个位置
‘C:\Users\ansg2\\.conda\envs\pymol_evn\Scripts'
C盘，使用者，用户名，.conda的储存位置，构建的各个环境的储存位置，刚构建的pymol_evn虚拟环境，Scripts就是这个pymol.exe文件存在的地方，为其构建一个快捷方式，放到桌面。
![[Pasted image 20251128225425.png]]

![[Pasted image 20251128225743.png]]
开源版pymol的界面
![[Pasted image 20251128225808.png]]
（zky说开源版比他们赚钱的版本好用）