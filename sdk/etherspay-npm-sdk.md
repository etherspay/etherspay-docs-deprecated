# Etherspay.js SDK

### Introduction

The Etherspay NPM SDK is used to integrate ERC20 payments for websites.

### Installation

Using NPM:

```makefile
npm install etherspay
```

Using Yarn:

```
yarn add etherspay
```

### Initialize Etherspay.js

{% tabs %}
{% tab title="Javascript" %}
```javascript
import { Etherspay } from 'etherspay';
const etp = new Etherspay({ project_id: '...', project_secret: '...' });
```
{% endtab %}

{% tab title="Typescript" %}
```typescript
import { Etherspay } from 'etherspay';
const etp = new Etherspay({ project_id: '...', project_secret: '...' });
```
{% endtab %}
{% endtabs %}
