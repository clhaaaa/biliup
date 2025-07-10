<div align="center">
  <img src="public/logo.png" alt="description"/>
</div>

<div align="center">

[![Python](https://img.shields.io/badge/python-3.9%2B-blue)](http://www.python.org/download)
[![PyPI](https://img.shields.io/pypi/v/biliup)](https://pypi.org/project/biliup)
[![PyPI - Downloads](https://img.shields.io/pypi/dm/biliup)](https://pypi.org/project/biliup)
[![License](https://img.shields.io/github/license/biliup/biliup)](https://github.com/biliup/biliup/blob/master/LICENSE)
[![Telegram](https://img.shields.io/badge/Telegram-Group-blue.svg?logo=telegram)](https://t.me/+IkpIABHqy6U0ZTQ5)

[![GitHub Issues](https://img.shields.io/github/issues/biliup/biliup?label=Issues)](https://github.com/biliup/biliup/issues)
[![GitHub Stars](https://img.shields.io/github/stars/biliup/biliup)](https://github.com/biliup/biliup/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/biliup/biliup)](https://github.com/biliup/biliup/network)

</div>


# 📜[» 分叉笔记（内含使用指导） ](https://github.com/ZXGU183/biliup/wiki)

## 💡 功能特色
* 开箱即用，多种安装方式，提供可视化WebUI界面
* 多主播录制/上传，24h不间断无人值守运行，可高度自定义元信息
* 边录边传不落盘对等上传，节省本地硬盘空间

[「原项目」](https://github.com/biliup/biliup)——[『官方文档』](https://github.com/viondw/viondw.github.io/tree/main/docs/guide)

## 🍱 [下载即食 «](https://github.com/ZXGU183/biliup/releases)

- Windows x64 用户：直接下载`biliup-[version]_win64.exe`运行即可，无需额外准备环境，如有必要可下载`PathTool_FFmpeg-[version]`并[按需执行其中的批处理](https://github.com/ZXGU183/biliup/wiki/%E6%A8%A1%E6%9D%BF#%E8%B7%AF%E5%BE%84%E5%8F%98%E9%87%8F%E5%A4%84%E7%90%86%E6%A8%A1%E6%9D%BF)

- Docker amd64 用户：下载并导入镜像 `docker load -i biliup-[version]_amd64.tar` ，从[「**创建并运行容器**」步骤](https://github.com/viondw/viondw.github.io/blob/main/docs/guide/%E5%AE%89%E8%A3%85%E9%83%A8%E7%BD%B2/docker.md#2-%E5%88%9B%E5%BB%BA%E5%B9%B6%E8%BF%90%E8%A1%8C%E5%AE%B9%E5%99%A8)开始参考官方说明，**注意我们的镜像名称标签是`biliup:local`**

- 其他架构平台和操作系统：下载pip包并执行本地安装，详可参见[Wiki中的“使用准备”篇](https://github.com/ZXGU183/biliup/wiki/%E4%BD%BF%E7%94%A8%E5%87%86%E5%A4%87)

## 🚀 从构建使用

- 仔细阅读 [Wiki](https://github.com/ZXGU183/biliup/wiki) 和[读我文件](https://github.com/ZXGU183/biliup/blob/master/README.md)，**尤其是对[后续更新](https://github.com/ZXGU183/biliup?tab=readme-ov-file#%EF%B8%8F-%E5%90%8E%E7%BB%AD%E6%9B%B4%E6%96%B0)的提示**
- [安装](https://zhuanlan.zhihu.com/p/662421567)  [**FFmpeg**](https://ffmpeg.org/) ，**推荐**[最新构建（即 master）的 gpl-shared 版本](https://github.com/BtbN/FFmpeg-Builds/releases)
0. `git clone https://github.com/ZXGU183/biliup && cd biliup`

### Windows
1. 确保 Python 版本 ≥ 3.9 （推荐3.11~3.12，过高或过低可能需要手搓依赖工具链）， Node.js 版本 ≥ 18
2. 安装后端依赖 `pip install .`
3. 安装前端依赖 `npm i`
4. 构建前端静态资源 `npm run build`
5. 启动 `BiliUPstart.bat` 或 `python -m biliup`
6. 访问 WebUI：`http://你的网络或本地IP:19159`

### Linux 或 macOS
1. 存在 Python 版本 ≥ 3.9 （推荐3.11~3.12，过高或过低可能需要手搓依赖工具链）， Node.js 版本 ≥ 18
2. 安装后端依赖 `pip3 install .`
3. 安装前端依赖 `npm i`
4. 构建前端静态资源 `npm run build`
5. 启动：`python3 -m biliup`
6. 访问 WebUI：`http://你的网络或本地IP:19159`

### Docker
- 按需修改 Docker 配置和 `DockerfileLocal` 中的文件内容（根据网络环境换源、调整链接加速等）
- `docker build -t 你想定义的镜像名:自定义标签名 . -f DockerfileLocal`
- 从[「**创建并运行容器**」步骤](https://github.com/viondw/viondw.github.io/blob/main/docs/guide/%E5%AE%89%E8%A3%85%E9%83%A8%E7%BD%B2/docker.md#2-%E5%88%9B%E5%BB%BA%E5%B9%B6%E8%BF%90%E8%A1%8C%E5%AE%B9%E5%99%A8)开始参考官方说明，**注意此处的镜像名称标签由你定义**

## 🛠️ 后续更新
1. 移走保存在程序目录下的录播
2. **备份** `/biliup/data/` 以及自定义预设等文件
3. `git pull`
4. 按需再次执行安装构建步骤
5. 若无特殊情况，根据需要还原之前备份的文件即可

---

## 🧑‍💻开发

### 前端

1. 启动开发服务器：`npm run dev`
2. 访问：`http://localhost:3000`

### 后端

确保 `/biliup/web/public` 目录存在构建好的前端静态资源

## 🤝其他💴
* 同原项目，请参照
* 感谢所有的BiliUP贡献者

## ⭐Stars

<a href="https://www.star-history.com/#ZXGU183/biliup&Date">
 <picture>
   <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=ZXGU183/biliup&type=Date&theme=dark" />
   <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=ZXGU183/biliup&type=Date" />
   <img alt="Star History Chart" src="https://api.star-history.com/svg?repos=ZXGU183/biliup&type=Date" />
 </picture>
</a>
