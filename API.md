# Hexa Pocket API

## API Description 

In this document will avaabile from the version of Hexa Pocket [Beta 2.0.0] [https://www.hexapocket.com]

## Hexa Pocket Connection


### Connect to the wallet

```javascript
//to connect
gethexapocketconnect(hexajsonformat);
//to disconnect
gethexapocketdisconnect(hexajsonformat);
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

### Add Token or Network

```javascript
insertnetworktohexapocket(hexajsonformat);
inserttokentohexapocket(hexajsonformat);
```

### Transaction

```javascript
hexa_pocket.gettokenbalance(token_address, chain_id, wallet_id,token_symbol)
hexa_pocket.getnetworkbalance(chain_id, wallet_id)
hexa_pocket.getswaptoken(from_token_address,to_token_address,account,network_id,amount)
hexa_pocket.senttoken(token_address,from_account,to_account,network_id,amount)
```

### Check Balance 

```javascript
hexa_pocket.getbalanceinethereum(account);
```

### Generating Account

```javascript
console.log(hexa_pocket.generateaccount("key","pass");
```
