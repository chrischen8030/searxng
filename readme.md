安装步骤
1. 克隆 SearXNG 仓库
```
git clone https://github.com/searxng/searxng.git
cd searxng
```

2. 安装依赖并初始化项目
```bash
make install
```

这个命令会自动：

创建虚拟环境

安装 Python 依赖

下载前端资源

生成默认配置文件（在 searxng/settings.yml）

1. 运行开发服务器

```bash
make run
```

默认会监听 http://127.0.0.1:8888，你可以直接在浏览器打开。

可用的 Makefile 命令一览
命令	说明
make install	安装所有依赖并初始化配置
make run	启动开发服务器
make clean	清除临时文件和构建缓存
make update	更新前端资源和 Python 依赖
make shell	进入 Python 虚拟环境 Shell（开发调试用）

在 settings.yml 中应包含：
yaml
```bash
search:
  formats:
    - html
    - json
    - csv
    - rss
```