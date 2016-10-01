.. index ! blocks

.. _blocks:

######
Blocks
######

HTTP
----

List Blocks
~~~~~~~~~~~

.. code-block:: bash

  curl "https://api.ethrex.io/v1/homestead/blocks?limit=1&offset=0&sort=number&direction=descending"

.. code-block:: json

  [
    {
      "coinbase": "0xbcdfc35b86bedf72f0cda046a3c16829a2ef41d1",
      "difficulty": 88538769253969,
      "extraData": "0x000000000000000000000000000000000000000000007777772e62772e636f6d",
      "extraDataDecoded": "www.bw.com",
      "gasLimit": 1495615,
      "gasUsed": 0,
      "hash": "0x9d8dbdbda3d06ab615017f3146bb1901559b91d334d63d74895f59a611239cbe",
      "internalTransactionCount": 1,
      "internalTransactions": [
        "0x15017f3146bb1901559b91d334d63d74895f59a611239cbe0000000000000000"
      ],
      "logsBloom": "0x0000000000000000000000000000000000000000000000000000000000000000",
      "nonce": 9731251472972642000,
      "number": 2423796,
      "parentHash": "0x8282261db6138b6fa47768854cff25b173fbf5544cc509bfc136d4ed991727c9",
      "receiptsHash": "0x56e81f171bcc55a6ff8345e692c0f86e5b48e01b996cadc001622fb5e363b421",
      "size": 527,
      "stateRoot": "0x1b093f181369295c6e2ea1bb542764473f429beb1c274d4d47e816eae91a1526",
      "time": 19,
      "timestamp": 1476234855,
      "totalDifficulty": 73308743572019460000,
      "totalValue": 5e+18,
      "transactionCount": 0,
      "transactionsHash": "0x56e81f171bcc55a6ff8345e692c0f86e5b48e01b996cadc001622fb5e363b421",
      "uncle": false,
      "uncleCount": 0,
      "uncleHash": "0x1dcc4de8dec75d7aab85b567b6ccd41ad312451b948a7413f0a142fd40d49347",
      "uncles": []
    }
  ]

Retrieve Block Information
~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: bash

  curl https://api.ethrex.io/v1/homestead/blocks/0x46015afbe00cf61ff284c26cc09a776a7303e422c7b359fe4317b4e6aaa410a4

.. code-block:: json

  {
    "coinbase": "0xacc8decdfdcbed202b8632947c60487494f5d2c7",
    "difficulty": 17179840512,
    "extraData": "0x476574682f76312e302e302d30636463373634372f6c696e75782f676f312e34",
    "extraDataDecoded": "Geth/v1.0.0-0cdc7647/linux/go1.4",
    "gasLimit": 5000,
    "gasUsed": 0,
    "hash": "0x46015afbe00cf61ff284c26cc09a776a7303e422c7b359fe4317b4e6aaa410a4",
    "internalTransactionCount": 1,
    "internalTransactions": [
      "0xf284c26cc09a776a7303e422c7b359fe4317b4e6aaa410a40000000000000000"
    ],
    "logsBloom": "0x0000000000000000000000000000000000000000000000000000000000000000",
    "nonce": 8512073925418495000,
    "number": 14,
    "parentHash": "0x55b6a7e73c57d1ca35b35cad22869eaa33e10fa2a822fb7308f419269794d611",
    "receiptsHash": "0x56e81f171bcc55a6ff8345e692c0f86e5b48e01b996cadc001622fb5e363b421",
    "size": 544,
    "stateRoot": "0xd0f6f874f63d905c25a9b4a7992e86a7dedf73812570ccb852f0443110033281",
    "time": 3,
    "timestamp": 1438270161,
    "totalDifficulty": 257471483967,
    "totalValue": 5e+18,
    "transactionCount": 0,
    "transactionsHash": "0x56e81f171bcc55a6ff8345e692c0f86e5b48e01b996cadc001622fb5e363b421",
    "uncle": false,
    "uncleCount": 0,
    "uncleHash": "0x1dcc4de8dec75d7aab85b567b6ccd41ad312451b948a7413f0a142fd40d49347",
    "uncles": []
  }

Retrieve Block Transactions
~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: bash

  curl https://api.ethrex.io/v1/homestead/blocks/0x46015afbe00cf61ff284c26cc09a776a7303e422c7b359fe4317b4e6aaa410a4/transactions

.. code-block:: json

  [
    {
      "blockHash": "0x46015afbe00cf61ff284c26cc09a776a7303e422c7b359fe4317b4e6aaa410a4",
      "blockNumber": 14,
      "confirmed": true,
      "from": "0x0000000000000000000000000000000000000000",
      "hash": "0xf284c26cc09a776a7303e422c7b359fe4317b4e6aaa410a40000000000000000",
      "internal": true,
      "internalTransactionCount": 0,
      "kind": "minerReward",
      "methodSpecification": null,
      "timestamp": 1438270161,
      "to": "0xacc8decdfdcbed202b8632947c60487494f5d2c7",
      "transactionIndex": 0,
      "value": 5e+18
    }
  ]

Specification
-------------

Block
~~~~~

========================= ================= ===========
Key                       Type              Description
------------------------- ----------------- -----------
hash                      string            Hex-encoded block hash.
parentHash                string            Hex-encoded parent block hash.
blockHash                 string            Hex-encoded associated block hash (for uncles).
number                    int               Block number (height).
blockNumber               int               Associated block number (for uncles).
uncle                     bool              Whether or not the block is an uncle.
uncleHash                 string            Hex-encoded uncle hash.
logsBloom                 string            Hex-encoded Bloom filter logs.
transactionsHash          string            Hex-encoded transactions hash.
receiptsHash              string            Hex-encoded receipts hash.
stateRoot                 string            Hex-encoded state root.
coinbase                  string            Hex-encoded coinbase (miner) address.
difficulty                int               Block difficulty.
totalDifficulty           int               Block total difficulty.
extraData                 string            Block extra data.
extraDataDecoded          string            UTF-8 decoded extra data.
gasLimit                  int               Block gas limit.
gasUsed                   int               Block gas used.
timestamp                 int               Block timestamp.
time                      int               Block time, in seconds.
transactionCount          int               Block transaction count.
uncleCount                int               Block uncle count.
internalTransactionCount  int               Block internal transaction count.
nonce                     int               Block nonce.
size                      int               Block size, in bytes.
totalValue                int               Block total value.
========================= ================= ===========
