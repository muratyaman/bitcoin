# bitcoin

bitcoin blocks

## Block 0

```
Block Header:
{
  "Previous Block Hash": "0000000000000000000000000000000000000000000000000000000000000000", // No previous block
  "Merkle Root": "4A5E1E4BAAB89F3A32518A88F7B44F74E36C9EBCDA1A3CDED2573ED542B6FBBE",      // Transaction hash
  "Timestamp": 1231006505,                                                                // Block creation time
  "Difficulty Target": 486604799,                                                         // Lowest difficulty
  "Nonce": 2083236893                                                                     // Proof-of-work solution
}

Transaction Data:
{
  "Transaction ID": "4A5E1E4BAAB89F3A32518A88F7B44F74E36C9EBCDA1A3CDED2573ED542B6FBBE",    // Hash of transaction
  "Inputs": [
    {
      "Coinbase Message": "The Times 03/Jan/2009 Chancellor on brink of second bailout for banks" // Embedded message
    }
  ],
  "Outputs": [
    {
      "Value": 50,                                                                        // 50 BTC reward
      "Recipient Address": "Unspendable"                                                  // Cannot be spent
    }
  ]
}
```

## Block 1

```
Block Header:
{
  "Previous Block Hash": "000000000019D6689C085AE165831E934FF763AE46A2A6C172B3F1B60A8CE26F", // Hash of Genesis Block
  "Merkle Root": "F3A1A96C79BABFF39898B656E6E122DD46BFADA33B982C6F5576B049F394DAB9",      // Transaction hash
  "Timestamp": 1231469665,                                                                // Block creation time
  "Difficulty Target": 486604799,                                                         // Lowest difficulty
  "Nonce": 2573394689                                                                     // Proof-of-work solution
}

Transaction Data:
{
  "Transaction ID": "F3A1A96C79BABFF39898B656E6E122DD46BFADA33B982C6F5576B049F394DAB9",    // Transaction hash
  "Inputs": [],
  "Outputs": [
    {
      "Value": 50,                                                                        // 50 BTC reward
      "Recipient Address": "1A1zP1eP5QGefi2DMPTfTL5SLmv7DivfNa"                            // Likely Satoshi's address
    }
  ]
}
```

## Block 2

```
Block Header:
{
  "Previous Block Hash": "0000000082b5015589a3f8c7b8e9f202b02b8b2d3c728abbba4ce24fc1b9d647", // Hash of Block 1
  "Merkle Root": "6d8cdbb781e5f916ef648c813c14499f62a3e8d896d7e3058531f93cc44bbee4",  // Coinbase transaction hash
  "Timestamp": 1230988505,                                           // Block creation time
  "Difficulty Target": 486604799,                                    // Lowest difficulty
  "Nonce": 1639830024                                                // Proof-of-work solution
}

Transaction Data:
{
  "Transaction ID": "6d8cdbb781e5f916ef648c813c14499f62a3e8d896d7e3058531f93cc44bbee4",  // Hash of this transaction
  "Inputs": [],
  "Outputs": [
    {
      "Value": 50,                                                  // 50 BTC reward
      "Recipient Address": "1A1zP1eP5QGefi2DMPTfTL5SLmv7DivfNa"      // Likely Satoshi’s address
    }
  ]
}
```

## Block 170

```
Block Header:
{
  "Previous Block Hash": "00000000D77E43E6F2B5B82D82706F190FA1E5FA3CBA832DD761C0CAB74F72A8", // Block 169 hash
  "Merkle Root": "<calculated value>",                                                   // Merkle root for transactions
  "Timestamp": 1231604712,                                                               // Block creation time
  "Difficulty Target": 486604799,                                                        // Difficulty level
  "Nonce": <value found through mining>                                                  // Proof-of-work solution
}

Transaction Data:
[
  {
    "Transaction ID": "<coinbase transaction hash>",                                      // Coinbase transaction ID
    "Inputs": [],
    "Outputs": [
      {
        "Value": 50,                                                                     // Mining reward
        "Recipient Address": "<miner’s address>"
      }
    ]
  },
  {
    "Transaction ID": "<historic transaction hash>",                                      // Regular transaction hash
    "Inputs": [
      {
        "Source Address": "<Satoshi’s address>",                                          // Address with existing BTC
        "Referenced Transaction ID": "<coinbase transaction hash from earlier block>"
      }
    ],
    "Outputs": [
      {
        "Recipient Address": "<Hal Finney’s address>",                                    // Address of Hal Finney
        "Value": 10                                                                       // Amount sent
      },
      {
        "Change Address": "<Satoshi’s address>",                                          // Address for change
        "Value": <remaining BTC>                                                          // Leftover BTC minus fees
      }
    ]
  }
]
```

Block 170 represents Bitcoin's first steps toward becoming a transactional system, highlighting its functionality beyond block rewards.

### Significance of Block 170

**1. First Non-Coinbase Transaction:**

The first Bitcoin transaction between two individuals (Satoshi Nakamoto and Hal Finney) is recorded in this block.

**2. Proof of Bitcoin's Use:**

It demonstrates Bitcoin’s ability to send funds between users securely and immutably.

**3. Introduction of Transaction Fees:**

While fees were not significant in this block, this marked the start of Bitcoin’s transaction fee mechanism.

**4. Symbolic Moment:**

Hal Finney received 10 BTC, representing trust in Bitcoin’s potential as a decentralized currency.

## Conclusion

* The original miner created lots of Bitcoins for himself before the block 170!
* Miners were the primary creators of **new wallet addresses** in the early days of Bitcoin. Bitcoin addresses are generated from **public-private key pairs** using cryptographic algorithms.
* The **coinbase transaction** is the first transaction in any block, and it rewards the miner with newly created bitcoins.
  * The reward consists of two components: the **50 BTC Block Reward** and the **Transaction Fees**

In the beginning, **miners** were the primary creators of new wallet addresses because they mined the first blocks, received the newly created Bitcoin, and controlled where the rewards went. They created new addresses as needed to store these rewards. Over time, the Bitcoin network grew, and more users (not just miners) created their own wallet addresses to participate in the Bitcoin economy.

Is there any other ridiculous system where users pay for creating a record in a database? Oh, yes, the banks! But that is different due to the rules and regulations, and they manipulate the markets entirely differently!

Bitcoin (cryptocurrencies) were created as a rebellion but unfortunately they are [ponzi schemes](https://en.wikipedia.org/wiki/Ponzi_scheme) due to their architecture (see **block reward**). You should be able to see it in their database as printed above. It is publicly available unlike the databases of the banks.
