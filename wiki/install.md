
运行在 Debian 12

参考资料

https://trezor.io/learn/a/custom-backend-in-trezor-suite

https://hub.docker.com/r/gostartups/blockbook-build

https://www.ankr.com/rpc/btc/btc_blockbook/

https://www.ankr.com/docs/rpc-service/chains/chains-api/btc/#get-block

## 替换系统镜像

https://hub.docker.com/r/gostartups/blockbook-build

## 修改编译内容

```
1）修改镜像

./Makefile

BASE_IMAGE = gostartups/blockbook-build

2）注释

./build/docker/bin/Dockerfile

安装golang & rocksdb
```

## 编译bitcoin deb包

```
make all-bitcoin

make all-bitcoin_testnet4
```

## 服务管理

推荐 blockbook-xxx.service -workers=1 添加命令行选项，防止同步出错

https://github.com/trezor/blockbook

run blockbook with parameter -workers=1. This disables bulk import mode, which caches a lot of data in memory (not in rocksdb cache). It will run about twice as slowly but especially for smaller blockchains it is no problem at all.

```
systemctl start backend-bitcoin.service

systemctl start blockbook-bitcoin.service


systemctl start backend-bitcoin-testnet4.service

systemctl start blockbook-bitcoin-testnet4.service
````

```
/lib/systemd/system/backend-bitcoin-testnet4.service
/lib/systemd/system/blockbook-bitcoin-testnet4.service

systemctl daemon-reload
```
