# Open Source
Open source is important for secure software because it allows people to verify that it's secure. It's also helpful from a sustainability standpoint - if a company loses funding and disappears and not all of its code is open source, the product stops working.

We identify four levels of open source for messengers:
* Closed source
* Open source client
* Open source server
* Open source spec

## Closed Source
The most popular messengers are closed source. Closed source messengers can only be run by the company that builds them, giving them the ability to charge money or sell data. They can use this income to build polished, full-featured apps.

Closed source messengers usually aren't security-focused. Messengers that sell data to work necessarily violate privacy, and because it's hard to trust closed source software, any reasonable security-focused messenger would need to open source.

## Open Source Client
Open sourcing a client is a middle-ground that lets a messenger company prove some security features of their app (generally end-to-end encryption) while still being able to charge money.

Companies that build open source client messengers can't sell data because it's encrypted, so they generally have a paid tier of the messenger for businesses to fund development.

## Open Source Server
Messengers with open source servers generally also have open source clients. With the full source of the messenger being open, all the security features can be checked, and the service can be run by anyone at cost even if the organization that created it disappears. These messengers are generally funded by community contributions and company partnerships.

## Open Source Spec
Some messengers go one step further for sustainability. Instead of making an open source messenger, they make an open source spec which can be implemented by any messenger (often including a reference implementation). This facilitates a network of interoperable messengers that give users freedom to choose without needing to migrate their friends.

The spec is managed and evolved by the open-source community, preventing an organization from moving the messenger in an undesirable direction. At the same time, new features must be coordinated across all the implementations, making it challenging for open source spec messengers to iterate as fast as competitors.
