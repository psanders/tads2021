## Inbound Call Setup

**Create a new Provider**

Run the command `fonoster providers:create` with the following parameters:

```none
friendly name = my-provider
username = tadsummit01
secret = [PASSWORD]
host = newyork1.voip.ms
transport = tcp
sip registration refresh = 3600
```

**Create a new Number**

Run the command `fonoster numbers:create` with the following parameters:

```none
number in E.164 format = [YOUR_NUMBER]
service provider [YOUR_PROVIDER_NAME]
address of record [IGNORE]
webhook [YOUR_NGROK_URL]
```

Call your Virtual Number. You should hear a "hello world.'
