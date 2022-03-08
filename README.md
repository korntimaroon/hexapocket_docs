# hexapocket_docs

## Hexa Source Document

### User Security

> User Account key convert to SHA-256

> Example User Account Key

```json
[
   {"hexa_id": 1,"hexa_name": Korn, "hexa_middle_name": null, "hexa_last_name": "Timaroon","hexa_key": "9iuwhe2uio1kj"},
]
```





## Connect to Hexa Pocket Wallet (Use - Hexa)

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


