在虚拟环境中安装jupyter

通过下面命令安装插件：

conda install nb_conda

错误1：EnvironmentLocationNotFound: Not a conda environment
打开jupyter后点击Conda会弹出这样的错误：


解决方法：

找到Anaconda安装路径下nb_conda库的envmanager.py文件

win系统在目录：Anaconda3\Lib\site-packages\nb_conda\envmanager.py

linux系统在目录：Anaconda3/pkgs/nb_conda-2.2.1-py36_0/lib/python3.6/site-packages/nb_conda/envmanager.py

找到该文件后在83~86行有这样一段代码：

return {
            "environments": [root_env] + [get_info(env)
                                          for env in info['envs']]
        }
我们将此段代码改成如下：

return {
            "environments": [root_env] + [get_info(env) for env in info['envs'] if env != root_env['dir']]
        }
然后重启jupyter就可以了。


1、conda更新
conda的更新方法：

conda update -n base conda -c conda-forge


2、安装nbextensions插件，给jupyter添加目录

pip install jupyter_contrib_nbextensions
jupyter contrib nbextension install --user --skip-running-check

注意配置的时候要确保没有打开 Jupyter Notebook，然后重启jupyter即可看到nbextensions选项卡。


点开 Nbextensions 的选项，并勾选 Table of Contents


安装tensorflow：
CPU版本安装：pip install --ignore-installed --upgrade tensorflow==2.4.0
GPU版本安装：pip install --ignore-installed --upgrade tensorflow-gpu==2.4.0

https://blog.csdn.net/XunCiy/article/details/89069562

版本参考：

https://tensorflow.google.cn/install/source_windows


链接参考：
https://blog.csdn.net/W_hm_M/article/details/107366442?utm_medium=distribute.pc_relevant.none-task-blog-baidujs_baidulandingword-1&spm=1001.2101.3001.4242

重点参考cuda安装部分

https://sophia-fez.blog.csdn.net/article/details/89070315

https://www.huaweicloud.com/articles/19faa544bda51633cc71cce987faa295.html

https://zhuanlan.zhihu.com/p/139776843

Anaconda中配置Tensorflow环境：

https://blog.csdn.net/XunCiy/article/details/89069193

https://blog.csdn.net/XunCiy/article/details/89016510
