# Papercups Chat

This repo contains the code for the chat window implemented by Dawood Trumboo

## Getting Started

# Clone the repository

```bash
git clone https://github.com/dawoodtrumboo/papercup-chatbot.git
```

# Setup the Chat Widget which will be rendered

Go into chat-widget-master

```bash
cd chat-widget-master
```

Run the following command

```bash
npm install or sudo npm install `(if persmission denied)`
```

Then go inside example

```bash
cd example
```

Run the following command

```bash
npm start
```

This will start the app at [http://localhost:3000](http://localhost:3000).

# Setup the Widget Window

Go into chat-window-master

```bash
cd chat-window-master
```

Run the following command

```bash
npm install or sudo npm install `(if persmission denied)`
```

Run the following command

```bash
npm run dev or  export NODE_OPTIONS=--openssl-legacy-provider npm run dev `(incase of error)`
```

This will start the app at [http://localhost:8080](http://localhost:8080).

You can start editing the page by modifying the components in the `/components` directory. The page auto-updates as you edit the file.

## Development

You'll notice on the localhost:8080, nothing gets render, the chatbot will be rendered on localhost:3000.
In case of implementing the chatbot for inhotel.io what we can do is we host the chat-window-master on our own server and instead of papercup's baseUrl in the chat widget component, we'll overide it with adding the iframeUrlOverride = {our server url} ,

To develop this chatbot, we need to run both directories side by side to see the changes.
