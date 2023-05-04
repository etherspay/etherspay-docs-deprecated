---
description: >-
  This page provides detailed information about Etherspay's billing system,
  including its features, benefits, and how it works.
---

# Billing

Billing is a critical aspect of any financial service, and Etherspay is no exception. Our billing system is designed to provide users with a seamless and transparent experience, ensuring that they are always aware of the fees associated with our services. We understand that transparency and fairness are essential components of any successful financial service, and our billing system is designed with these principles in mind.

&#x20;

#### Problem

Web3 blockchains were designed with the principle of decentralization, which means that users have complete control over their wallets and assets. This design ensures that no third party can access or manipulate a user's funds without their consent.

However, this design also means that recurring payments or subscriptions on Ethereum are not possible. This is because other people cannot transfer money from a user's wallet without their explicit approval. Subscriptions require an automatic transfer of funds at predetermined intervals, which is not possible without the user's direct involvement.

Therefore, while Ethereum and other Web3 blockchains enable a wide range of financial activities, including secure and transparent transactions, they are not suitable for recurring payments or subscriptions.

&#x20;

#### Solution

Etherspay has developed smart contracts to address the problem of recurring payments on Web3 blockchains. The company has made opt-out subscriptions possible, enabling subscribers to make preauthorized, recurring payments to a merchant at predetermined intervals.

The smart contracts define a contract interface that allows subscribers and merchants to initiate, approve, and manage subscriptions. Subscribers can create subscriptions with a specified start date, and can cancel them at any time. Merchants can also create, approve, and cancel subscriptions.

This standard provides basic functionality to enable secure and transparent transactions between subscribers and merchants. It supports ERC-20 token, which is a widely used digital currency standard on the Ethereum network.

Recurring payments are a prevalent use case in the internet sector, and this standard offers a straightforward, secure, and scalable solution for implementing recurring payments, using Web3.

&#x20;

#### Abstract

A standard interface for preauthorized, recurring subscription payments.

This standard defines a contract interface enabling subscribers to make recurring payments to a merchant, and for the contract to then make this payment on behalf of the subscriber at the predetermined interval.

This standard provides basic functionality to initiate, approve, and manage subscriptions between a subscriber and merchant. These subscriptions allow a merchant to transfer a pre-authorized amount of ERC-20 tokens within each recurring time interval.



#### Motivation

Recurring payments are a prevalent use case across the internet sector. This standard offers a straightforward, secure, and scalable solution for implementing recurring payments, using Web3.

&#x20;

#### Features

·        Subscriptions can be created, approved, and cancelled by either the subscriber or merchant.

·        Subscriptions can be created with a specified start date, and can be cancelled at any time.

·        ERC-20 Token support.

&#x20;

#### References

·        \[ERC-20]            ([https://eips.ethereum.org/EIPS/eip-20](https://eips.ethereum.org/EIPS/eip-20))

·        \[ERC-948]          ([https://github.com/sb777/erc-948-draft/issues/1](https://github.com/sb777/erc-948-draft/issues/1))
