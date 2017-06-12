# 客户端

!> 请确保了解 `golang`，并且需要了解项目使用的库

项目地址：[gost-c/gost-cli](https://github.com/gost-c/gost-cli)

## 库

- [gcli](https://github.com/tcnksm/gcli) The easy way to build Golang command-line application.
- [mitchellh/cli](https://github.com/mitchellh/cli) A Go library for implementing command-line interfaces.

本项目使用 `gcli` 初始化， 框架模板为 `mitchellh/cli`, 详情请查看上面两个库的文档。

## 打包

需要将 `command/helper.go` 中的3个变量修改为自己的：

- BaseURL 你的服务端接口地址
- WebURL 你的网页端网址
- config 客户端配置文件名，可自定义
