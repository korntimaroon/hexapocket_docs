# hexapocket_docs

## Hexa Source Document

### User Security



#### Storing and Backup (User Database)

User Account key convert to SHA-1 while signup then will convert to the QR-code, when Hexa Pocket platform scan it will convert back from QR-code to SHA-1 then Hexa Pocket will compare to the database whether is correct or not

> Example of User Account Key

```json
[{"hexa_id": 1,"hexa_name": "Korn", "hexa_middle_name": null, "hexa_last_name": "Timaroon","hexa_key": "9iuwhe2uio1kj"}]
```
> Example of SHA-1 (Data from above code)

```
b1fa9375fd8c508442628ebd8b7e161ce810ed42
```

#### The Database

All of Hexa Pocket data is store in Postgresql 

>User Database Storing Example (Normal Plan)

| hexa_id | hexa_fullname | hexa_user_name | hexa_middle_name | hexa_last_name | fist_account | password | last_active | additional_data |
|---------|---------------|----------------|------------------|----------------|--------------|----------|-------------|-----------------|
|1|Korn|null|korntimaroon|Timaroon|[{}]|password|12/12/12|<span style="color:red">null</span>|

>Account Wallet Database (Cloud Plan)

| hexa_id | account_public_key | hexa_user_name | account_private_key | additional_data |
|---------|---------------|----------------|------------------|----------------|
|1|0xdkuiiu2jjoe938u3uw9qi|korntimaroon|sndu3i2jewu8ijuiekjfui|null|

#### Plugin Chain and Coin

List of Plugin Chain and Provider

- Hexa Pocket will use Hexa Chain List API to store all of the information of all networks.

> Mainnet

| Chain Name | Chain ID | Chain Currency|
|------------|----------|---------------|
| Ethereum Mainnet | 1 | ETH|
| Binance Smart Chain Mainnet | 56 | BNB |
| Polygon Mainnet | 137 | MATIC |

> Testnet

| Chain Name | Chain ID | Chain Currency|
|------------|----------|---------------|
| Ropsten Test Network | 3 | ETH |
| Kovan Test Network | 43 | ETH |
| Rinkerby Test Network | 4 | ETH |
| Goerli Test Network | 5 | ETH |

> Mainnet Web3js Provider List

```javascript
const Web3 = require('web3');
// BSC Mainnet
const web3 = new Web3('https://bsc-dataseed1.binance.org:443');
// Ethereum Mainnet
const web3 = new Web3('https://api.mycryptoapi.com/eth')
// Polygon Mainnet
const web3 = new Web3('https://rpc-mainnet.maticvigil.com/')

```

The Plugin network will store in Hexa Pocket API in JSON format.

> Example

```json
[{"network": "Ethereum Mainnet", "network_id": "1", "rpc_url": "https://api.mycryptoapi.com/eth","currency_symbol": "ETH","block_url":"https://etherscan.io"}]
```





> Source

- https://docs.binance.org/smart-chain/developer/BEP20.html
- https://hexa-chainlist.com/
- https://chainlist.org/
- https://replit.com/@KornTimaroon/FragrantPotableSoftwareagent#index.js
- https://www.google.com/search?q=ethereum+wallet+dashboard+ui&tbm=isch&ved=2ahUKEwjQ7rXhkLv2AhUKXWwGHZuWDHoQ2-cCegQIABAA&oq=ethereum+wallet+dashboard+ui&gs_lcp=CgNpbWcQA1DMBFj9DmDcEGgAcAB4AIABVogB0ASSAQE4mAEAoAEBqgELZ3dzLXdpei1pbWfAAQE&sclient=img&ei=frcpYtC3PIq6seMPm62y0Ac&bih=1001&biw=1920&rlz=1C5CHFA_enTH944TH944#imgrc=zTzn_vsY0XMBqM
- https://www.google.com/search?q=ethereum+wallet+dashboard+ui&tbm=isch&ved=2ahUKEwjQ7rXhkLv2AhUKXWwGHZuWDHoQ2-cCegQIABAA&oq=ethereum+wallet+dashboard+ui&gs_lcp=CgNpbWcQA1DMBFj9DmDcEGgAcAB4AIABVogB0ASSAQE4mAEAoAEBqgELZ3dzLXdpei1pbWfAAQE&sclient=img&ei=frcpYtC3PIq6seMPm62y0Ac&bih=1001&biw=1920&rlz=1C5CHFA_enTH944TH944#imgrc=IYiIjzP-XLTHTM&imgdii=vnjm-gk8uMLofM
- https://replit.com/@KornTimaroon/ImperfectImmediateDrivers#index.js:1:4
- https://replit.com/@KornTimaroon/EcstaticTrustworthyProcessors#index.js
#### The token list JSON format

