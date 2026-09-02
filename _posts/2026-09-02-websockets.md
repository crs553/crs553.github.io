---
layout: post
title: Websockets - Intriduction
date: 2026-08-12
---

This article is the first in a series on understanding WebSockets.

Writing about a subject often helps develop one's understanding of it, so I thought it was appropriate to attempt this myself.

I want to use this series of articles to help me (and potentially others) explore what is involved in using this protocol and how I might apply it to future projects.

## Why WebSockets?

First and foremost, when understanding WebSockets, it is important to understand the motivation behind their use.
In the simplest sense, the web has traditionally followed a request–response model. This involves the client making a request to the server. The server then responds with some data, such as a webpage, an error code, or other information.
The client can interact with this data (e.g. a webpage) and then request more data by, for example, clicking a link or submitting a form.
This has worked well for a lot of applications. However, for some applications, real-time information is required. For instance, in a quizzing application such as Kahoot, the server needs to send information to the client as soon as something happens, without waiting for the client to make another request.
This is where a persistent, bidirectional communication channel is required; this is where WebSockets come in.

## What are WebSockets?

Websockets are:

> A communication protocol that enables persistent, bidirectional communication between a client and server.

They are a choice when you need two-way communication and are particularly useful for applications requiring real-time communication, such as collaborative applications, multiplayer games, or live updates where the server needs to provide information to the client as soon as it becomes available, rather than waiting for a new request.

WebSockets operate over TCP and commonly use port 80 (ws://) or 443 (wss://). They allow full-duplex communication, meaning data can flow in both directions at the same time.

## How do they work?

WebSockets begin with an HTTP handshake. Once the connection is successfully upgraded from HTTP to WebSocket, it remains open.

Both the client and server can then send data to each other independently, without either side having to wait for the other to make a new request.
WebSockets work by first handshaking through http. Once the connection is 'upgraded' (the term used by the protocol) it stays open; both client and server can send data to eachother entirely independently.

## Getting Started

There are two options:

1. Use native websocket APIs
2. Use an existing, managed WebSocket Platform
