## 环境准备

### 测试网节点配置建议
最低配置：单核2G服务器，硬盘30G
推荐配置：双核4G服务器，硬盘50G

### 以下两种获取可执行文件方式任选其一

#### 1、从源码编译

- 编译环境配置
- 启动命令行
- 进入 mathchain 根目录
- cargo build --release
- 可以在 mathchain/target/release 下面找到编译好的可执行文件 mathchain(.exe)

#### 2、下载可执行文件
当前版本 0.5.1
- [macOS Catalina](https://github.com/mathwallet/MathChain/releases/download/0.5.1/mathchain-0.5.1-x86_64-apple-darwin.tar.bz2)
- [Linux](https://github.com/mathwallet/MathChain/releases/download/0.5.1/mathchain-0.5.1-x86_64-linux-gnu-glibc-2.17-llvm-3.8.tar.bz2)

## 启动参数

#### 从命令行读取配置启动

```sh
./mathchain \
	-d /tmp/example \
	--name Example \
    	--chain galois
```

### 常用参数

|     参数     |                                      注释                                       |  子参数  | 子参数类型 |
| :----------: | :-----------------------------------------------------------------------------: | :------: | :--------: |
|  validator   |                              节点类型为验证人节点                               |    无    |     无     |
| rpc-external | 监听所有 rpc，验证人节点需要使用 `--unsafe-rpc-external` 但不推荐验证人节点开启 |    无    |     无     |
| ws-external  |  监听所有 ws，验证人节点需要使用 `--unsafe-ws-external` 但不推荐验证人节点开启  |    无    |     无     |
|     port     |                                    p2p 端口                                     |  端口号  |    数字    |
|   rpc-port   |                                    rpc 端口                                     |  端口号  |    数字    |
|   ws-port    |                                     ws 端口                                     |  端口号  |    数字    |
|  base-path   |                           保存用于链的各种数据的地址                            |   路径   |   字符串   |
|     name     |                                   节点的名称                                    |  节点名  |   字符串   |
|   rpc-cors   |                                  请求头白名单                                   | 过滤类型 |    枚举    |
|  bootnodes   |            用来获取启动数据的种子节点（/ip4/0.0.0.0/tcp/0/p2p/xxx）             | 节点 URL | 字符串数组 |

#### 查看所有参数

```
./mathchain --help
```

## 启动节点

### 启动命令

```sh
./mathchain \
	-d /tmp/example \
	--name Example \
    	--chain galois
```

建议使用 systemctl，pm2，screen 等工具来维护进程。

### 种子节点

测试网已内置种子节点地址

### Q&A

- Q：无法启动节点
- A：
	1. 确认系统支持该可执行文件
	1. 部分动态链接库依赖丢失，安装依赖

- Q：我的节点为什么不同步块
- A：
	1. 检查 bootnodes 是否填错
	1. 与目标节点网络通信差，尝试其他 bootnodes
	1. 目标节点连接数已满，尝试其他 bootnodes
	1. 确认版本号一致（多数情况下并不需要完全一致）

- ***如仍有问题，欢迎[提交 issue]("https://github.com/mathwallet/MathChain/issues/new")***
