# bitcoin mainnet

删除tls证书配置

```
cd /etc/systemd/system

vi blockbook-bitcoin.service
删除 -certfile=/opt/coins/blockbook/bitcoin/cert/blockbook

systemctl daemon-reload

systemctl stop blockbook-bitcoin.service

systemctl start blockbook-bitcoin.service

systemctl status blockbook-bitcoin.service
```

[注]
/lib/systemd/system
不要在这个目录中改
