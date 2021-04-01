## 说明
本教程仅帮助您启动 MathChain-Galois 验证人节点，如您不需要验证人功能，请查看 [全节点搭建教程](https://docs.mathchain.org/cn/tut_run_node.md)
<font color="#dd0000">\* 重要：如果您之前运行过0.6.1版本之前的节点，在启动节点前，需要删除之前链的数据文件夹，即之前启动命令中 -d 部分。</font>

## 环境准备

### 测试网节点配置建议
最低配置：单核2G服务器，硬盘30G

推荐配置：双核4G服务器，硬盘50G

### 以下两种获取可执行文件方式任选其一

#### 1、从源码编译（对机器要求比较高，至少双核4G，没有负载才可以正常编译）
源码仓库：https://github.com/mathwallet/MathChain

- 编译环境配置
- 启动命令行
- 进入 mathchain 根目录
- cargo build --release
- 可以在 mathchain/target/release 下面找到编译好的可执行文件 mathchain(.exe)

#### 2、根据系统下载可执行文件
当前版本 0.6.1

- [macOS Catalina](https://github.com/mathwallet/MathChain/releases/download/0.6.1/mathchain-0.6.1-x86_64-apple-darwin.tar.bz2)
- [Linux](https://github.com/mathwallet/MathChain/releases/download/0.6.1/mathchain-0.6.1-x86_64-linux-gnu-glibc-2.17-llvm-3.8.tar.bz2)

## 启动步骤：

### 一、准备一个MathChain-Galois账户
可以查看 [创建账户教程](https://docs.mathchain.org/cn/tut_create_account)

### 二、填写申请表单
打开 [申请表单](https://docs.qq.com/form/page/DUXBFUVpVWUxLcFFr)

我们将挑选稳定的节点成为验证人节点，如果通过申请我们会通过您填写的联系方式联系您。

当您的申请被通过后，我们为您申请表中填写的测试网络地址添加少许MATH，以供后续操作使用。

### 三、启动节点

1、使用下列启动命令启动节点：

```
./mathchain \
	-d /tmp/example \
	--name Example \
  --validator \
  --chain galois
```

可以使用nohup命令将代码放置在后台运行，也可以使用其他进程管理程序进行进程管理，以下以nohup为例：

```
nohup ./mathchain \
	-d /tmp/example \
	--name Example \
  --validator \
  --chain galois > galois.log &
```

2、在服务器命令行内，执行如下命令，并记录返回结果：

```
curl -H "Content-Type:application/json" -d '{"id":1,"jsonrpc":"2.0", "method":"author_rotateKeys", "params":[]}' http://localhost:9933

返回示例：
{"jsonrpc":"2.0","result":"0x84a1635e10889e04ae3dbeabe8f765f044a3ac0c0d582bdab4f0b4cba18b862749e544da941ab7934fd7892054b0e0da90456c3732dd511c5608041413040a93","id":1}
```

3、在链上设置session key：

![](/images/run_validator_node/set_session_key.png)

4、在节点同步完成后，请在微信群或者TG内联系管理员，我们将在验证后将您的节点加入到验证人列表中。

### 注意事项

1、mathchain 0.6.0与之前版本网络不兼容，老版本已不再维护，需要删除之前网络数据重新同步；

2、为保证网络质量，本轮验证人节点需要经过人工筛选，申请结果会有少许延迟，还请申请之后耐心等待；

3、如果同步全节点，想成为验证人，需要重新同步节点，验证人节点数据与全节点数据类型不同，无法兼容；