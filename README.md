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

##### Export your account (Normal Plan)

> To export your account whether you change your browser or change your device you could go to the Exportation Menu in setting and click export your account to a hexa json format and throw the file in your new browser or device added account in Hexa Pocket Website account management page because if you are using normal plan the account will not be save if you are changing your device or browser

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


