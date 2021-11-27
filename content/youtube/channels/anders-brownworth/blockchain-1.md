---
title: "Blockchain 101 - a visual demo"
---

[00:00:22](https://www.youtube.com/watch?v=_160oMzblY8&t=22)

hashing explained

[00:02:08](https://www.youtube.com/watch?v=_160oMzblY8&t=128)

same hash for same data, different hash for different data

[00:02:20](https://www.youtube.com/watch?v=_160oMzblY8&t=140)

block - extending hash idea

[00:02:26](https://www.youtube.com/watch?v=_160oMzblY8&t=146)

data will contain more sections, block number, nonce and data

[00:03:04](https://www.youtube.com/watch?v=_160oMzblY8&t=184)

hash is calculated from all of this data
we will claim that hash is signed if it has some specific pattern, like 0000 at the beginning

[00:03:55](https://www.youtube.com/watch?v=_160oMzblY8&t=235)

nonce- just a number, that we set, so that block will be signed, will have 0000 at the beginning of hash, searching or generating such a number is called mining

[00:05:23](https://www.youtube.com/watch?v=_160oMzblY8&t=323)

blockchain is a chain of blocks, where blocks are block explained from previous, but in the data section it also contains hash of the previous block in the chain

[00:06:53](https://www.youtube.com/watch?v=_160oMzblY8&t=413)

changing data in some block breaks all the following blocks, which means they need to be mined again, more block to mine, more time it takes

[00:07:14](https://www.youtube.com/watch?v=_160oMzblY8&t=434)

so changing the history is difficult and expensive

[00:08:55](https://www.youtube.com/watch?v=_160oMzblY8&t=535)

this is how blockchain is going to resist mutation/change

[00:09:33](https://www.youtube.com/watch?v=_160oMzblY8&t=573)

distributed blockchain - it's the same block chain but on more devices/peerws

[00:10:02](https://www.youtube.com/watch?v=_160oMzblY8&t=602)

if we want to change something on the blockchain, it need to be changed on all devices

[00:10:55](https://www.youtube.com/watch?v=_160oMzblY8&t=655)

if block chain has be maliciously changed, we can tell just by looking at hashes, because when content changes, hashes changes, and they will be different than on other peers, the right one is declared by most peers

[00:12:07](https://www.youtube.com/watch?v=_160oMzblY8&t=727)

just look at the last block hash to compare right vs wrong block chain

[00:12:41](https://www.youtube.com/watch?v=_160oMzblY8&t=761)

token - block which contains same meaningful data in block, e.g. transactions

[00:13:11](https://www.youtube.com/watch?v=_160oMzblY8&t=791)

now we can't change what transaction amount in the past, because the mining time will be a lot and other right chains will not believe it, because last hash is different

[00:14:19](https://www.youtube.com/watch?v=_160oMzblY8&t=859)

we are not remembering account balance, only money movements

[00:14:33](https://www.youtube.com/watch?v=_160oMzblY8&t=873)

in this version of blockchain, we don't know who had how much at the beginning

[00:14:41](https://www.youtube.com/watch?v=_160oMzblY8&t=881)

coinbase transactions - will tell how much money had been added to each account, this information will be stored in blocks as well

[00:15:25](https://www.youtube.com/watch?v=_160oMzblY8&t=925)

now we can calculate and verify, if transaction can happen and who has how much money in their account

[00:17:17](https://www.youtube.com/watch?v=_160oMzblY8&t=1037)

efficient way to handle agreement of what happened in the past

[00:17:23](https://www.youtube.com/watch?v=_160oMzblY8&t=1043)

immutable history

[source](https://www.youtube.com/watch?v=_160oMzblY8)
