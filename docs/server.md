# 服务端

!> 请确保了解 `golang`，并且需要了解项目使用的库

项目地址：[gost-c/gost](https://github.com/gost-c/gost)

## 库

- [gin](https://github.com/gin-gonic/gin) Gin is a HTTP web framework written in Go (Golang).
- [gorm](https://github.com/jinzhu/gorm)(with mysql) The fantastic ORM library for Golang, aims to be developer friendly
- [gin-jwt](https://github.com/appleboy/gin-jwt) JWT Middleware for Gin framework
- [go.uuid](https://github.com/satori/go.uuid) UUID package for Go
- [scrypto](https://github.com/srfrog/scrypto) Scrypt functions for Go

## 项目目录

```
- main.go         # 入口文件
- .env            # 需要环境变量
- server          # server包，提供核心服务
  |- db.go        # 数据库model
  |- helpers.go   # helper函数
  |- jwt.go       # jwt中间件
  |- server.go    # 服务端核心
  |- mock.go      # 开发阶段假数据填充handler
```
需要 `MySQL` 数据库， 并且需要设置 `.env.example` 中的环境变量，建议使用 [enr](https://github.com/gost-c/enr) 工具。

```bash
$ MYSQL_DB_URL=mysql_user:mysql_passwd@/mysql_db_name?charset=utf8&parseTime=True&loc=Local JWT_SECRET="you secret" GIN_MODE=debug go run main.go
# 使用 enr, 配置环境变量到 .env 文件中
$ enr go run main.go
```

## 部署

将代码置于服务器

```bash
$ nohup MYSQL_DB_URL=mysql_user:mysql_passwd@/mysql_db_name?charset=utf8&parseTime=True&loc=Local JWT_SECRET="you secret" GIN_MODE=release go run main.go &
# 使用 enr, 将 .env 文件中 GIN_MODE 改为 release
$ nohup enr go run main.go &
```
