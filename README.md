# BITCOIN NODE
To deploy your Bitcoin node run the following command.

```bash
# docker run -d --name=bitcoin-node -h bitcoind -p 8332:8332 -p 8333:8333 anak10thn/bitcoin-node
```

Alternatively, to start a secure standalone Bitcoin node omit port options to disallow port connection from the external network:

```bash
# docker run -d --name=bitcoin-node -h bitcoind anak10thn/bitcoin-node
```

The above commands will instantly start and configure your Bitcoin node. Once your Bitcoin has started depending on your environment it will take around 24 hours synchronize with the latest bitcoin block chain. Currently, you can expect your /root/.bitcoin/blocks directory to grow to about 35GB in size.

Obtain rpcuser credentials :

```bash
#  docker exec bitcoin-node cat /root/.bitcoin/bitcoin.conf
```

Get bitcoin wallet balance :

```bash
# docker exec bitcoin-node bitcoin-cli getbalance
```

Obtain bitcoin mining info :

```bash
# docker exec bitcoin-node bitcoin-cli getmininginfo
```

For more available bitcoin commands run:

```bash
# docker exec bitcoin-node bitcoin-cli help
```
