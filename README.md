# Convr

Developing a chat application with Node, React, MySQL and WebSockets.

client repo - [client](https://github.com/idevso/Convr-client)
server repo - [server](https://github.com/idevso/Convr-backend)

## Current Architecture 

The entire application uses React Router Dom to decide which component to render and this is decided upon the information provided by Redux. A rendered component then can make requests to the server or connect to websocket and dispatch actions based on responses or emitted events.

![image1](/img/1.png)
![image2](/img/2.png)
![image3](/img/3.png)
![image4](/img/4.png)
![image5](/img/5.png)

## Bugs and Challenges

Redux doesn’t persist the state, this leads to the application losing important data on the authenticated user on certain events such as page reload. If such event occurs while the user is active in a certain room, React Router Dom force renders the login page.

For each client there has to be one socket connection. The application makes this connection when the chat component mounts and as expected should disconnect on unmount. 
The challenge here is occurs when it fails to disconnect, leading to the client having multiple connections when mounting again and emitting an event multiple times when it should only emit once.

## Note

The design and development of this application is still ongoing...

