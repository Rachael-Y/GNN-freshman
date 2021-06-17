Task01: 简单图论与环境配置


踩坑记录：
https://pytorch-geometric.com/whl/torch-1.8.0+cpu.html
此处可以下载离线.whl 安装包

注意虚拟环境


Jupyter 虚拟环境使用：
让Jupyter Notebook支持虚拟运行环境，需要在Anaconda里安装一个插件。

回到终端下面，用C-c退出目前正在运行的Jupyter Notebook Server，然后执行：

conda install nb_conda
再重新开启Jupyter Notebook：

jupyter notebook

参考链接：
1.Mac下安装PyTorch https://zhuanlan.zhihu.com/p/168748757


进入虚拟环境
source activate deeplearning

退出虚拟环境
conda deactivate

查看本机所有（由conda安装的）虚拟环境
conda list # 或者 conda info -e

删除虚拟环境
conda remove -n your_env_name(虚拟环境名称) --all

退出虚拟环境
source deactivate

2.mac 安装pyg https://blog.csdn.net/weixin_39188290/article/details/117933408?spm=1001.2014.3001.5501

部分命令：
pip install torch-scatter -f https://pytorch-geometric.com/whl/torch-1.8.0+cpu.html

pip install torch-sparse -f https://pytorch-geometric.com/whl/torch-1.8.0+cpu.html

pip install torch-cluster -f https://pytorch-geometric.com/whl/torch-1.8.0+cpu.html

pip install torch-spline-conv -f https://pytorch-geometric.com/whl/torch-1.8.0+cpu.html

