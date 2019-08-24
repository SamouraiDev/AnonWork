# Whirlpool

## Chaumian CoinJoin implementation by the developers of [Samourai Wallet](https://samouraiwallet.com)

Whirlpool is a framework backed up by a collection of software tools that mathematically disassociates the ownership of inputs to outputs in a given bitcoin transaction. This is to increase the privacy of the users involved, protect against financial surveillance, and to increase the fungibility of the Bitcoin network as a whole.

Whirlpool is a fully modular CoinJoin implementation based on a heavily modified fork of the ZeroLink theory. You can [review the theory](THEORY.md) or [review the architecture](ARCHITECTURE.md) in further detail.

**Current Status - PUBLIC BETA**

### What makes Whirlpool different

- **Fast**
  - Focusing on many smaller CoinJoin cycles instead of a single large cycle allows for a theoretical anonymity set that grows exponentially in minutes instead of hours.
  
- **Portable**
  - Modular architecture allows Whirlpool to be embedded anywhere. Our focus on creating a system that can handle the limitations of a mobile environment has created a robust protocol usable under most conditions.
  
- **Usable**
  - Focusing on the spending by enforcing best practices to prevent privacy damaging pitfalls automatically without the user needing to intervene. A simple UX that feels familiar to most users.
  
- **Strong**
  - Structurally built on a strong mathematical foundation. Each Whirlpool cycle:
    - **100%** maximum entropy (10.54 bits)
    - **1496** possible interpretations
    - **Never** any deterministic links between inputs and outputs
    - **Never** cycle with yourself
    - **Never** cycle with UTXOs seen in a previous cycle.

An example of a Whirlpool CoinJoin transaction can be found on [KYCP.org](https://www.kycp.org/#/323df21f0b0756f98336437aa3d2fb87e02b59f1946b714a7b09df04d429dec2/in)
[![](https://samouraiwallet.com/static/public/images/whirlpool/kycp-example.png)]((https://www.kycp.org/#/323df21f0b0756f98336437aa3d2fb87e02b59f1946b714a7b09df04d429dec2/in))

## Using Whirlpool
Whirlpool requires the use of a blinded coordinator server to pass messages between clients. This server doesn't and crucially **cannot** know the contents of the messages it is passing. The following clients have been created and open sourced by the developers of Samourai Wallet and offer unrestricted access to the Samourai operated coordinator server.

**NOTE** - Whirlpool is currently in a **public beta** state. While we are confident in the architecture and the core functionality, it is essential to keep Whirlpool up to date throughout the development cycle. Bug reports and other issues can be relayed to support@samouraiwallet.com

### Windows, OSX, Linux

- An electron/react GUI desktop client is available on Windows, OSX, and most flavors of Linux. You can find binaries for [the most recent release](https://github.com/Samourai-Wallet/whirlpool-gui/releases/latest)
 hosted on the [`whirlpool-gui`](https://github.com/Samourai-Wallet/whirlpool-gui/) repository.

### Mobile

- [Samourai Wallet](https://samouraiwallet.com) [(Android)](https://play.google.com/store/apps/details?id=com.samourai.wallet)

### Developers

- A [REST API](https://github.com/Samourai-Wallet/whirlpool-client-cli/blob/develop/README-API.md) is made available to quickly bootstrap your own applications on top of Whirlpool.
- Java and Android libraries can be found within the [`whirlpool-client`](https://github.com/Samourai-Wallet/whirlpool-client) repository.
- A command line client is also available. You can find more information within the [`whirlpool-client-cli`](https://github.com/Samourai-Wallet/whirlpool-client-cli) repository.

## Implementing Whirlpool into your products and services

Samourai has strived to create a toolkit that can easily be implemented and embedded at any level of your existing technology or product stack. We would love to discuss how you plan to use Whirlpool within your own products and services and how we can help. Email us at implementations@samourai.io

## Acknowledgements
Whirlpool theory is based on a fork of the original [ZeroLink](https://github.com/Samourai-Wallet/Whirlpool/tree/25723b8832c59f6920e341e1b7f565f51f117cea) framework which was originally co-written by [nopara73](https://github.com/nopara73) and [TDevD](https://github.com/samouraidev), with thanks to Adam Gibson and Chris Belcher from [JoinMarket](https://github.com/JoinMarket-Org/joinmarket), Ethan Heilman from [TumbleBit](https://eprint.iacr.org/2016/575.pdf), Dan Gershony from [Breeze Wallet](https://github.com/stratisproject/Breeze/) and Kristov Atlas from [Open Bitcoin Privacy Project](http://openbitcoinprivacyproject.org/) for their reviews, suggestions and feedback.

Significant changes have been made since the fork from ZeroLink. We thank [TDevD](https://github.com/samouraidev) and [ZeroLeak](https://github.com/zeroleak) of [Samourai](https://samouraiwallet.com), and [LaurentMT](https://github.com/laurentMT) of OXT.me for their continued contributions.

## Support

If you appreciate our work and wish to support our continued efforts in providing free, unencumbered, open source code that enhances your sovereignty please consider a donation.

### Address

bc1qh287jqsh6mkpqmd8euumyfam00fkr78qa9kqk2  
[![address](http://api.qrserver.com/v1/create-qr-code/?color=000000&bgcolor=FFFFFF&data=bc1qh287jqsh6mkpqmd8euumyfam00fkr78qa9kqk2&qzone=1&margin=0&size=200x200&ecc=L)](https://oxt.me/address/bc1qh287jqsh6mkpqmd8euumyfam00fkr78qa9kqk2)

### PayNym (BIP47)

PM8TJVzLGqWR3dtxZYaTWn3xJUop3QP3itR4eYzX7XvV5uAfctEEuHhKNo3zCcqfAbneMhyfKkCthGv5werVbwLruhZyYNTxqbCrZkNNd2pPJA2e2iAh  
[![BIP47 payment code](http://api.qrserver.com/v1/create-qr-code/?color=000000&bgcolor=FFFFFF&data=PM8TJVzLGqWR3dtxZYaTWn3xJUop3QP3itR4eYzX7XvV5uAfctEEuHhKNo3zCcqfAbneMhyfKkCthGv5werVbwLruhZyYNTxqbCrZkNNd2pPJA2e2iAh&qzone=1&margin=0&size=200x200&ecc=L)](https://paynym.is/+samouraiwallet)
