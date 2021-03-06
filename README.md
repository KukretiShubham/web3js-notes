# web3js-notes
These are for quick reference. For hands on practice, checkout cryptozombies [tutorial](https://cryptozombies.io/)

For Web3js official [Documentation](https://web3js.readthedocs.io/)

## What is Web3.js?
Remember, the Ethereum network is made up of nodes, with each containing a copy of the blockchain. When you want to call a function on a smart contract, you need to query one of these nodes and tell it:

The address of the smart contract
The function you want to call, and
The variables you want to pass to that function.

Ethereum nodes only speak a language called `JSON-RPC`, which isn't very human-readable. A query to tell the node you want to call a function on a contract looks something like this:
```javascript
// Yeah... Good luck writing all your function calls this way!
// Scroll right ==>
{"jsonrpc":"2.0","method":"eth_sendTransaction","params":[{"from":"0xb60e8dd61c5d32be8058bb8eb970870f07233155","to":"0xd46e8dd67c5d32be8058bb8eb970870f07244567","gas":"0x76c0","gasPrice":"0x9184e72a000","value":"0x9184e72a","data":"0xd46e8dd67c5d32be8d46e8dd67c5d32be8058bb8eb970870f072445675058bb8eb970870f072445675"}],"id":1}
```
Luckily, Web3.js hides these nasty queries below the surface, so you only need to interact with a convenient and easily readable JavaScript interface.
