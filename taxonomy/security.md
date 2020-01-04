# Security
Security in a messenger revolves around who can know what. Certain parts of security aren't up to the messenger. Your ISP will always see your internet traffic and a keylogger on your device can always compromise your message contents. Some guarantees can be provided by a messenger though. We identify two categories of important messenger security features:
* Encryption
* Anonymity

## Encryption
Encryption controls who can read a message separately from who stores or moves the message using mathematical guarantees. This prevents messenger clients from needing to trust servers, which is critical for security. Even if the server is open source, proving that the server is running the version of the code that's open source is difficult and complicated at best (though some messengers try). Clients can be compiled from source to be sure of what you're running; encryption guarantees that no server can read your messages.

### Passwords And Keys
To perform encryption, you need to use a key. You can use a password as a key, but if you do, your messages are only as secure as your password - attackers can guess short or obvious ones just by checking lots of passwords. Additionally, users don't want to remember more than one password for a messenger, so if an attacker gets your password they have everything.

It's more secure to generate a key. Generated keys are long and random, making them statistically impossible to guess. The downside is that users can't remember keys, so the messenger needs a mechanism to securely sync keys across devices. For added security, some messengers generate new keys for each conversation or a different key for each device to limit what an attacker can access if they manage to get one of your keys.

### Encryption At Rest
When messengers say they're encrypted, they usually mean they encrypt messages before sending them and the sender decrypts them when they're received. Some messengers additionally offer at-rest encryption; they make sure messages are never saved unencrypted so that they can't be read if your device is stolen. Encryption at rest doesn't help if your device is compromised; if it's a work device for instance, your company could have installed a keylogger that would make encryption unhelpful.

### Technical Complexity
The most full-featured messengers aren't encrypted, and that's because encryption makes certain features hard to build. Group conversations can get tricky, with some encrypted messengers not offering group chats or only offering unencrypted group chats. Search can only happen on the client because the server can't understand what it's searching through; few  messengers offer search on encrypted conversations.

## Anonymity
Anonymity is concerned with whether someone can connect your identity on the messenger with your identity in other places. A messenger that requires you to sign up with your phone number is not anonymous because your messenger identity is associated with your cell phone plan, which is often associated with your name, address, and social security number. Your email is associated with any number of other accounts you have.

Like encryption, anonymity makes it harder to implement some features. In many social networks, you associate a phone number with your account, and other users can use their contacts to check for friends they might have on the network. This drives adoption by making it easier for users to onboard, but can't be achieved with anonymity.
