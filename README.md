# Merkle Tree Gift List 🎁

Blockchains have a storage problems because they require that nodes in the network store every value recorded in their shared database. 

For Ethereum this means all account balances, as well as every persistent variable on a smart contract.

There is a need to be careful how much data we are storing on the blockchain with one thing in mind:

#### The less data we store, the cheaper it will be.
 
### Key Learnings

Merkle Trees

Merkle Trees in Blockchains

Ethereum tries




### Step to reproduce

1. run server - 'node server/index'

2. run client - 'node client/index'

3. Check project structure below.

4. Change name variable in client script according to names in niceList.json file.

### Project structure 

#### Client

Think of the client as the _prover_ here. It needs to prove to the server that some `name` is in the `MERKLE_ROOT` on the server. 

#### Server

Think of the server as the _verifier_ here. It needs to verify that the `name` passed by the client is in the `MERKLE_ROOT`. If it is, then we can send the gift! 

#### Utils

There are a few files in utils:

- The `niceList.json` - contains all the names of the people who deserve a gift this year,randomly generated.
- The `example.js` script shows how to generate a root, generate a proof and verify that some value is in the root using the proof.
- The `MerkleTree.js` -- Merkle Tree implementation !
- The `verifyProof.js` - function to prove a name is in the merkle root, as show in the example.
