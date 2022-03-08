# hexapocket_docs

## Hexa Source Document

### User Security

User Account key convert to SHA-256 then will convert to the QR-code, when Hexa Pocket platform scan it will convert back from QR-code to SHA-256 and SHA-256 will turn to the JSON form.

> Example of User Account Key

```json
[{"hexa_id": 1,"hexa_name": "Korn", "hexa_middle_name": null, "hexa_last_name": "Timaroon","hexa_key": "9iuwhe2uio1kj"}]
```
> Example of SHA-256 (Data from above code)

```
EEA72F116AE750A0D6D7BE6DBFE62C57665EE220EBFB27FF59892D152866A7ED
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


