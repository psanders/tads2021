# Exercise #3: Creating a Voice Assistant with Rox AI

[Rox AI](https://github.com/fonoster/rox) is a connector between Fonoster and Dialogflow. It will allow you to deploy a voice application from your existing Dialogflow Agents.

**Steps:**

1. Close the old application
2. Be sure to have the `google.json` file
3. Run the following command:

## Linux/OSX

```bash
rox \
--asr-engine=google \
--tts-engine=google \
--intents-engine=dialogflow.es \
--tts-voice=en-US-Standard-C \
--language-code=en-US \
--google-config-file=$(pwd)/google.json
```

## Windows

**CMD**

```bash
rox ^
--asr-engine=google ^
--tts-engine=google ^
--intents-engine=dialogflow.es ^
--tts-voice=en-US-Standard-C ^
--language-code=en-US ^
--google-config-file="%cd%"/google.json
```

**Powershell**

```bash
 rox `
--asr-engine=google `
--tts-engine=google `
--intents-engine=dialogflow.es `
--tts-voice=en-US-Standard-C `
--language-code=en-US `
--google-config-file=${pwd}/google.json
```
