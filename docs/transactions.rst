.. index ! transactions

.. _transactions:

############
Transactions
############

HTTP
----

List Transactions
~~~~~~~~~~~~~~~~~

.. code-block:: bash

  curl "https://api.ethrex.io/v1/homestead/transactions?limit=1&offset=0&sort=timestamp&direction=descending"

.. code-block:: json

  [
    {
      "R": 6.358799344352821e+76,
      "S": 2.6771635834424243e+76,
      "V": 27,
      "blockHash": "0xf89135f92fa485758b7533ad736d28459c5ec8f3d9f15fe7dab0e99147d14706",
      "blockNumber": 2423803,
      "bloom": "0x0000000000100004000000000000000000000000400000000000000000000000",
      "confirmed": true,
      "cost": 1008991665461455100,
      "cumulativeGasUsed": 169905,
      "from": "0x1e9939daaad6924ad004c2560e90804164900341",
      "gasLimit": 90000,
      "gasPrice": 23836183119,
      "gasUsed": 22905,
      "hash": "0xf79aee813a469a0d00efc946f56996853a666fab39eedb4e8c18b6563f1e5f75",
      "internal": false,
      "internalTransactionCount": 2,
      "kind": "valueTransfer",
      "logs": [
        {
          "address": "0xb0b8a5cb95c8ab1ad54e5bf53602f2c7877eb877",
          "data": "AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAADfkJeXasy4w=",
          "topics": [
            "0x90890809c654f11d6e72a28fa60149770a0d11ec6c92319d6ceb2bb0a4ea1a15",
            "0x0000000000000000000000001e9939daaad6924ad004c2560e90804164900341",
            "0x0000000000000000000000000000000000000000000000000000000000000058"
          ]
        }
      ],
      "methodSpecification": null,
      "nonce": 29318,
      "signatureHash": "0xa6f2df70f779e12ec39722880469ab97475956ad330c0960176837dcf5a4417a",
      "size": 113,
      "timestamp": 1476235015,
      "to": "0xb0b8a5cb95c8ab1ad54e5bf53602f2c7877eb877",
      "transactionIndex": 7,
      "value": 1006846408980745100
    }
  ]

Retrieve Transaction Information
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: bash

  curl https://api.ethrex.io/v1/homestead/transactions/0xf79aee813a469a0d00efc946f56996853a666fab39eedb4e8c18b6563f1e5f75

.. code-block:: json

  {
    "R": 6.358799344352821e+76,
    "S": 2.6771635834424243e+76,
    "V": 27,
    "blockHash": "0xf89135f92fa485758b7533ad736d28459c5ec8f3d9f15fe7dab0e99147d14706",
    "blockNumber": 2423803,
    "bloom": "0x0000000000100004000000000000000000000000400000000000000000000000",
    "confirmed": true,
    "cost": 1008991665461455100,
    "cumulativeGasUsed": 169905,
    "from": "0x1e9939daaad6924ad004c2560e90804164900341",
    "gasLimit": 90000,
    "gasPrice": 23836183119,
    "gasUsed": 22905,
    "hash": "0xf79aee813a469a0d00efc946f56996853a666fab39eedb4e8c18b6563f1e5f75",
    "internal": false,
    "internalTransactionCount": 2,
    "kind": "valueTransfer",
    "logs": [
      {
        "address": "0xb0b8a5cb95c8ab1ad54e5bf53602f2c7877eb877",
        "data": "AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAADfkJeXasy4w=",
        "topics": [
          "0x90890809c654f11d6e72a28fa60149770a0d11ec6c92319d6ceb2bb0a4ea1a15",
          "0x0000000000000000000000001e9939daaad6924ad004c2560e90804164900341",
          "0x0000000000000000000000000000000000000000000000000000000000000058"
        ]
      }
    ],
    "methodSpecification": null,
    "nonce": 29318,
    "signatureHash": "0xa6f2df70f779e12ec39722880469ab97475956ad330c0960176837dcf5a4417a",
    "size": 113,
    "timestamp": 1476235015,
    "to": "0xb0b8a5cb95c8ab1ad54e5bf53602f2c7877eb877",
    "transactionIndex": 7,
    "value": 1006846408980745100
  }

Retrieve Transaction Trace
~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: bash

  curl https://api.ethrex.io/v1/homestead/transactions/0xf79aee813a469a0d00efc946f56996853a666fab39eedb4e8c18b6563f1e5f75/trace

.. code-block:: json

  [
    {
      "depth": 1,
      "err": null,
      "gas": 68997,
      "gasCost": 3,
      "memory": "",
      "op": "PUSH1",
      "programCounter": 0,
      "stack": null,
      "storage": {}
    },
    ...
  ]

Specification
-------------

Transaction
~~~~~~~~~~~

================= ================= ===========
Key               Type              Description
----------------- ----------------- -----------
hash              string            Hex-encoded transaction hash - special for internal.
blockHash         string            Hex-encoded hash of the transaction's block, if any.
blockNumber       int               Number of the block in which the transaction is included.
transactionHash   string            Hex-encoded hash of the parent transaction.
internal          bool              Whether the transaction is an internal transaction.
confirmed         bool              Whether or not the transaction has been confirmed.
depth             int               For internal transactions, transaction depth.
transactionIndex  int               Index of the transaction in the block.
nonce             int               Transaction nonce.
from              string            Hex-encoded address of transaction sender.
to                string            Hex-encoded address of transaction recipient.
gasLimit          int               Transaction gas limit.
gasUsed           int               Transaction gas used.
gasPrice          int               Transaction gas price.
data              string            Base64-encoded transaction data.
timestamp         int               Transaction timestamp.
kind              string            Transaction kind (see :ref:`Kinds`).
value             int               Transaction value.
cost              int               Transaction cost, where applicable.
size              int               Transaction size in bytes.
signatureHash     string            Hash of transaction signature.
V                 int               V parameter of transaction signature.
R                 int               R parameter of transaction signature.
S                 int               S parameter of transaction signature.
cumulativeGasUsed int               Cumulative gas used by transaction.
bloom             string            Hex-encoded bloom filter.
storageDiff       map[string]string Storage entries written by transaction, hex-encoded.
logs              []log             Transaction logs.
contractAddress   string            Hex-encoded address of contract created, if any.
err               string            Error encountered during transaction processing, if any.
================= ================= ===========

Log
~~~

======= ======== ===========
Key     Type     Description
------- -------- -----------
Address string   Hex-encoded log address.
Topics  []string Hex-encoded log topics.
Data    string   Base64-encoded log data.
======= ======== ===========

.. _kinds:

Kinds
-----

* **genesis** Genesis transactions included in genesis block.
* **minerReward** Transactions paid to miners for mining blocks.
* **uncleReward** Transactions paid to miners for mining uncles.
* **fee** Transaction fees.
* **contractCreation** Transactions which created contracts.
* **contractInvocation** Transactions which invoked methods on contracts.
* **valueTransfer** Transactions which transfered Ethereum only.
* **selfDestruct** Self-destruct transactions.
