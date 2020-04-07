`https://gateway.pinata.cloud/ipfs/QmPN1XBSTeH8RE6QkCbg37RU6gTxcBN1RgmgG5x9qozoLE`
`mv ./QmPN1XBSTeH8RE6QkCbg37RU6gTxcBN1RgmgG5x9qozoLE ./robonomics`
`chmod +x ./robonomics`
`mv ./robonomics /usr/bin/robonomics`
`rm -rf /home/robonomics/.local/share/robonomics/chains/ipci/db/`
`systemctl restart robonomics_ipci.service`
