.. index ! accounts

.. _accounts:

########
Accounts
########

HTTP
----

List Accounts
~~~~~~~~~~~~~

.. code-block:: bash

  curl "https://api.ethrex.io/v1/homestead/accounts?limit=1&offset=0&sort=balance&direction=descending"

.. code-block:: json

  [
    {
      "address": "0xb136707642a4ea12fb4bae820f03d2562ebff487",
      "balance": 7277385711515429000000000,
      "contract": false,
      "lastSeen": 1467553276,
      "minedCount": 0,
      "nonce": 3,
      "recvCount": 662,
      "sentCount": 621
    }
  ]

Retrieve Account Information
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: bash

  curl https://api.ethrex.io/v1/homestead/accounts/0xdc84953d7c6448e498eb3c33ab0f815da5d13999

.. code-block:: json

  {
    "address": "0xdc84953d7c6448e498eb3c33ab0f815da5d13999",
    "balance": 0,
    "bytecode": "YGBgQFJgAGABgZBVYAKBkFVgA1ViCTqAQgFgBFU0YAJVYAWAVGABYKBgAgoDGRYzF5BVYQUcgGEAQGAAOWAA82BgYEBSNhVhAI1XYOBgAgpgADUEYxOvQDWBFGEAmFeAYzXB00kUYQDSV4BjcN6nmhRhATNXgGOM9Nv7FGEBPFeAY42ly1sUYQF6V4BjkAOt/hRhAYxXgGOmDzWIFGEBlVeAY6iMXvcUYQGeV4Bjtp74qBRhAkRXgGPIeWVyFGECTVeAY+l9y2IUYQJ8V1thAyBhAnphAoBWW2EDIGAENWAFVDNgAWCgYAIKA5CBFpEWFBVhAkFXYAWAVGACgFQ0AZBVYAFgoGACCgMZFoIXkFVQVlthAyJgBDVgAIBUgpCBEBVhAAJXUIBSYAICYACAUWAgYQT8gzmBUZFSgQFUfykN7NlUi2Ko1gNFqYg4b8hLpryVSEAI9jYvkxYO8+VkkZCRAVRgAWCgYAIKA5GQkRaQglZbYQNIYARUgVZbYQMgYAVUM2ABYKBgAgoDkIEWkRYUFWECeldgA4BUNAGQgZBVYAAUgBVhAXBXUGAEVEIRWxVhBNFXYQJ6VlthA1pgBVRgAWCgYAIKAxaBVlthA0hgAlSBVlthA0hgAVSBVltgA4BUNAGQVWABVGAAgFRhAyCSgpGBEBVhAAJXkIBSYAICYACAUWAgYQT8gzmBUZFSAYFQYANUYAGRkJEBVJFQgZAQYQJBV2ABVGAAgFSQkZCBEBVhAAJXgYBSYAICYACAUWAgYQT8gzmBUZFSAZBQYEBRkFRgAWCgYAIKAxaQYACQg5CCgYGBhYiD8VBQYAOAVJGQkQOQVVBQYAGAVIEBkFVbUFZbYQNIYANUgVZbYQMgYAVUM2ABYKBgAgoDkIEWkRYUFWECeldgAoBUNAGQgZBVYAAUFWEEp1dbVlthAyBbYABgAGcBY0V4XYoAADQQFYAVYQKlV1BoArXjrxaxiAAANBEVWxVhA3dXYAKAVGAUNJCBBJGCAZCSVWADgFSRkJIDAZBVYACAVGABgQGAg1WQk1CQgYSAFYKQEWEDhFdgAgKBYAICg2AAUmAgYAAgkYIBkQFhA4SRkFuAghEVYQSjV4BUYAFgoGACCgMZFoFVYABgAZGQkQGQgVVhAvpWWwBbYEBRgINgAWCgYAIKAxaBUmAgAYKBUmAgAZJQUFBgQFGAkQOQ81tgQIBRkYJSUZCBkANgIAGQ81tgQIBRYAFgoGACCgOSkJIWglJRkIGQA2AgAZDzW2ACgFQ0AZBVW1BQVltQUFBQM2AAYABQg4FUgRAVYQACV4GAUmACAmAAgFFgIGEE/IM5gVGRUgGQUIBUYAFgoGACCgMZFpCRF5BVYACAVGAUNJCBBJADYAICkZCEkIEQFWEAAldgAgJ/KQ3s2VSLYqjWA0WpiDhvyEumvJVIQAj2Ni+TFg7z5WQBkZCRVWABVIFUgRAVYQACV2ADVGACkZCRAn8pDezZVItiqNYDRamIOG/IS6a8lUhACPY2L5MWDvPlZAFUklCCkBCQUGEEnldgAVRgAIBUkJGQgRAVYQACV2ACAmAAgFFgIGEE/IM5gVGRUgFUYEBRYAFgoGACCgORkJEWkZCDkIKBgYGFiIPxUFBgA4BUkZCRA5BVUFBgAYBUgQGQVVthA4BWW1CQVltgBVRgQFFgAlRgAWCgYAIKA5KQkhaRYACRgoGBgYWIg/FQUFBgAlVQVltgBVRgA1RgQFFgAWCgYAIKA5KQkhaRYACRkIKBgYGFiIPxUFBQYANVUFYpDezZVItiqNYDRamIOG/IS6a8lUhACPY2L5MWDvPlYw==",
    "contract": true,
    "interface": [
      {
        "constant": false,
        "inputs": [
          {
            "name": "_owner",
            "type": "address"
          }
        ],
        "name": "setOwner",
        "outputs": [],
        "type": "function"
      },
      {
        "constant": true,
        "inputs": [
          {
            "name": "",
            "type": "uint256"
          }
        ],
        "name": "participants",
        "outputs": [
          {
            "name": "etherAddress",
            "type": "address"
          },
          {
            "name": "PayAmount",
            "type": "uint256"
          }
        ],
        "type": "function"
      },
      {
        "constant": true,
        "inputs": [],
        "name": "timeout",
        "outputs": [
          {
            "name": "",
            "type": "uint256"
          }
        ],
        "type": "function"
      },
      {
        "constant": false,
        "inputs": [],
        "name": "collectBalance",
        "outputs": [],
        "type": "function"
      },
      {
        "constant": true,
        "inputs": [],
        "name": "owner",
        "outputs": [
          {
            "name": "",
            "type": "address"
          }
        ],
        "type": "function"
      },
      {
        "constant": true,
        "inputs": [],
        "name": "collectedFees",
        "outputs": [
          {
            "name": "",
            "type": "uint256"
          }
        ],
        "type": "function"
      },
      {
        "constant": true,
        "inputs": [],
        "name": "payoutIdx",
        "outputs": [
          {
            "name": "",
            "type": "uint256"
          }
        ],
        "type": "function"
      },
      {
        "constant": false,
        "inputs": [],
        "name": "NextPayout",
        "outputs": [],
        "type": "function"
      },
      {
        "constant": true,
        "inputs": [],
        "name": "balance",
        "outputs": [
          {
            "name": "",
            "type": "uint256"
          }
        ],
        "type": "function"
      },
      {
        "constant": false,
        "inputs": [],
        "name": "collectFees",
        "outputs": [],
        "type": "function"
      },
      {
        "constant": false,
        "inputs": [],
        "name": "enter",
        "outputs": [],
        "type": "function"
      },
      {
        "inputs": [],
        "type": "constructor"
      }
    ],
    "lastSeen": 1457110595,
    "minedCount": 0,
    "name": "Doubler",
    "nonce": 0,
    "optimize": true,
    "recvCount": 94,
    "sentCount": 19,
    "source": "contract Doubler{\n\n    struct Participant {\n        address etherAddress;\n        uint PayAmount;\n    }\n\n    Participant[] public participants;\n\n    uint public payoutIdx = 0;\n    uint public collectedFees = 0;\n    uint public balance = 0;\n\tuint public timeout = now + 1 weeks;\n\n    address public owner;\n\n\n    // simple single-sig function modifier\n    modifier onlyowner { if (msg.sender == owner) _ }\n\n    // this function is executed at initialization and sets the owner of the contract\n    function Doubler() {\n\t\tcollectedFees += msg.value;\n        owner = msg.sender;\n    }\n\n    // fallback function - simple transactions trigger this\n    function() {\n        enter();\n    }\n    \n    function enter() {\n\t\t//send more than 0.1 ether and less than 50, otherwise loss all\n\t\tif (msg.value >= 100 finney && msg.value <= 50 ether) {\n\t        // collect fees and update contract balance\n\t        collectedFees += msg.value / 20;\n\t        balance += msg.value - msg.value / 20;\n\t\n\t      \t// add a new participant to array and calculate need balance to payout\n\t        uint idx = participants.length;\n\t        participants.length += 1;\n\t        participants[idx].etherAddress = msg.sender;\n\t        participants[idx].PayAmount = 2 * (msg.value - msg.value / 20);\n\t\t\t\n\t\t\tuint NeedAmount = participants[payoutIdx].PayAmount;\n\t\t\t// if there are enough ether on the balance we can pay out to an earlier participant\n\t\t    if (balance >= NeedAmount) {\n\t            participants[payoutIdx].etherAddress.send(NeedAmount);\n\t\n\t            balance -= NeedAmount;\n\t            payoutIdx += 1;\n\t        }\n\t\t}\n\t\telse {\n\t\t\tcollectedFees += msg.value;\n            return;\n\t\t}\n    }\n\n\tfunction NextPayout() {\n        balance += msg.value;\n\t\tuint NeedAmount = participants[payoutIdx].PayAmount;\n\n\t    if (balance >= NeedAmount) {\n            participants[payoutIdx].etherAddress.send(NeedAmount);\n\n            balance -= NeedAmount;\n            payoutIdx += 1;\n        }\n    }\n\n    function collectFees() onlyowner {\n\t\tcollectedFees += msg.value;\n        if (collectedFees == 0) return;\n\n        owner.send(collectedFees);\n        collectedFees = 0;\n    }\n\n    function collectBalance() onlyowner {\n\t\tbalance += msg.value;\n        if (balance == 0 && now > timeout) return;\n\n        owner.send(balance);\n        balance = 0;\n    }\n\n    function setOwner(address _owner) onlyowner {\n\t\tcollectedFees += msg.value;\n        owner = _owner;\n    }\n}",
    "url": "",
    "verified": true,
    "version": "v0.2.1+commit.91a6b35"
  }

