# Bachelor-Seminarium

**Spending 50kEuro - operational security procedures for anonymous hosting** — As of 2015, Delft University owns 50000Euro of Bitcoins to buy computer hardware in complete privacy. Your task is to spend these Bitcoins in a safe and productive manner by devising and documenting operational security procedures for anonymous hosting. If finished and approved you will be asked to help execute your own plans. You will investigate and search the literature on how to make Bitcoins anonymous and how to safely procure private servers for anonimized Bitcoins. You will search the literature on anonymous cash and hosting. Documentation also includes trial evidence used against the Silk Road in order to document basic mistakes.

## Summary
 - [Overview of Papers](Overview.md)
 - [Relevant links](Links.md)
 - [Research keywords](Keywords.md)
 - [Potential hosts](Hosts.md)


## Anonymous payment
Bitcoin could be used to pay for hosting. Several (hosting) companies/providers accept Bitcoin payments. The point is, Bitcoin transactions are public and therefore not totally anonymous. Several techniques could be used to anonymize: mixing transactions, shared wallets. Some commercial services exist: Bitcoin Fog, BitLaundry, Blockchain.info's Send Shared. There's been many research on the anonymity of Bitcoin and we could probably use that. 

## Anonymous server management
When we want to purchase a VPS or manage it, we should not publish our location. The easiest is to use the TOR protocol which establishes a connnection to a server through mulitple relays. And the last one, the exit node, connects to the actual server. To prevent the exit node from capturing our traffice, which an untrusted maintainer of an exit node could do, we must make sure we use end-to-end encryption. This can be achieved by using HTTPS, Tunnel Proxy, SSH and/or a VPN through Tor.

To prevent our computer or browser leaking any information to third parties, we could use WhoNIX or Tails, both linux distributions build for keeping someone anonymous. These distributions make sure that any out going connection is passed through Tor.

## Anonymous hosting provider
Maarten

## Silk Road mistakes
Silk Road's mistakes can be grouped as either technical mishaps or human failure. Ulbricht, the creator of Silk Road, left a lot of traces online hinting at his ownership of Silk Road. For instance, Ulbritch used his real email address when hiring an IT specialist and used his real name on Stack Overflow when asking questions about Tor. These mistakes are something to keep in mind, but aren't incredibly relevant to the paper.

On the technical front i expected to find a subtle mistake and some really clever hacking, but was left feeling dissappointed. As the FBI was feeding the login page random strings, they noticed some data originated from an ip address that wasn't associated with any known Tor exit nodes. Upon entering this ip into a regular browser Silk Road's Captcha prompt appeared. In short, the login page was poorly configured for Tor and as such leaked the server IP. After the servers were taken into custody, they discovered an IP address that was last used to connect to the server was the same one Ulbricht used to access his Gmail account. 

