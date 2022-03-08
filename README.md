# hexapocket_docs

## Hexa Source Document

### User Security

User Account key convert to SHA-1 while signup then will convert to the QR-code, when Hexa Pocket platform scan it will convert back from QR-code to SHA-1 then Hexa Pocket will compare to the database whether is correct or not

> Example of User Account Key

```json
[{"hexa_id": 1,"hexa_name": "Korn", "hexa_middle_name": null, "hexa_last_name": "Timaroon","hexa_key": "9iuwhe2uio1kj"}]
```
> Example of SHA-1 (Data from above code)

```
b1fa9375fd8c508442628ebd8b7e161ce810ed42
```


### Comparing Plan

#### Normal Plan

Normal Plan can hold your account up to about 150, Depends on the browser can hold in the local storage. User account including ID and SHA-1 form with your account will store in the local storage of your browser. The non support local storage such as Safari would not support this Hexa Pocket wallet plan.





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


