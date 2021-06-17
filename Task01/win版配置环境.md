（1）打开Anaconda Prompt



（2）切换到工作目录


（3）建立Pytorch Anaconda虚拟环境

conda create -n pytorch python=3.8 anaconda

（4）启动Pytorch Anaconda虚拟环境

activate pytorch
（5）安装Pytorch


conda install pytorch torchvision torchaudio cudatoolkit=11.1 -c pytorch -c nvidia
