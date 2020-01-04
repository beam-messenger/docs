# Scope
In some messengers, users can interact with any other user. In others, they can only interact with users that are on the same deployment of the messenger. Which users can interact with which other users depends on something we call 'scope', and we identify three categories:
* Global: users can interact with all users
* Siloed: users form logical groups and can only interact within a group
* Federated: users form logical groups but can still interact with all users

## Global
The most popular messengers are global. Global messengers assign each user a globally unique identifier like a username or phone number for users to find each other. They're generally run by a single organization and at least the server is closed source (otherwise other organizations could run their own).

## Siloed
Siloed messengers are for teams and businesses where users only need to interact with other members of the same organization. Sometimes this means businesses deploy servers for the messenger on-premise and messages are server-local; other times businesses pay for a 'workspace' that's hosted by the messenger company but still siloed.

## Federated
Federated messengers are the most complicated. Federated messengers allow people to run their own servers but all the servers connect to form one global network. Users sign up with one of the servers (they pay the server owner if it's a paid service). Users are identified by a server-local unique idenfier plus a server identifier e.g. @johndoe:server.com.

Federated messengers tend to be open source and are often open spec. They tend to be more sustainable than global networks because they are deployed by a variety of organizations if not developed by a variety of organizations.

Some siloed essengers offer server federation for scalability but users are only reachable within an organization; we call these siloed messengers even though federation is involved at the server level.
