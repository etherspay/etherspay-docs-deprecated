# Etherspay NPM SDK

### Introduction

The Etherspay NPM SDK is used to integrate ERC20 payments for websites.

### Installation

Using NPM:

```makefile
npm install etherspay-sdk
```

Using Yarn:

```
yarn add etherspay-sdk
```

### Usage

{% tabs %}
{% tab title="Javascript" %}
```javascript
import { etherspay } from 'etherspay';
const etp = new etherspay('your_api_key_here');

etp.bsc.createInvoice('0x05f2h78', 5000);
```
{% endtab %}

{% tab title="Typescript" %}
```typescript
const etherspay = require('etherspay');
```
{% endtab %}
{% endtabs %}
