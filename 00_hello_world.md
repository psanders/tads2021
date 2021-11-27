# Practice #1: Hello world

## Part #1

1. Start Ngrok on port 3000
2. Create a folder and init a NodeJS application
3. Install the voice module `@fonoster/voice`
4. Create an `index.js` file with the content below and start the service

```javascript
// index.js
const { VoiceServer } = require("@fonoster/voice");
const voiceServer = new VoiceServer();

voiceServer.listen(async(req, res) => {
  console.log(req);
  await res.answer();
  await res.play("sound:hello-world");
  await res.hangup();
});
```

## Part 2

1. Go to `https://console.fonoster.io` to get your credentials
2. Use `fonoster auth:login` to login the tool
3. Use `fonoster projects:create` to create a new project
4. Use `fonoster projects:use [REF]` to set the current project

## Part 3

1. Create a VoIP provider with `fonoster providers:create` and credentials we provied
2. Create a Number with `fonoster numbers:create`
3. Create a Domain with `fonoster domains:create`
4. Create an Agent with `fonoster agents:create`

## Part 4

1. Launch the phone simulator with `fonoster phone:start`
2. Configure the phone simulator
3. Call the Voice Application from the browser
4. Call the Voice Application from your phone

