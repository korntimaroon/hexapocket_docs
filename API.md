# Hexa Pocket API

## API Description 

In this document will avaabile in a version of Hexa Pocket [Beta 2.0]

## Hexa Pocket Connection


### Connect to the wallet

```javascript
//to connect
gethexapocketconnect();
//to disconnect
gethexapocketdisconnect();
```


### Wallet Information

```javascript
console.log(account.hexa_account)
//It will output all store account in JSON formats

console.log(account.hexa_account[i])
//It will output the current opened account in JSON formats

console.log(network.hexa_network)
//It will output the current network that the user use

console.log(token.chain[i].hexa_token)
//It will output the current chain token that the user added)
```
