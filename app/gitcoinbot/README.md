# Gitcoinbot is a Github App for Gitcoin.co

## Installation Instructions

The following environment variables must be set for gitcoinbot to work correctly

- GITHUB_API_USER = 'gitcoinbot' ( Should correspond to [the gitcoinbot user](https://github.com/gitcoinbot))
- GITHUB_API_TOKEN = api token for gitcoinbot user (from the developer settings)
- GITCOINBOT_APP_ID = Github application id found on the settings page for [Gitcoinbot](https://github.com/apps/gitcoinbot)
- SECRET_KEYSTRING = contents of pem file from the Gitcoinbot application settings page. This is read in settings.py lines 36-38

Aside from these environment variables, the settings page of the gitcoin bot application must have the correct url for webhook events to post to. It should be set to "https://gitcoin.co/payload" based on urls.py line 131.

After running the migrations and deploying the gitcoin.co website, gitcoinbot will begin to receive webhook events from any repository that it is installed into. This application will then parse through the comments and respond if it is called with @gitcoinbot + registered action call.

## Usage instructinos

[Gitcoinbot](https://github.com/Gitcoinbot) is a bot that allows you to interact with gitcoin via the github comments, like follows:

### help command
![Gitcoinbot help](https://media.giphy.com/media/l3diQfLs75ALi61a0/giphy.gif)

### Gitcoinbot bounty <amount> 
![Gitcoinbot bounty](https://media.giphy.com/media/xT1R9X9z8aIrNwC5Da/giphy.gif)

To get it running on your repo, you can install it [here](https://github.com/apps/gitcoinbot)