Retrieve Account Sent Transactions
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: bash

  curl "https://api.ethrex.io/v1/homestead/accounts/0xdc84953d7c6448e498eb3c33ab0f815da5d13999/sent?limit=1&offset=0"

.. code-block:: json

  [
    {
      "blockHash": "0x03616cf2a12030c04188809fc1bbee5ce6239b78cc5f76e63a0f2a7de5f96c1b",
      "blockNumber": 1099021,
      "confirmed": true,
      "depth": 1,
      "from": "0xdc84953d7c6448e498eb3c33ab0f815da5d13999",
      "hash": "0x308609f7ed20e7b5084d25e146686b042250092dd419e8390100000000000000",
      "internal": true,
      "internalTransactionCount": 0,
      "kind": "valueTransfer",
      "methodSpecification": null,
      "timestamp": 1457110595,
      "to": "0x1b5cec08bf55f9d61ffa38b8e2714a3821825d7b",
      "transactionHash": "0x7bd4fc1e1abfe92a308609f7ed20e7b5084d25e146686b042250092dd419e839",
      "transactionIndex": 0,
      "value": 9.5e+17
    }
  ]

Retrieve Account Received Transactions
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: bash

  curl "https://api.ethrex.io/v1/homestead/accounts/0xdc84953d7c6448e498eb3c33ab0f815da5d13999/recv?limit=1&offset=0"

