Name:                   Veles (Cryptocurrency)
Image:                  /images/logo/veles256.png
Ticker:                 VLS
ProgrammingLanguage:    C++
InitialRelease:         November 2018
OrgStructure:           Decentralized
OpenSource:             Yes
License:                MIT
ConsensusMechanism:     Proof of Work
DevelopmentStatus:      Alpha (active)
Bitcointalk:            [\[ANN\] ▼ VELES ... ](https://bitcointalk.org/index.php?topic=5064523)
Website:                https://www.veles.network
Whitepaper:             [WP - First Release](https://veles.network/Whitepaper.wiki.en.html)

# Coin Specifications

General Specifications  | :
----------------------- | -------------------------------------------
Mining Algorithms       | Lyra2z, X11, X16R, Sha256d, Scrypt, Nist5
Maximum Supply          | 2 500 000 VLS
Circulating Supply      | {: data-entity-id="market.price" data-attribute="total_supply" data-format="number" data-fixed-decimals="2" data-unit="VLS" .ws }
Block Time              | 2 minutes 
Coin-swap Premine       | 50 000 VLS
Blockchain Height       | {: data-entity-id="chain.tip" data-format="number" data-attribute="height" data-unit="blocks" .ws }

Masternode Specifications   | :
--------------------------- | ---------------------------------------
Masternode Collateral       | 500 VLS
Number of Masternodes       | {: data-entity-id="masternodes" data-attribute="count" .ws }
Enabled dApps               | dVPN, dDNS (recursive)

Block Reward Specifications | ⚒
--------------------------- | ---------------------------------------
Maximum Block Reward        | {: data-entity-id="chain.halving.status" data-attribute="max_block_reward" data-format="number" data-fixed-decimals="2" data-unit="VLS" .ws }
Minimum Block Reward        | 0.01 VLS
Average Block Reward        | {: data-entity-id="chain.stats.mining" data-attribute="block_reward_average" data-format="number" data-fixed-decimals="2" data-unit="VLS" .ws }
PoW Miner Reward %          | {: data-entity-id="chain.stats.mining" data-attribute="block_reward_pow_percent" data-format="number" data-fixed-decimals="2" data-unit="%" .ws }
Masternode Reward %         | {: data-entity-id="chain.stats.mining" data-attribute="block_reward_mn_percent" data-format="number" data-fixed-decimals="2" data-unit="%" .ws }
Dev Team Reward %           | {: data-entity-id="chain.stats.mining" data-attribute="block_reward_dev_percent" data-format="number" data-fixed-decimals="2" data-unit="%" .ws }
Dev Team Address            | VKtig9w7wfx6Ep9B4NnbwxLj1bkY2kHXBj

Block Reward Halving           | ⚒
------------------------------ | ------------------------------------
Blocks to next halving check:  | {: .chain-pow-blocks-to-next-epoch .ws }
Epoch start block              | {: data-entity-id="chain.halving.status" data-attribute="start_block" .ws }
Epoch end block                | {: data-entity-id="chain.halving.status" data-attribute="end_block" .ws }
Supply emitted since halving   | {: data-entity-id="chain.halving.status" data-attribute="supply_since_halving" data-format="number" data-fixed-decimals="2" data-unit="VLS" .ws }
Supply emission target         | 160 000 VLS
Supply target reached by       | {: data-entity-id="chain.halving.status" data-attribute="supply_target_reached" .ws }
Min % required from target     | 80%
Current halving epoch          | {: data-entity-id="chain.halving.status" data-attribute="epoch_name" .ws }

For more information and full list of previous halving epochs see [Halving Epochs table on the Mining Stats](https://explorer.veles.network/miningstats#halving-epoch-table) page on the Explorer. You can also check `gethalvingstatus` command in your local wallet. 


!!! note ""
    Items shown in green are dynamically changing by the network's consensus
    and display current values right now.
    {: .ws}

    If you see some values missing, it's probably because you're not viewing
    this page using official wiki web-app, then plese visit
    [current page on the Veles Core wiki](http://veles.network/Coin-Specifications.wiki.en.html).
    If you do then your browser is facing issues with the connection to 
    the backend server.
    {: .websocket-offline}
