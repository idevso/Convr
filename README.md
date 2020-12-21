# Convr

Developing a chat application with Node, React, MySQL and WebSockets.

client repo - [client](https://github.com/idevso/Convr-client)
server repo - [server](https://github.com/idevso/Convr-backend)

## Current Architecture 

The entire application uses React Router Dom to decide which component to render and this is decided upon the information provided by Redux. A rendered component then can make requests to the server or connect to websocket and dispatch actions based on responses or emitted events.
