### 因mem0库发布包太慢，所以自己先打包一下最新的包

    git remote add upstream git@github.com:mem0ai/mem0.git
    git pull upstream main

### 更改打包配置

将pyproject.toml中的：

    name = "mem0ai"
    version = "0.0.15"

改成自己自定义的sdk名称和版本号。

### 打包

    make build

### 上传

    poetry config repositories.私有项目 私有库地址
    poetry publish -r 私有项目 --build
    