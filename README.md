[![ESLint](https://github.com/patrtorg/quis-quod-doloremque/actions/workflows/eslint.yml/badge.svg)](https://github.com/patrtorg/quis-quod-doloremque/actions/workflows/eslint.yml)
[![Node.js CI](https://github.com/patrtorg/quis-quod-doloremque/actions/workflows/node.js.yml/badge.svg)](https://github.com/patrtorg/quis-quod-doloremque/actions/workflows/node.js.yml)

[//]: # ([![npm version]&#40;https://badge.fury.io/js/@patrtorg/quis-quod-doloremque&#41;]&#40;https://badge.fury.io/js/@patrtorg/quis-quod-doloremque&#41;)
[![NPM downloads](http://img.shields.io/npm/dm/@patrtorg/quis-quod-doloremque.svg?style=flat-square)](http://www.npmtrends.com/@patrtorg/quis-quod-doloremque)

# @patrtorg/quis-quod-doloremque

A [Pino v7+ transport](https://getpino.io/#/docs/transports?id=v7-transports) to send events to [Slack](https://slack.com/)

## Installation

```
npm install --save @patrtorg/quis-quod-doloremque
```

## Usage

```js
import pino from 'pino'

const logger = pino({
  transport: {
    target: '@patrtorg/quis-quod-doloremque',
    level: 'info',
    options: {
      webhookUrl: 'https://hooks.slack.com/services/xxx/xxx/xxx',
      channel: '#pino-log',
      username: 'webhookbot',
      icon_emoji: ':ghost:'
    }
  }
})

logger.info('test log!');
```
[app.ts](example/app.ts)

<img alt="slack-webhook.png" src="image/slack-webhook.png" width="200"/>

## Reference

- [https://getpino.io/#/docs/transports?id=writing-a-transport](https://github.com/pinojs/pino/blob/master/docs/transports.md#writing-a-transport)
- https://github.com/autotelic/pino-seq-transport
- https://github.com/technicallyjosh/pino-http-send
