# 安装

使用者只需要 `gost-cli` 即可使用。

## 下载安装（推荐）

##### 1. 下载

下载适合自己操作系统的 [gost-cli](https://github.com/gost-c/gost-cli/releases)

##### 2. 放在系统 `PATH` 目录中

- windows:

在C盘根目录创建 `bin` 文件夹， 然后将 `bin` 加入系统环境变量 `PATH` 中。环境变量设置方法请自行搜索。

- *nix：

```bash
# 进入文件下载目录
$ mv gost-osx gost # rename, filename is gost-linux when plateform is linux
$ chmod +x gost # make it executable
$ mv gost /usr/local/bin/gost # move to PATH folder
```

##### 3. 验证是否成功

```bash
$ gost -v
# gost-cli version 0.1.0 ("a9bbfe4")
```
出现上面信息代表安装成功。

## 自行打包

请保证本地 `golang` 版本为 `1.8`。

```bash
$ go get -d github.com/gost-c/gost-cli # download repos
$ cd $GOPATH/src/github.com/gost-c/gost-cli
$ make build # build
# 如果 `$GOPATH/bin` 目录在环境变量 `PATH` 中， 没有请参照上面方法
$ mv ./bin/gost $GOPATH/bin/gost
```
