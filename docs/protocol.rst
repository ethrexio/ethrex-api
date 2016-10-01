.. index ! protocol

.. _protocol:

########
Protocol
########

.. _network specification:

Network Specification
---------------------

Ethrex provides APIs for both the Ethereum Homestead mainnet and the Morden testnet, which function identically.
To switch from one to the other, change the network component of the request path.

Requests targeting the Homestead mainnet should be made to https://api.ethrex.io/v1/homestead/.

Requests targeting the Morden testnet should be made to https://api.ethrex.io/v1/morden/.

.. _authentication:

Authentication
--------------

Requests against the Ethrex API require authorization. You will need to register for an API key by emailing support@ethrex.io.

Once you have received your API key, pass it with your HTTP request by appending the header ::
  
  Authorization: Bearer <APIKEY>
