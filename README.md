# hexapocket_docs

# Connect to Hexa Pocket Wallet

## Connection Button (UI)

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
## Javascript Code (React, Next)

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

# Use Hexa Pocket Quickswap API

## Sent Money



