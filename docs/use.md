# 使用

请确保 `gost-cli` 已成功安装。

## 帮助

`gost-cli` 提供默认帮助以及子菜单帮助

```bash
# show all help
$ gost -h
# show help msg of register
$ gost register -h
```

## 注册

你需要注册账号才可以使用。

```bash
$ gost register -u=用户名 -p=密码
# register success
```
!> 用户名支持字母数字，最少6位最多20位， 密码最少6位

## 登录

登录后才可使用 `push` 功能。

```bash
$ gost login -u=用户名 -p=密码
# login success
```

## 上传

假如我们目录下有两个文件 `test.js`, `README.md` 需要上传。

```bash
$ gost push test.js README.md
# 成功会获得url链接
# 增加自己的介绍
$ gost push -d="my custom description" test.js README.md
```
?> 使用相对路径时，相对于当前目录，也可以使用绝对路径