> Example Token Store In JSON Format

```json
[{"token_name": "USDC","token_deci": 18,"token_sym":"BTC","token_con_add": "wsdkjcwqqw2we","token_chain_id": 53}]
```

#### Supported Token Type

| Token Type | Description |
|------------|-------------|
|ERC-20|TS|
|ERC-721|NFT|
|ERC-777|TS|
|ERC-1155|MTS|


#### Page Sitemap
```
Hexa Wallet Advertise Main Floder (ReactJS)
|- Hexa Pocket Home Page
|- Hexa Pocket Download Page
|- Setup Floder |
                | - Login Page
                | - Signup Page
                | - Profile Setup Floder|
                                        | - Setup Profile Page
Hexa Quick Swap Main Floder (NextJS)
| - Quickswap Hexa Floder | 
                          | - Service Quickswap Type  |
                                                      | - Sent Money Page
                                                      | - Chainswap Page
                                                      | - In-chain Swap Page
Hexa Wallet Main Floder (NextJS)
|- Account Management Page
|- Add Account Page
|- Setting Page
|- Account Floder |
                  | - Wallet Page
                  | - Token View Floder |
                                        | - See My Token Page
                                        | - See My Transaction Transaction Page
                                        | - NFT Page
                                      
| - Quickswap Hexa Floder | 
                          | - Service Quickswap Type  |
                                                      | - Sent Money Page
                                                      | - Chainswap Page
                                                      | - In-chain Swap Page
                                                      | - Recieve Money Page && Giftcard Page
                           
| - Notification Floder  |
                         | - Type Trasaction Floder |
                                                    | - Notification Transaction Page
                                                    | - Add Chain Network Page
                                                    | - Add Token Page
                                                    | - Sent Money Page
                                                    | - Swap Chain Page
                                                    | - Swap Money Page
                         | - Type Error and Connection Floder |
                                                              | - Notification Error Page
                                                              | - Connection Page
                         
```
#### Hexa Pocket Browser Support

Hexa Pocket supports all browsers and work in different methods. Such as Google Chrome and Safari, In Google Chrome Hexa Pocket While user opens extension with website in google chromeextension will closes itself as 2 Hexa Pocket windows cannot be opened at the same time. But in safari there is no extension. So when people transact cryptocurrencies, the Hexa Pocken window opens as a safari notification confirming the people to make the transaction.

> Version Browser Supported

<img width="675" alt="image" src="https://user-images.githubusercontent.com/86138908/158092256-37abf2cb-230e-4041-bce3-496dd66f9411.png">


#### Hexa Pocket Secret Phrase Keys (10 Words)

In this feature, Hexa Pocket supports Secret Phrase Key up to 10^145 words as it contains 145 words.

> Example

```
it asset I are wooden asset rocket block person noddle 
```


#### Hexa Pocket Use Network Features

Hexa Pocket has a list of the popular networks you can use if you want. You can add and edit new networks or even your own networks as well.

#### Export your account (Normal Plan)

To export your account whether you change your browser or change your device you could go to the Exportation Menu in setting and click export your account to a hexa json format and throw the file in your new browser or device added account in Hexa Pocket Website account management page because if you are using normal plan the account will not be save if you are changing your device or browser

#### Export your account (Cloud Plan)

In cloud plan you don't need to export anything because all of your data is stored in Hexa Pocket database.

#### Link URL

Hexa Pocket use Nextjs Dynamic Routes which can make your data such as your public key and your dashbord more securely.

> Example of Hexa Pocket Nextjs Dynamic Routes (Open Account)


```
https://hexapocket.com/{$username}/{$id}/{$publickey-account}
```

> Example of Hexa Pocket Nextjs Dynamic Routes (Account-Management Page)


```
https://hexapocket.com/account-manage/{$username}/{$id}
```