.. code-block:: json

  [
    {
      "blockHash": "0x662454ec0b509edbd29500b424d559f3ad2866e2c351a993a52ccf8ed07a3b3e",
      "blockNumber": 1031294,
      "confirmed": true,
      "from": "0xe12341d3cc891680142cae8145c92ff7133048c6",
      "hash": "0x045f58095c6fa25c7f8fbe7e09cdc7d72b5760c22f24f7d20100000000000000",
      "internal": true,
      "internalTransactionCount": 0,
      "kind": "valueTransfer",
      "methodSpecification": null,
      "timestamp": 1455946668,
      "to": "0xdc84953d7c6448e498eb3c33ab0f815da5d13999",
      "transactionHash": "0xea748d07c243b76f045f58095c6fa25c7f8fbe7e09cdc7d72b5760c22f24f7d2",
      "transactionIndex": 0,
      "value": 1e+18
    }
  ]

Retrieve Account Mined Blocks
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: bash

  curl "https://api.ethrex.io/v1/homestead/accounts/0xdc84953d7c6448e498eb3c33ab0f815da5d13999/mined?limit=1&offset=0"

.. code-block:: json

  []

Verify Contract
~~~~~~~~~~~~~~~

.. code-block:: bash

  curl -X POST "https://api.ethrex.io/v1/homestead/accounts/0xc9c1bfb27e97531ecfe005faa2b2ed4828b08a0b/verify?optimize=true&version=v0.3.5-nightly.2016.8.8%2Bcommit.c3ed550&name=Etherandom" -d @core.sol

.. code-block:: json

  {"message":"Contract verified successfully. Past method calls to this contract will be decoded and updated over the next minute or so."}

Call Contract Function
~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: bash

  curl -X POST https://api.ethrex.io/v1/homestead/accounts/0xdc84953d7c6448e498eb3c33ab0f815da5d13999/call/participants -d '[2]'

.. code-block:: json

  [
    "0x301b088c267bcc3a132691a8b18f9e5a4465e515",
    9.5e+19
  ]

Specification
-------------

Account
~~~~~~~

========================= ================= ===========
Key                       Type              Description
------------------------- ----------------- -----------
address                   string            Hex-encoded account/contract address.
contract                  bool              Whether or not the account is a contract.
bytecode                  string            Base64-encoded contract bytecode, if applicable.
nonce                     int               Account nonce.
balance                   int               Account balance.
lastSeen                  int               Timestamp account was last involved in transaction.
========================= ================= ===========
