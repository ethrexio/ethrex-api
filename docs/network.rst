.. index ! network

.. _network:

#######
Network
#######

HTTP
----

Retrieve Network Information
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: bash

  curl https://api.ethrex.io/v1/homestead/network

.. code-block:: json

  {
    "blockNumber": 2423800,
    "blockHash": "",
    "ethVersion": 63,
    "gasPrice": 20000000000,
    "genesisHash": "0xd4e56740f876aef8c010b86a40d5f56745a118d0906a34e69aec8c0db1cb8fa3",
    "lastSynced": 2423800,
    "name": "homestead",
    "netVersion": 1,
    "peerCount": 25,
    "totalDifficulty": 17968865808695849000
  }

Specification
-------------

Network
~~~~~~~

========================= ================= ===========
Key                       Type              Description
------------------------- ----------------- -----------
blockNumber               int               Current block number (chain head).
blockHash                 string            Current block hash (chain head).
lastSynced                int               Last block synced with Ethrex system state.
ethVersion                int               Ethereum protocol version.
genesisHash               string            Hex-encoded genesis block hash.
gasPrice                  int               Current gas price.
name                      string            Network name.
netVersion                int               Network version.
peerCount                 int               Current peer count.
totalDifficulty           int               Current total difficulty.
========================= ================= ===========
