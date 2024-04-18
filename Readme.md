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

## Changes

- Changes made in theme

  The changes in the theme was done in **chat-window-master**. There is a helper function (theme.ts) where I change the colors according to the theme I wanted.
  `eg. I change the overide object's primary color from blue to yellow`.

- Changes made for Responsiveness

  For responsiveness the widget components provides us with the style attribute where we can change the width and height of the window. The changes I did are in the **chat-widget-master/example/src/App.tsx**. So what I did is , I created a variable which would capture the size of the window width because inline styling doesn't support media queries. Then I used that window size to dynamically set the size of the widget by making changes in the style object.
  Now here I was facing an issue , the toggleButton was coming on top of the chat window. So I created a function and a state to watch whether the chat window is open or close. So the widget comes with attributes such as onChatOpened & onChatClosed. I binded them with function which was setting the isOpen state to either true or false. So on mobile screens whenever the chat was opened the chat widget would hide its toggleButton.
