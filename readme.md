# vancrypt: [VAN]illa (js) En[CRYPT]ion in the Browser 🔋

## Description
Vancrypt is a lightweight encryption library for client-side JavaScript applications. It uses the Web Crypto API to provide secure encryption without relying on external dependencies. This ensures that data is encrypted in the browser before being sent, enhancing security by making it harder to intercept sensitive data. Vancrypt is compatible with ES5, ES6, and TypeScript, making it a versatile choice for any project.

## Features
- **Secure Encryption**: Uses the Web Crypto API for robust encryption.
- **No External Dependencies**: Lightweight and easy to integrate.
- **Wide Compatibility**: Works with ES5, ES6, and TypeScript.

## Installation
Simply include the Vancrypt script in your project or import it as a module.

## Usage

### ES6+
```js
import { generateUUID, generateEncKeyAndIv, encrypt } from './vancrypt/bin/main';
```


### ES5
```html
<script src="https://raw.githubusercontent.com/dchahla/vancrypt/bin/main"></script>
<script>
  const Vancrypt = window.Vancrypt;

  const keys = Vancrypt.generateEncKeyAndIv();
  console.log('ENC_KEY:', keys.ENC_KEY);
  console.log('IV:', keys.IV);

  const data = 'your-data-here';
  Vancrypt.encrypt(data, keys.ENC_KEY, keys.IV).then(function(result) {
    console.log('Encrypted Token:', result.encrypted);
    console.log('IV:', result.iv);
  });
</script>
