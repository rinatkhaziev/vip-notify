# vip-notify

Send wordpress VIP deployment notifications to Slack

[![Travis](https://img.shields.io/travis/doejo/vip-notify.svg)]()

## Install

Clone repository and install dependencies:

```
git clone https://github.com/doejo/vip-notify.git
cd vip-notify
bundle install
```

## Configure

Application requires the following environment variables to function:

- `SLACK_WEBHOOK` - Wehbook url for a channel
- `SLACK_CHANNEL` - Channel name to post updates to
- `SLACK_USER`    - Name of the user that sends notifications

## Start

To start application just run:

```
bundle exec thin start
```

## Endpoints

Test integration endpoint:

```
GET /test
```

Notifications endpoint:

```
POST /notify
```

Required params:

- `theme`             - Application theme name
- `deployer`          - Deployer name
- `deployed_revision` - Deployed commit ID
- `previous_revision` - Previously deployed commit ID
- `revision_log`      - Revision log text

## License

The MIT License (MIT)

Copyright (c) 2014-2015 Doejo LLC