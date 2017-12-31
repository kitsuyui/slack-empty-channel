# slack-empty-channel

## Usage

1. Download latest `slack-empty-channel` binary that suits your platform from [release page ](https://github.com/kitsuyui/slack-empty-channel/releases/).
2. Make it executable. (`chmod +x ./slack-empty-channel`)
3. Set environment variables.
4. Execute it.

```
$ ./slack-empty-channel
```

And then it reports empty channels into incoming-webhooks channel.

## Run periodically

It doesn't have any daemonizing options.
So you must set in cron jobs or daemonize script if you want it runs periodically.

### Tokens

- incoming-webhook: https://{ your organization }.slack.com/services/new/incoming-webhook
- oauth-tokens: https://api.slack.com/docs/oauth-test-tokens

### Environment variables.

See .env.sample .

```console
$ export SLACK_API_TOKEN='xxxx-1234567890-1234567890-124567890-aaaaaaaaaaaaaaaaaaaaaaaa'
$ export SLACK_WEBHOOK_URL='https://hooks.slack.com/services/dUmMy/YOuR/HoOkUrLHeRE'
```

## Build

```
$ docker run --rm -v "$(pwd)":/slack-empty-channel -w /slack-empty-channel tcnksm/gox sh -c "./build.sh"
```
