
# 重新安装后配置文件找回

解压文件：dpkg -x 会将 .deb 文件中的文件和目录结构解压到指定的目标目录

dpkg -x <package.deb> <destination_directory>

```
dpkg -x /path/xx.deb /path/confdir

dpkg -x /opt/blockbook/build/backend-dogecoin-testnet_1.14.9-satoshilabs-1_amd64.deb /root/blockbook/backend-dogecoin-testnet/

dpkg -x /opt/blockbook/build/blockbook-dogecoin-testnet_0.4.0_amd64.deb /root/blockbook/blockbook-dogecoin-testnet/
```

# 进程管理文件

**backend-dogecoin-testnet.service**

**blockbook-dogecoin-testnet.service**

```
/root/blockbook/backend-dogecoin-testnet/lib/systemd/system/backend-dogecoin-testnet.service

/root/blockbook/blockbook-dogecoin-testnet/lib/systemd/system/blockbook-dogecoin-testnet.service
```

* dogecoin 配置文件

```
ls /root/blockbook/backend-dogecoin-testnet/opt/coins/nodes/dogecoin_testnet/

dogecoin_testnet.conf  dogecoin_testnet_client.conf
```
