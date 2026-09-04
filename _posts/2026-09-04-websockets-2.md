---
layout: post
title: WebSockets - The APIs and Interfaces
date: 2026-09-04
---

WebSockets have an API that makes it possible to open a bi-directional communication session between the user (browser) and server.

It allows for sending and receiving messages without the need to poll the server.

The WebSocket API has 2 different mechanisms to create connections. The `WebSocket` interface and the `WebSocketStream` interface.

## WebSocket Interface

Stable interface with good browser and server support, but doesn't support [backpressure](https://developer.mozilla.org/en-US/docs/Web/API/Streams_API/Concepts#backpressure).

The problem with this is that when messages arrive faster than the application can process them, the device's memory can fill up through the buffer of messages and/or the CPU can become overloaded.

## WebSocketStream Interface

Uses the [Streams API](https://developer.mozilla.org/en-US/docs/Web/API/Streams_API) to handle receiving and sending messages.

This provides backpressure mechanisms to regulate reading and writing, helping to avoid bottlenecks when the application can't process messages fast enough.

This interface is non-standard and has limited browser support.

## What Next

[WebTransport API](https://developer.mozilla.org/en-US/docs/Web/API/WebTransport_API) provides some of the capabilities that WebSockets don't, and may be a better fit for some applications.

---

## Sources

[WebSockets API](https://developer.mozilla.org/en-US/docs/Web/API/WebSockets_API)
