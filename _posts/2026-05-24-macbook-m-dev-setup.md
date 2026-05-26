---
layout:     post
title:      "MacBook M系列芯片配置开发环境实战总结"
subtitle:   "Homebrew + Python + Node.js + Go 一次搞定"
date:       2026-05-24
author:     "JACK ZHANG"
header-img: "img/home-bg.jpg"
catalog: true
tags:
    - MacBook
    - 开发环境
    - Homebrew
---

换了 M 芯片的 MacBook 之后，原来的开发环境不能直接用了，重新配置一遍，顺便记录下来，供以后参考。

## 统一用 Homebrew 管理

Homebrew 已经原生支持 Apple Silicon，只需要一条命令：

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

## 安装编程语言

### Python（pyenv 管理多版本）

```bash
brew install pyenv
echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.zshrc
echo 'command -v pyenv > /dev/null || export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.zshrc
eval "$(pyenv init -)"
pyenv install 3.11.0
pyenv global 3.11.0
```

### Node.js（fnm 比 nvm 快 20倍）

```bash
brew install fnm
echo 'eval "$(fnm env --use-on-cd)"' >> ~/.zshrc
fnm install 20
fnm default 20
```

### Go

```bash
brew install go
go version
```

## 常用工具

```bash
brew install git gh wget curl htop
```

M 芯片的 Mac 开发体验其实很好，性能强，发热少，续航持久。推荐！
