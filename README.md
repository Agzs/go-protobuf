## golang 使用 protobuf 的教程

### 1、下载protobuf的编译器protoc

[下载地址：](https://github.com/google/protobuf/releases)
#### window：
 * 下载: protoc-3.3.0-win32.zip
 * 解压，把bin目录下的protoc.exe复制到GOPATH/bin下，GOPATH/bin加入环境变量。
 * 当然也可放在其他目录，需加入环境变量，能让系统找到protoc.exe
#### linux：
 * 下载：protoc-3.3.0-linux-x86_64.zip 或 protoc-3.3.0-linux-x86_32.zip
 * 将压缩包解压，把protoc-3.3.0-linux-x86_64/bin目录下的protoc复制到GOPATH/bin下
 * GOPATH/bin加入环境变量。编辑~/.bashrc文件，在最后添加：
 * export GOPATH="go项目的路径"
 * export PATH=$PATH:$GOPATH/bin
 * 如果喜欢编译安装的，也可下载源码自行安装，最后将可执行文件加入环境变量。
    源码地址：https://github.com/google/protobuf

### 2、获取protobuf的编译器插件protoc-gen-go
 * 进入GOPATH目录
 * 运行 go get -u github.com/golang/protobuf/protoc-gen-go
 * 如果成功，会在GOPATH/bin下生成protoc-gen-go.exe文件

### 3、拷贝库文件
* 从解压目录protoc-3.3.0-linux-x86_64/include/google/protobuf中拷贝全部文件,复制到 GOPATH/src/google/protobuf目录下

### 4、运行
 * protoc --go_out=. *.proto
 * Note，*前有空格，*是你proto文件的名称
    


