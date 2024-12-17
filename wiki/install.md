
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

BASE_IMAGE = gostartups/blockbook-build

2）注释

安装golang & rocksdb
```

## 编译bitcoin deb包

```
make all-bitcoin

make all-bitcoin_testnet4
```

## 服务管理

```
systemctl start backend-bitcoin.service

systemctl start blockbook-bitcoin.service


systemctl start backend-bitcoin_testnet4.service

systemctl start blockbook-bitcoin_testnet4.service
````