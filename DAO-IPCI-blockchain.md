`https://gateway.pinata.cloud/ipfs/QmPN1XBSTeH8RE6QkCbg37RU6gTxcBN1RgmgG5x9qozoLE`

`mv ./QmPN1XBSTeH8RE6QkCbg37RU6gTxcBN1RgmgG5x9qozoLE ./robonomics`

`chmod +x ./robonomics`

`mv ./robonomics /usr/bin/robonomics`

`rm -rf /home/robonomics/.local/share/robonomics/chains/ipci/db/`

`systemctl restart robonomics_ipci.service`

`ssh -L 9944:localhost:9944 root@178.62.41.59`

`./subkey -n robonomics -k transfer 0хPRIVATE 4G6w1MiMqQgbN4ntFDwCZmgCBSHNYzWiFLs1Re4FjXaR9wRk 1000000000000 0`
