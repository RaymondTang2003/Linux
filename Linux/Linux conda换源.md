# windows下

转载自：[https://blog.csdn.net/dream_allday/article/details/80344511](https://blog.csdn.net/dream_allday/article/details/80344511)

在清华源和中科大源之间自行选择

## 1 添加清华源

[命令行](https://so.csdn.net/so/search?q=%E5%91%BD%E4%BB%A4%E8%A1%8C&spm=1001.2101.3001.7020)中直接使用以下命令

```crystal
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/conda-forge conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/msys2/ 
# 设置搜索时显示通道地址conda config --set show_channel_urls yes
```

注意如果需要**pytorch**, 还需要添加pytorch的镜像

```crystal
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/pytorch/
```

## 2 添加中科大源

```crystal
conda config --add channels https://mirrors.ustc.edu.cn/anaconda/pkgs/main/conda config --add channels https://mirrors.ustc.edu.cn/anaconda/pkgs/free/conda config --add channels https://mirrors.ustc.edu.cn/anaconda/cloud/conda-forge/conda config --add channels https://mirrors.ustc.edu.cn/anaconda/cloud/msys2/conda config --add channels https://mirrors.ustc.edu.cn/anaconda/cloud/bioconda/conda config --add channels https://mirrors.ustc.edu.cn/anaconda/cloud/menpo/conda config --set show_channel_urls yes
```

# Linux下

将以上配置文件写在`~/.condarc`中  
`vim ~/.condarc`

```crystal
channels:  - https://mirrors.ustc.edu.cn/anaconda/pkgs/main/  - https://mirrors.ustc.edu.cn/anaconda/cloud/conda-forge/  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/  - defaultsshow_channel_urls: true
```