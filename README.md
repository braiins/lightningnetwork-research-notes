# Presentation link
 <LightningNetwork.pdf>
# BIPS


## Relative lock-time

- BIP 68 Relative lock-time using consensus-enforced sequence numbers
- BIP 112 (CHECKSEQUENCEVERIFY) - describes also use cases - htlc, bidirectional payment channels and the Lightning Network, requires BIP68
- BIP 113 Median time-past as endpoint for lock-time calculations


# Resources
- original LN whitepaper: <https://lightning.network/lightning-network-paper.pdf>

- a series of articles covering many aspects of LN:
  - <https://bitcoinmagazine.com/articles/understanding-the-lightning-network-part-building-a-bidirectional-payment-channel-1464710791/>
  - <https://bitcoinmagazine.com/articles/debunking-the-most-stubborn-lightning-network-myths-1444837807/>
  - <https://bitcoinmagazine.com/articles/does-the-lightning-network-threaten-bitcoin-s-censorship-resistance-1462904079/>
  - <http://bitcoinschannel.com/lightning-how-payment-channels-build-up-a-network/>

- cross blockchain trades/atomic swaps: <http://www.coindesk.com/cross-blockchain-trades-lightning-gives-new-life-atomic-swaps/>
- documentation of the current protocol implementation: <https://github.com/lightningnetwork/lightning-rfc>
- very recommended highlevel view of the current spec by Rusty Russel: <https://medium.com/@rusty_lightning/the-bitcoin-lightning-spec-part-1-8-a7720fb1b4da>
- limitations and other issues: <https://medium.com/@rusty_lightning/bitcoin-lightning-things-to-know-e5ea8d84369f>
- Rusty Russell's blog describing LN: <https://rusty.ozlabs.org/?p=450>
- THE WIKI - terminology: <https://en.bitcoin.it/wiki/Lightning_Network>
- setting up and testing with a faucet (free giveaway of coins through LN channel): <http://lightning.community/lnd/faucet/2017/01/19/lightning-network-faucet/>
- Elements project: <https://github.com/ElementsProject/lightning/tree/master/doc>

# Demo

# Environment setup

```
mkdir ln-example
cd ln-example
virtualenv .venv
git clone https://github.com/braiins/lnd
. .venv/bin/activate
cd lnd/docker
git checkout -b ltc-rebased-master origin/ltc-rebased-master
source conf/bitcoin
```

And follow the README.md and start charlie too:

```
docker-compose up -d --no-recreate charlie
docker exec -ti btc_charlie /bin/bash
```
