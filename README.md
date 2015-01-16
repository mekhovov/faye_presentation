## The Dark Arts of Push Servers
Coupa on Faye


## INSTALL

### Install compass

gem install compass
compass watch -s expanded

### Run server or just open index.html
./serve.sh 8080

### Install Python libraries for markdown (optional)
sudo easy_install Jinja2
sudo easy_install markdown




## TODO:


http://faye.jcoglan.com/
https://github.com/faye/faye
http://railscasts.com/episodes/260-messaging-with-faye
http://railscasts.com/episodes/316-private-pub?
view=asciicast
http://svn.cometd.com/trunk/bayeux/bayeux.html
https://github.com/ryanb/private_pub
https://github.com/dmoulton/fayedemo




What is Faye?

Faye is an implementation of the Bayeux protocol. Clients send messages to each other via a central server, by sending JSON messages over various flavours of HTTP-based transport, including WebSocket, EventSource, XMLHttpRequest, CORS and JSON-P. Clients that run in the browser are not constrained by the same-origin policy.

Messages are routed using subscriptions. When a client publishes a message, the server determines which clients are subscribed to the message’s channel and forwards the message to them verbatim. This means the whole wire message is forwarded, not just the data field containing the application payload.

A special set of channels whose names begin with /meta/ are used for operating the protocol itself, and messages sent to these channels are never forwarded to other clients.

Messages pass through extensions on their way into and out of the clients and server. Data required by extensions is typically sent in the message’s ext field. Any changes made to a message by a server-side extension will be reflected in the messages forward to subscribed clients.

Authorization credentials embedded in messages should be deleted from them by server-side extensions to prevent these credentials being forwarded to subscribed clients.



http://faye.jcoglan.com/security.html