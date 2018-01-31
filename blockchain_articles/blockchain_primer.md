Back to [contents](../)

## Distilling the Blockchain

[//]: # (Image References)

[image1]: images/blockchain1.PNG "Distributed ledger"
[image2]: images/blockchain2.PNG "Merkle tree"

A key tenant of cryptography is that anything that uses a centralized entity to carry out a function can be done without the intermediary. This is the basis for blockchain technologies, where people can transact or agree on and execute contracts without the need for a third party.
In this first of a series of articles, I aim to explain the theory and practices involved in what may be one of the most revolutionary technologies of our time. Whereas the various whitepapers of cryptocurrencies and smart contract platforms can be dense and presuppose a degree of technical experience, I hope to distill complex concepts for anyone to understand. 
Many people may have first heard of Bitcoin before they did blockchain. Bitcoin is a digital currency which is transacted on and validated by a blockchain. It enables people around the world to send funds without an intermediary such as a bank. The underlying technology may be the enduring legacy of the currency, since its potential goes far beyond simply a method for transactions. 

### Broad strokes

At the heart of the blockchain is a distributed ledger. Imagine a plumber who keeps a ledger of orders, client information, payments, work due and work completed. To keep the clients informed, once a week the plumber sends them a summary of the parts of the ledger that concerns them, including what work they have ongoing, and what payments they may have made or may be due. Updating the ledger and sharing it takes time, and the clients may not always have the most up to date information. They also have to trust the plumber is sending accurate information, and hope that the ledger mirrors their own records of how much they paid to have work done. 

Now imagine that the ledger the plumber keeps updates constantly, in real time. It shows the exact materials available in the van, the warehouse, the state of client work and a record of client payments. The ledger cannot be doctored retroactively. It shows whether work was completed on time, and how often it went over budget. 

The same is true of the ledgers held by clients. They can see all this in real time, and they can also see all records of payment, as well as work done. The ledger is written in such a fashion that while they can see details of the plumbing jobs and payments, the information is anonymized so that private information such as names and addresses aren’t available. 
The ledger can also be seen not only by the plumber and clients but everyone with an interest. This means people looking for a reliable plumber can look at the ledger, gauge how reliable they may be, and what their prices are like – both initial quotes and whether clients got a surprise upon completion! 

This is a distributed ledger. It has no central ownership, so we call it ‘decentralized’. It cannot be doctored retroactively, so we call the data on the ledger ‘immutable’. Such a ledger isn’t held on one server, but on many different servers, usually spread geographically, so there is no single point of failure.

### A whirlwind history of computing

Powerful computers over the past 50 years were largely centralized. They occupied entire rooms and floors of corporations such as IBM, university labs and government entities such as NASA. Personal computers and private networks then brought an era of ‘client-server’ technology, supported by relational database systems. A user on a laptop is the ‘client’, and the service loading their favorite television show from the cloud onto their screen is the ‘server’. The proliferation of data as communication, work and leisure have moved online has led companies such as Google and Facebook to store massive amounts of data at centers dispersed geographically. These data centers work ‘relationally’ and share the load of users requesting data all over the world. 

### Decentralization

Though the hardware in these cases is decentralized in the sense it may be spread geographically, the applications (Facebook, Twitter etc) are centralized. Decentralization in computing means that the end user at their laptop can not only access their data but they still control the asset, thus removing any need for third parties.

### Finer points of a decentralized ledger

According to the Linux Foundation, distributed ledger technology (DLT) generally consists of three components: a data model to capture the real-time state of the ledger; a language of transactions that change the ledger state, and a protocol which builds consensus among participants that transactions took place, and in a certain order.

![alt text][image1]


It can be illustrative to use Bitcoin as an example. Bitcoin is sustained by distributed computers which operate as ‘nodes’ on the network. Though Bitcoin requires massive computing power beyond the hope of a laptop, some more recent cryptocurrencies and blockchain projects are designed so it’s less costly to operate a ‘node’. Why do people leave their computers on all night and increase their electricity bill to help sustain the network? Participants generally receive rewards, paid in the cryptocurrency or ‘tokens’ of the project they are helping support. 
Back to Bitcoin. The blockchain is constantly updated, and there is a consensus protocol among network participants to have the majority agree that valid transactions took place and in a certain order. There are different methods for achieving this, and we’ll go into some of the main theories below. Bitcoin uses an approach called ‘proof-of-work’.
Proof-of-work involves nodes, also called ‘miners’ because they ‘mine’ bitcoins, which compete to solve cryptographic puzzles and add transactions to the blockchain. We can dive deeper into proof-of-work by examining what we mean by a ‘block’.
Miners bundle confirmed and unconfirmed transactions together into a ‘block’. They then use extensive computing power in a race against among other miners (or ‘mining pools’ of participants working together) to solve cryptographic challenges and propose this group of transactions as the next validated block to be added to the blockchain. The winning miner or mining pool then receives a fee in Bitcoin for solving the challenge. These blocks then become part of the immutable record of transactions and are publicly available here.
The following diagram shows some of the computer science concepts employed here. The binary hash tree, also known as a Merkle tree, is a data structure which allows cryptographic hashes of its ‘leaves’ to keep immutable records as data is added to the ‘tree’.


![alt text][image2]
tx = transaction

If this seems complex, the topic is even fraught with difficulties for computer scientists. The main takeaway is that incoming transactions are added to an immutable record. The transaction root for block 8 becomes the previous hash (‘prev_hash’) of block 9, which is then carried to block 10. Incoming hashes from transactions 0, 1, 2, 3, become the root of those blocks. Were a malicious actor to attempts to inject a fraudulent transaction at say, tx 0, the record would show up the tree since hash 0 and Hash 01 wouldn’t be correct. In this fashion the entire blockchain becomes one single source of truth. 
The real-time knowledge and immutability of data has massive implications for an array of industries. Imagine a chain of restaurants that could accurately predict what fresh food they had available at every location in real-time. Or that while travelling to another state or country you need immediate access to your encrypted, anonymized health records on seeing a new doctor. The technology’s scope reaches far beyond digital currency.

### Scalability

This consensus mechanism is an essential part of validating the transactions to ensure transparency and avoid fraudulent attacks. As the blockchain grows with transactions added daily, it can become enormously costly to maintain, and therefore difficult to scale to more users. 
Bitcoin now accounts for 0.21 percent of [electricity consumption worldwide](https://digiconomist.net/bitcoin-energy-consumption).
It also suffers from a lack of efficiency, with slow transaction times, and high fees. In December 2017, average transaction fees reached a high of [$55](https://bitinfocharts.com/comparison/bitcoin-transactionfees.html#3m).
Mining power is heavily concentrated for Bitcoin, which threatens its decentralization and could even make the network susceptible to what is known as a ‘51% attack’ – a reference to the fact that if more than half of network participants agreed to write fraudulent transactions to the chain, they may be able to do so.

### Proof-of-stake

‘Proof-of-stake’ is a potential rescue. This consensus protocol requires network participants to stake significant amounts of a cryptocurrency to help validate incoming transactions. Ethereum, the second largest cryptocurrency by market cap (and also smart contract platform, more on this later), is switching from proof-of-work to this technique. Those running nodes and ‘staking’ currency are selected at random to validate incoming transactions, and participants with higher amounts of the currency are more likely to be picked to complete the task and receive rewards.

### Proof-of-elapsed-time

There are other methods besides. ‘Proof-of-elapsed-time’ comes from Intel and is a hybrid algorithm of a random lottery and first-come-first-served. Validators participating in the network request a wait time and the peer with the shortest wait time for a particular transaction grouping is elected the leader charged with validating that block. This is yet a young method among blockchain technologies, however its efficiency at scale and fairness may bring increased popularity. There are other methods besides these, and I hope to write about a new and exciting method known as the 'tangle' in future posts.

### Smart contracts

A further progression came from the Ethereum currency and the smart contracts it offers on its Ethereum Virtual Machine (EVM). If Bitcoin allows parties to send one another currency, Ethereum allows a party to schedule a payment once a condition is met, so Alice can send Bob some funds once Bob makes good on his promise to wash her car. As with transactions, so too are these added to the blockchain. In this way, all parties to the contract have a public record, which can be very different to typical systems whereby authenticated details rarely go beyond buyer and seller.

Since the original internet protocols don’t include a means of encrypting identity, we have a fragmented internet where our personal data and contacts maybe held by Facebook or Microsoft, our photos by Google, vacation arrangements on Expedia, and all require logins and passwords. Ethereum is the first of now several projects that may even lead the charge towards not only smart contracts and digital currency, but a new, decentralized internet. We’ll go deeper into smart contracts in a separate article.

### What does this mean for clients?

For clients interested in blockchain technology, a good starting point may be to ask about their business needs. There may be scope for leveraging a distributed ledger to help them increase efficiency, avoid third party fees, and make their systems more secure and accurate. Some questions worth asking: What might be the size of the network (number of nodes)?

How geographically distributed could those nodes be?

(Companies without geographic reach or capacity could use external services (e.g. IBM or Hyperledger) rather than build their own).

What kind of data and in what amounts do you have?

(Constantly synching enormous amounts of data to a chain can be computationally costly).

Would immutable data records be worthwhile for your data?

(If their data is largely ‘static’, which means it doesn’t need to be updated often, they may not benefit).

### In summary

Blockchain is a broad and fascinating field which lies at the intersection of mathematics (cryptography), computer science (the implementation) and may greatly improve and impact industry, finance, government and civics. We'll dive deeper into the technology and further use cases in subsequent posts.

#### Sources

Nakamoto's Bitcoin paper: <https://bitcoin.org/bitcoin.pdf>
Ethereum: <https://ethereum.org/>
With thanks to the Linux Foundations's excellent Hyperledger course on edX:
<https://www.edx.org/course/blockchain-business-introduction-linuxfoundationx-lfs171x>
