# AndroidLibV2rayLite

将 v2ray-core 编译为 aar 库，提供给 Android 客户端使用，本库开发的 [V2free APP ](https://github.com/bannedbook/ssvpn/) 就是使用这个aar库。

## 编译环境和步骤

### 系统环境： 推荐 Debian 9 Linux系统

### 编译步骤：
首先安装好go 和 gomobile 环境，然后请用root用户依次执行下列命令：
```
apt update
apt install git
cd /root/
git clone https://github.com/bannedbook/AndroidLibV2rayLite.git
cd /root/AndroidLibV2rayLite
cp -r AndroidLibV2rayLite go/src
cd /root/go/src/AndroidLibV2rayLite
chmod +x build_libv2ray_aar.sh
./build_libv2ray_aar.sh sdk data dep
```

最后一条就是编译命令了，后面的3个参数请酌情选择：
* sdk 表示会安装 Android SDK Tool 和 NDK
* data 参数表示会更新 geoip.dat  geosite.dat 文件
* dep 表示会执行 go get -u 更新v2ray core 程序等本地依赖
