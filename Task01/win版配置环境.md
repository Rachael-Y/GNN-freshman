（1）打开Anaconda Prompt



（2）切换到工作目录


（3）建立Pytorch Anaconda虚拟环境

conda create -n pytorch python=3.8 

（4）启动Pytorch Anaconda虚拟环境

activate pytorch

（5）安装Pytorch


conda install pytorch torchvision  cudatoolkit=11.0


本地原有pytorch
python -c "import torch; print(torch.__version__)"
1.7.0+cu110
python -c "import torch; print(torch.version.cuda)"
11.0


安装正确版本的PyG

pip install torch-scatter -f https://pytorch-geometric.com/whl/torch-1.8.0+cu111.html

pip install torch-sparse -f https://pytorch-geometric.com/whl/torch-1.8.0+cu111.html

pip install torch-cluster -f https://pytorch-geometric.com/whl/torch-1.8.0+cu111.html

pip install torch-spline-conv -f https://pytorch-geometric.com/whl/torch-1.8.0+cu111.html

pip install torch-geometric

# torch——sparse报错
去
https://pytorch-geometric.com/whl/torch-1.7.0.html
下载 torch_sparse-0.6.8+cu110-cp37-cp37m-win_amd64.whl
