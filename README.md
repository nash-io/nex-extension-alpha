<p align="center">
  <img
    src="http://neonexchange.org/img/NEX-logo.svg"
    width="125px;">
</p>

# NEX Extension: Alpha Release (v0.1.0)

A NEO wallet and chrome extension that will allow users to interact with decentralized applications on the blockchain through the world wide web.

**NOTE: Alpha release is for developers only. We will be doing a release for the general public on March 12th.**

## Important

**Developers: do not use keys with funds on mainNet for the Alpha testing. Please only use keys with funds on testNet or CoZNet**

![Alt text](nex_release_image.png 'NEX Release Image')

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

```
Google Chrome Browser
```

### Installing

After cloning or downloading this repo, please open your google chrome browser and go to the extension page found here:

```
chrome://extensions/
```

Next, click on the Developer mode checkbox in the top bar. You will then click **Load unpacked extensions** and select the **NEXExtension** folder from this repo; this will install the NEX extension for you in developer mode.

You are now ready to create an account, use the extension as a web wallet, and start building your website for users to interact with your dapp through the NEX extension.

## NEX Extension Client

To make it easy to interact with the NEX Extension, we have started the process of creating a client library that you can use to pass messages from your site to the extension. The client library is available as a file located in the **NEXExtensionClient** folder included with this repo. This early version of the client has the following 2 methods, which may be called as described below:

```
const nexExtApi = new NEXExtensionClient()

// Start a transaction
nexExtApi.startTx({
  amount: '1.5',
  symbol: 'GAS',
  toAddr: 'AWmzT3dqJDTucBmv4X7TXNsbqQMioMGt6L'
})

// Open receive modal
nexExtApi.openReceive()
```
