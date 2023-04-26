---
description: Explore all of Etherspay here
---

# Welcome!

{% hint style="warning" %}
Etherspay is under development, and not available yet
{% endhint %}

This documentation is designed to provide comprehensive information on how to use Etherspay to accept and process cryptocurrency payments for your project or business.

## Introduction

Etherspay is a secure and reliable platform that enables businesses to accept payments in any [ERC20](https://ethereum.org/en/developers/docs/standards/tokens/erc-20/) crypto token. The project is backed by Web3 technology and supports multiple blockchains.

Throughout this documentation, we will provide detailed information on how to set up and configure your Etherspay account, how to integrate our payment processor into your website or application.



## Whitepaper

Etherspay has a document to explain the technical background, problems, info and more about the project.

{% embed url="https://etherspay.notion.site/Whitepaper-15e3740da9d043a09e724d436dd65668" %}

## Try it out

<details>

<summary>Create a checkout session</summary>

<pre class="language-javascript"><code class="lang-javascript"><strong>
</strong><strong>import Etherspay from "etherspay";
</strong><strong>const etherspay = new Etherspay("#api-key")
</strong><strong>
</strong><strong>const session = await etherspay.checkout.create({
</strong><strong>  success_url: 'https://example.com/success',
</strong>  line_items: [
    {price: '#price-id', quantity: 2},
  ],
  mode: 'payment',
<strong>})
</strong><strong>
</strong><strong>console.log(session.url) // https://buy.etherspay.com/75442486-0878-440c
</strong></code></pre>

</details>

<details>

<summary>Create a product</summary>

<pre class="language-javascript"><code class="lang-javascript"><strong>import Etherspay from "etherspay";
</strong>const etherspay = new Etherspay("#api-key")

const product = await etherspay.products.create({
  name: 'White T-shirt',
});
</code></pre>

</details>

## Browse by service

<table data-view="cards"><thead><tr><th></th><th data-hidden data-card-cover data-type="files"></th></tr></thead><tbody><tr><td>Payments</td><td><a href=".gitbook/assets/IconCrypto.svg">IconCrypto.svg</a></td></tr><tr><td>Balances</td><td><a href=".gitbook/assets/IconReceipt.svg">IconReceipt.svg</a></td></tr><tr><td>Customers</td><td><a href=".gitbook/assets/IconPersons.svg">IconPersons.svg</a></td></tr><tr><td>Products</td><td><a href=".gitbook/assets/IconBox.svg">IconBox.svg</a></td></tr></tbody></table>
