# Beam Messenger
The world of messengers is populous, yet we are unable to find a satisfactory choice. The feature set we are interested in is:
* Open source client and server
* Federated and deployable on-premise
* Anonymous; identity not based on phone number or other outside identity
* End-to-end encrypted private and group messages
* Multi-device messaging with support for all major platforms
* Search

Additionally, we have the following design philosophies:
* Simple UX
* Native-level performance and power consumption

## Existing Solutions
Digital Communications Protocols presents a breakdown of the features of 80 products. Of those, only 4 fulfill our desired feature set:
* Matrix/Riot
* XMPP
* Nextcloud Talk
* Kontalk

We have additionally tried these 5 messengers:
* Slack
* Hangouts
* Signal
* Keybase
* Wire

### Matrix/Riot
Matrix is an open standard for communication with many implementations. The most notable client is Riot - the Matrix team didn’t start using Matrix until the Riot implementation was stabilized. We’re largely going to judge Matrix by Riot’s feature set because it’s the most feature-rich and supports the most platforms of any Matrix client.

What Riot gets right:
* Checks all boxes for feature set
* Apps are performant (well-optimized Electron apps)
* Interoperability

What Riot gets wrong:
* No encrypted message search
* Device verification requires full mesh (optional)
* Bugs, inconsistent/complicated UX, general lack of polish

### XMPP
XMPP, like Matrix, is an open standard for communication with many implementations, but at a lower level. It’s more of an XML streaming protocol than a messenger; it’s at the same level of abstraction as HTTP. XMPP is used by Facebook Messenger, Google Chat, and WhatsApp among others.

### Nextcloud Talk
Nextcloud Talk is a very enterprise-y messaging platform (it’s comparison page compares Nextclouds ecosystem to other enterprise ecosystems). You can self-host or have them host for $90 per user per year. While it’s technically federated, you need admin access to two servers to connect them, which makes Nextcloud Talk networks closed and not ideal for use as a messenger.

### Kontalk
Kontalk is a “community-driven instant messaging network” with all the hallmarks of an underfunded open-source project. I was unable to find an explanation of how it works. From screenshots, the UX seems pretty basic (although it does have native apps). I also got a certificate error when I accessed their website.

### Slack
Slack is a popular messaging platform for teams.

What Slack gets right:
* On-premise deployments
* Polished
* Search

What Slack gets wrong:
* Messaging is server-local
* Not encrypted
* Closed source
* Heavy clients that use electron

### Hangouts
Hangouts is a popular messenger by Google.

What Hangouts gets right:
* Best video chatting experience

What Hangouts gets wrong:
* Not encrypted
* No native clients
* Closed source
* No self hosting

### Signal
Signal is an open-source secure messenger.

What Signal gets right:
* Encrypted
* Open source
* Simple UX

What Signal gets wrong:
* Not anonymous - identity is based on phone number
* Clunky electron apps

### Keybase
Keybase is an open-source secure messenger, filestore, cryptocurrency wallet, git repository, and some other things too…

What Keybase gets right:
* Encrypted
* Open source clients
* Anonymous

What Keybase gets wrong:
* Closed source server
* Messaging and other errors
* Too many services in one
* Developers not that quick to ack/fix bugs
* Funding source influences development

### Wire
Wire is an open-source secure messenger.

What Wire gets right:
* Encrypted
* Open source
* Search
* Simple UX

What Wire gets wrong:
* Clunky electron apps
* Message decryption is slow
* Some bugs
* Lack of organizational clarity

## High Level Design
Matrix seems like a promising standard. The ability to interoperate with established products is great. Using Matrix helps us develop incrementally, implementing a server without a client or vice versa. Using Matrix takes parts of our design out of our hands, but Riot is a solid demonstration of its quality.

Todo: understand Matrix in more detail (spec)

### Client
Potential Riot improvements:
* Client-side search of encrypted messages
* Simplify user experience
* One-touch chat switching on mobile
* Don’t have bugs
  * Travis got randomly added to 2 empty rooms on Android
  * Parth has really large context menus on Android
  * Key synchronization is noisy and inconsistent

### Server
Potential server improvements:
* Write server in Rust instead of Python (has this been done?)
* Make server horizontally scalable using distributed systems magic (is this possible?)