#### Sync with Devices

Hexa Pocket will make a JSON type file contain all of your information in account in to a QR-CODE


> JSON file Example

```json
[
  {"chain_num": 1},
  {"chain_num": 2},
  {"chain_num": 3},
  {"chain_num": 4},
],
[
  {"account_public": "0098327yguy3tfeg","account_name": "Ryu Account 1","account_private": "lkjdhgsyuiksdnbhuwidsj", network: {"1": [{"token": 1},{"token": 2}]}},
  {"account_public": "0098327yguy3wstfeg","account_name": "Ryu Account 2","account_private": "lkjdhgsyusdcdikdnbhuwidsj", network: {"1": [{"token": 1},{"token": 2}]}}
]
```

#### Browser Detector

Hexa Pocket will detect the browser every time you enter the website because some of the browser do not support Hexa Pocket such as Safari.

> Browser Detect Code

```javascript
var isOpera = (!!window.opr && !!opr.addons) || !!window.opera || navigator.userAgent.indexOf(' OPR/') >= 0;
var isFirefox = typeof InstallTrigger !== 'undefined'; 
var isSafari = /constructor/i.test(window.HTMLElement) || (function (p) { return p.toString() === "[object SafariRemoteNotification]"; })(!window['safari'] || (typeof safari !== 'undefined' && window['safari'].pushNotification));
var isIE = /*@cc_on!@*/false || !!document.documentMode;
var isEdge = !isIE && !!window.StyleMedia;
var isChrome = !!window.chrome && (!!window.chrome.webstore || !!window.chrome.runtime);
var isEdgeChromium = isChrome && (navigator.userAgent.indexOf("Edg") != -1);
var isBlink = (isChrome || isOpera) && !!window.CSS;
output += 'isFirefox: ' + isFirefox + '<br>';
output += 'isChrome: ' + isChrome + '<br>';
output += 'isSafari: ' + isSafari + '<br>';
output += 'isOpera: ' + isOpera + '<br>';
output += 'isIE: ' + isIE + '<br>';
output += 'isEdge: ' + isEdge + '<br>';
output += 'isEdgeChromium: ' + isEdgeChromium + '<br>';
output += 'isBlink: ' + isBlink + '<br>';
document.body.innerHTML = output;
```

> Output

```
isFirefox: false
isChrome: true
isSafari: false
isOpera: false
isIE: false
isEdge: false
isEdgeChromium: false
isBlink: true
```


### Transaction and Tax

#### Tax

Hexa Pocket will charge you 2% for every transaction in the wallet.





### Comparing Plan

#### Normal Plan

Normal Plan can hold your account up to about 150, Depends on the browser can hold in the local storage. User account including ID and SHA-1 form with your account will store in the local storage of your browser. The non support local storage such as Safari would not support this Hexa Pocket wallet plan. Some of the private user data will store in the Hexa Database.

#### Cloud Plan

Cloud Plan can hold your account up unlimitedly, Depends on what storage you choose. User account including ID and SHA-1 form with your account will store in the Hexa Database.

Price Including:

- 1 GB: 2 USDC per years 
- 2 GB: 3 USDC per years
- 5 GB: 4 USDC per years
- 10 GB: 5 USDC per years


## Use Hexa Connection API





## Connect your Dapps to Hexa Pocket Wallet (Use - Hexa)

### Connection Button (UI)

>Code (HTML)

```html
<button onClick={Click_connect} id="hexa_connect" className="hexa_button">Hexa Pocket</button>
```

>Code (Style)

Include Poppins Font

```css
.hexa_button {
  border-radius:50px;
  font-family: 'Poppins', sans-serif;
  font-weight:bolder;
  background-color: #27257A;
  color:white;
  height:30px;
  width:70px;
}
```
### Javascript Code (React, Next)

>Install Package

```
npm install hexapocket_pack
```

> Connection

```javascript
function Click_connect() {
  hexapocket_pack.getconnectaccount();
}
```

## Use Hexa Pocket Quickswap API

### Sent Money

```javascript
var sent_amount
var sent_account
var sent_public_key
```

### Swap Chain

```javascript
var sent_amount
var sent_account
var sent_public_key
```

### Swap Token between chain

```javascript
var sent_amount
var sent_account
var sent_public_key
```


