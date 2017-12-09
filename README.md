# Connex Protocol Reference



Connex is an aforesaid secure P2P message protocal using WebRTC for connections and GPG for identification, capable for group chats with reasonable timing.

## Roles

### Hub

Also known as `server`, is required for the very first connection.

**Functionality:**

1. Tracker, stores pod informations including pods' public key.
2. Proxy when direct P2P connections are not available.

**Security:**

1. Have no ability to read messages for the initial handshaking message is not readable without private keys.

### Pod

Also known as `client`, is the basic component of the connex network.

**Functionality:**

1. Peer node which can connect to hubs and other pods, and can be connected by other pods.
2. Tracker, stores peer informations that connected to this pod. Similar to DHT.
3. Proxy when two connected pods cannot communicate directly.
4. Stores verified history messages that goes through this pod.

**Security:**

1. Messages stored must be encrypted as received.
2. Block unverified message transfer.
3. Have no ability to read unauthorized messages for the initial handshaking message is not readable without private keys.

## API

*TBD*