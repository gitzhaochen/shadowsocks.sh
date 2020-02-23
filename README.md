#### Usage
```sh
#远程登陆服务器
ssh root@ip
#服务器上安装shadowsocks
wget --no-check-certificate -O shadowsocks.sh https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks.sh
#设置脚步执行权限
chmod +x shadowsocks.sh
#运行脚本 打印相关信息 根据提示窗完成配置即可
./shadowsocks.sh 2>&1 | tee shadowsocks.log

#查看或修改ss服务器的端口密码
#查看当前ss服务器所开放的端口
ss -lntp | grep ssserver
#查找ss配置文件位置
ps aux | grep ssserver
#查看配置文件
cat /etc/shadowsocks.json
#vim修改ss密码 i进入编辑模式 esc退出编辑 :wq保存退出
vi /etc/shadowsocks.json

#附：ss启动停止方法
#启动：
service shadowsocks start
#停止：
service shadowsocks stop
#重启：
service shadowsocks restart
#状态：
service shadowsocks status
```
> [shadowsocks.sh](./shadowsocks.sh) 脚本已经down下来，也可以直接跑 