# node-red-contrib-socketio-2.x-client-with-dynamic-listener-emitter
is edit clone from node-red-contrib-socketio-client-with-dynamic-listener-emitter

## Nodes

1. Socket.IO Emitter
2. Socket.IO Listener

## How to use

> Socket.IO Connector -> Socket.IO Listener -> Payload

# Socket.IO Connector

default options setting is a json string:

{
  transports: ["websocket"],
  forceNew: true,
  reconnectionAttempts: '2',
  reconnectionDelay: 1000,
  timeout: 2000,
};

options it can not fill in;

you can overwrite it or add new attribute

for example:

you set options in ui {"query": "userId=10392"}

the composite results is

{
  transports: ["websocket"],
  forceNew: true,
  reconnectionAttempts: '2',
  reconnectionDelay: 1000,
  timeout: 2000,
  query: 'userId=10392',
};

#Note: Now this lib under development


# 1. Socket.IO Emitter 

  We can create dynamic emittor node. ie the event name and message are created runtime based on the input's message payload.
  From message payload we accept eventName as 'msg.payload.eventName' and emitted message as  'msg.payload.message'.
  
# 2. Socket.IO Listener 

  We can create dynamic listener node. ie the event name is created runtime based on the input's message payload.
  From message payload we accept eventName as 'msg.payload.eventName'.
  
