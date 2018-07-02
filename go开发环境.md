1、`brew install go`

```
==> Downloading https://homebrew.bintray.com/bottles/go-1.10.1.high_sierra.bottle.tar.gz
######################################################################## 100.0%
==> Pouring go-1.10.1.high_sierra.bottle.tar.gz
==> Caveats
A valid GOPATH is required to use the `go get` command.
If $GOPATH is not specified, $HOME/go will be used by default:
  https://golang.org/doc/code.html#GOPATH

You may wish to add the GOROOT-based install location to your PATH:
  export PATH=$PATH:/usr/local/opt/go/libexec/bin
==> Summary
🍺  /usr/local/Cellar/go/1.10.1: 8,158 files, 336.7MB
```
2、`cd ~`

3、`vim .bash_profile`

加入环境变量

```
export GOROOT=/usr/local/opt/go/libexec
# GOPAT为目录路径
export GOPATH=/Users/zhangguangbin/Documents/go
export PATH=$PATH:$GOROOT/bin:$GOPATH/bin
```
4、环境变量立即生效

`source .bash_profile`

5、输入`go env` 查看配置结果

```
GOARCH="amd64"
GOBIN=""
GOCACHE="/Users/zhangguangbin/Library/Caches/go-build"
GOEXE=""
GOHOSTARCH="amd64"
GOHOSTOS="darwin"
GOOS="darwin"
GOPATH="/Users/zhangguangbin/Documents/go"
GORACE=""
GOROOT="/usr/local/opt/go/libexec"
GOTMPDIR=""
GOTOOLDIR="/usr/local/opt/go/libexec/pkg/tool/darwin_amd64"
GCCGO="gccgo"
CC="clang"
CXX="clang++"
CGO_ENABLED="1"
CGO_CFLAGS="-g -O2"
CGO_CPPFLAGS=""
CGO_CXXFLAGS="-g -O2"
CGO_FFLAGS="-g -O2"
CGO_LDFLAGS="-g -O2"
PKG_CONFIG="pkg-config"
GOGCCFLAGS="-fPIC -m64 -pthread -fno-caret-diagnostics -Qunused-arguments -fmessage-length=0 -fdebug-prefix-map=/var/folders/l8/l7hg1wx91vz7r7ts8zrq9zfh0000gn/T/go-build149998649=/tmp/go-build -gno-record-gcc-switches -fno-common"
```
6、在/Users/zhangguangbin/Documents/go文件夹下创建main.go文件
写入代码:

```
package main
import (
  "fmt"
)
func main() {
  fmt.Println("hello word");
}
```
7、保存后执行： `go run main.go`或者执行  `go build main.go`生成main文件
