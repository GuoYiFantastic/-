# 轻松玩转书生·浦语大模型趣味Demo

**pip换源设置默认镜像源**
```
python -m pip install --upgrade pip
pip config set global.index-url https://mirrors.cernet.edu.cn/pypi/web/simple
```

**conda快速换源**

```
cat <<'EOF' > ~/.condarc
channels:
 - defaults
show_channel urls: true
default channels:
 - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main
 - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/r
 - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/msys2
custom channels:
 conda-forge: https://mirrors,tuna,tsinghua.edu.cn/anaconda/cloud
 pytorch: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
EOF
```

**模型下载**

Hugging Face 下载使用 Hugging Face 官方提供的huggingface-cli 命令行工具。
安装依赖:
```
pip install -U huggingface_hub
huggingface-cli download --resume-download internlm/internlm-chat-7b --local-dir your_path
```

OpenXLab 可以通过指定模型仓库的地址，以及需要下载的文件的名称，文件所需下载的位置等，直接下载模型权重文件。使用 Python 脚本下载模型首先要安装依赖安装代码如下: pipinstall -U openxlab 安装完成后使用 download 函数导入模型中心的模型将以下代码写入 Python 文件，运行即可
```
from openxlab.model import download
download(model_repo='OpenLMLab/InternlM-7b', model name='InternLM-7b', output='your local path')
```

使用 modelscope 中的 snapshot download 函数下载模型，第一个参数为模型名称，参数cache dir 为模型的下载路径。首先安装依赖:
```
pip installmodelscope
pip install transformers
```
在当前目录下新建python 文件，填入以下代码，运行即可
```
import torch
from modelscope import snapshot_download, AutoModel AutoTokenizer
import os
model dir = snapshot download('Shanghai AI laboratory/internlm-chat-7b', cache dir='your path', revision='master')
```

## 大模型以及InternLM框架介绍

## InternLM-Chat-7B智能对话Demo
![1705041141198](https://github.com/GuoYiFantastic/InternLM_training_camp/assets/130634988/3ba81735-40c0-42be-833b-f6f49a0ade23)

## Lagent智能体工具调用Demo
![1705068147521](https://github.com/GuoYiFantastic/InternLM_training_camp/assets/130634988/60dff1aa-11b9-4e9a-a49a-dc5a0470505d)
![1705068396908](https://github.com/GuoYiFantastic/InternLM_training_camp/assets/130634988/99b27c0b-4ede-4cfa-9749-d9ec3def638e)


## 浦语·灵笔的图文理解及创作
需要A100（1/4）*2
![image](https://github.com/GuoYiFantastic/InternLM_training_camp/assets/130634988/ab0ca60e-4c83-48cc-82d4-6cb876e61977)

## InternalLM-Xcomposer介绍

