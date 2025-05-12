# dogecoin testnet

安装成功后，运行也正常的，就是不能正常访问18038端口的解决办法

https://github.com/trezor/blockbook/issues/792

Fixed by: removing[test] line from /opt/coins/nodes/dogecoin_testnet/dogecoin_testnet.conf (thus moving rpcport=18038 to top level) and restarting backend-dogecoin-testnet.

删除 dogecoin_testnet.conf 配置文件中的 [test] 选项
