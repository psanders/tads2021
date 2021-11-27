# Practice #2: Connecting to Speech APIs

1. Copy the `google.json` file at the root of your application
2. Modify your application to look like that one bellow
3. Test your application using your mobile or phone simulator

```javascript
// index.js
const { VoiceServer } = require("@fonoster/voice");
const GoogleTTS = require("@fonoster/googletts");
const GoogleASR = require("@fonoster/googleasr");
const voiceServer = new VoiceServer();
const speechConfig = { keyFilename: "./google.json" };

// Set the server to use the speech APIS
voiceServer.use(new GoogleTTS(speechConfig));
voiceServer.use(new GoogleASR(speechConfig));

voiceServer.listen(async(req, res) => {
  console.log(req);
  await res.answer();
  // To use this verb you MUST have a TTS plugin
  const speech = await res.gather();

  await res.say("You said " + speech);
  await res.hangup();
});
```
