
## Distilling the Blockchain



Blockchain technologies enable parties who don’t know one another to have a relationship based on trust, accountability and transparency. Whereas government regulations, industry endorsements and even online reviews help us to assess which service provider to trust, where to eat, or which doctor to choose, distributed ledgers may provide validation for separate entities and erode the need for centralized authorities. As such, the technology may prove the most revolutionary of this still young century. 

This is the first of a series of articles in which I aim to distill some of the fascinating concepts behind blockchain and cryptocurrencies in a form that the lay reader may grasp with interest. This article will explain some of the theory and capabilities of Bitcoin and the blockchain, and further writing will include smart contracts, additional currencies, some of the different consensus mechanisms and innovative approaches that make the field so riveting.

Most people became aware of the first cryptocurrency, Bitcoin, before they heard of blockchain. The Bitcoin paper published in 2008 by Satoshi Nakamoto, a pseudonym for an anonymous person (or persons), runs on the blockchain. No matter what the fate and trajectory of the currency, it is the blockchain that likely be its most enduring legacy. An awareness of how the technology works, its requirements and suitability for a variety of usages is essential for software developers, business leaders, consultants, and people in any industry or profession who may like to consider how the technology may improve systems for the benefit of all.

To give a whirlwind history of computing, large mainframes capable of resource-intensive work such as large databases and cryptography, were centralized. Supercomputers occupied entire labs at universities, a few private companies, and government entities such as NASA. The proliferation of personal computing led to the ‘client-server’ model, where relational databases based on distributed architecture fed data to users’ computer screens. This is how companies such as Google and Facebook operate, with data centers spread geographically, sharing their and workload feeding users’ client requests all over the world.

At the heart of the blockchain are decentralized systems, with no single point of failure or ownership of the data. It 
enables a distributed ledger, where the data resides across devices, with nodes spread across geographical regions and working together to keep the ledger up to date. In this fashion, an American logistics company can send a Siberian truck driver payment by Bitcoin, and the shared ledger is updated and available for all to see. 
Distributed ledgers mean we can do much more than send transactions to one another, however. They enable smart contracts, peer-to-peer networks, sharing of computation power, and more besides. I aim to expand on these capabilities in further articles.





![alt text](files/images\blockchain1.PNG "Distributed ledger")


A crucial part of the technology is the consensus mechanism, part of the protocol in the diagram. This allows participants to synchronize the same block data and prevents fraudulent attacks which may aim to inject transactions into the chain where no value has changed hands. Before we look at some of the popular methods for achieving consensus, let’s first go over what we mean by a ‘block’.

A block is a set of transactions bundled together and added to the chain at the same time. In the case of Bitcoin, ‘miners’ bundle confirmed and unconfirmed transactions together. They then use extensive computing power in a race to solve cryptographic challenges and propose this grouping of confirmed and unconfirmed transactions as the next entirely valid block to be added to the chain. 

The miner, or pool of miners working together, that wins this race is rewarded a fee for contributing to the network. Each block is marked with a timestamp, a cryptographic hash, and is now part of the public ledger. You can see the latest blocks for Bitcoin here - https://blockchain.info 

This is known as the ‘proof of work’ consensus mechanism. The following diagram shows how the blocks and hashes combine to form a chronological record of transactions. The chain is generally irrevocable, since to go back in time and rewrite the chain would be unthinkably computationally expensive. The binary hash tree, known as a merkle tree, for the transactions to be included.


![alt text](files/images\blockchain2.PNG "Merkle tree")
tx = transaction


The transaction root for block 8 becomes the previous hash (‘prev_hash’) of block 9, which is then carried to block 10. Incoming hashes from transactions 0, 1, 2, 3, become the root of those blocks. Were a malicious actor to attempts to inject a fraudulent transaction at say, tx 0, the record would show up the tree since hash 0 and Hash 01 wouldn’t be correct. 
In this fashion the entire blockchain becomes one single source of truth.  The real-time knowledge and immutability of data has massive implications for an array of industries. Imagine a chain of restaurants that could accurately predict what fresh food they had available at every location in real-time. Or that while travelling to another state or country you need immediate access to your encrypted, anonymized health records on seeing a new doctor. The technology’s scope reaches far beyond digital currency. 


### Limitations



The ‘proof-of-work’ model is difficult to do efficiently at scale. In the case of Bitcoin, the computation power necessary to solve the cryptographic riddles necessary to process the blocks, and update and synchronize an ever-growing blockchain means Bitcoin accounts for 0.21 percent [worldwide electricity consumption](https://digiconomist.net/bitcoin-energy-consumption).
It also suffers from a lack of efficiency, with slow transaction times, and high fees. In December 2017, the highest average transaction fee reached [$55](https://bitinfocharts.com/comparison/bitcoin-transactionfees.html#3m).


### Proof of stake


‘Proof-of-stake’ is a potential rescue. This method requires network participants to stake significant amounts of a currency to help validate incoming transactions. Ethereum, the second largest cryptocurrency (and also smart contract platform) after Bitcoin by market cap, is switching from proof-of-work to this consensus technique. Those running nodes and ‘staking’ currency are selected at random to validate incoming transactions, and participants with higher amounts of the currency are more likely to be picked to complete the task and receive rewards. 

There are other methods besides. ‘Proof-of-elapsed-time’ comes from Intel and is a hybrid algorithm of a random lottery and first-come-first-served. Validators participating in the network request a wait time and the peer with the shortest wait time for a particular transaction grouping is elected the leader charged with validating that block. This is yet a young method among blockchain technologies, however its efficiency at scale and fairness may bring increased popularity.
There are other methods besides these, and I hope to write about a new and exciting method known as the 'tangle' in future posts. 


### A brief words on smart contracts


A further progression came from the Ethereum currency and the smart contracts it offers on its Ethereum Virtual Machine (EVM). If Bitcoin allows parties to send one another currency, Ethereum allows a party to schedule a payment once a condition is met, so Alice can send Bob some funds once Bob makes good on his promise to wash her car. As with transactions, so too are these added to the blockchain. In this way, all parties to the contract have a public record, which can be very different to typical systems whereby authenticated details rarely go beyond buyer and seller.

Since the original internet protocols don’t include a means of encrypting identity, we have a fragmented internet where our personal data and contacts maybe held by Facebook or Microsoft, our photos by Google, vacation arrangements on Expedia, and all require logins and passwords. Ethereum is the first of now several projects that may even lead the charge towards not only smart contracts and digital currency, but a new internet. We’ll go deeper into smart contracts in a separate article. 


### What does this mean for our clients?


For clients interested in blockchain technology, a good starting point may be to ask about their business needs. There may be scope for leveraging a distributed ledger to help them increase efficiency, avoid third party fees, and make their systems more secure and accurate. Some questions worth asking:
What might be the size of the network (number of nodes)?

How geographically distributed could those nodes be?

(Companies without geographic reach or capacity could use external services (e.g. IBM or Hyperledger) rather than build their own).

What kind of data and in what amounts do you have? 

(Constantly synching enormous amounts of data to a chain can be computationally costly).

Would immutable data records be worthwhile for your data?

(If their data is largely ‘static’, which means it doesn’t need to be updated often, they may not benefit). 


### To sum up

Blockchain is a broad and fascinating field which lies at the intersection of mathematics (cryptography), computer science (the implementation) and may greatly improve and impact industry, finance, government and civics. We'll dive deeper into the technology and further use cases in subsequent posts. 
