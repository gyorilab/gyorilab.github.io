CLARE uses the Slack Real Time Messaging (RTM) API to connect to a Slack workspace and answer messages
sent to it either in one-to-one private conversations, or in multi-party dialogues and channels 
(only ones to which clare was invited) when
messages are prepended with @clare. The RTM API requires setting up a "classic app" on the Slack website as
the instructions describe below.

1. Go to https://api.slack.com/apps?new_classic_app=1

    You should see a dialog with the header `Create a Slack App (Classic)`. Enter the following information:

    - App name: clare
    - Development Slack Workspace: `<select your workspace from the dropdown>`.

    If the workspace doesn't appear in the dropdown,
    click "+ Sign in to another workspace" and sign in first, then come back to this page.
    Then click the `Create App` button. This should take you to the app's settings page.

2. Under the `Add features and functionality heading`, click the `Permissions` card.
  
    The second heading on this page is called `Scopes`, here click the `Add an OAuth Scope` button.
    Scroll down and select the `bot` scope from the list to add it.

    We next need to add a bot user.

3. Click the `App Home` menu item on the left, then click the `Add Legacy Bot User` button.

    In the dialog, enter the following information:
    - Display Name (Bot Name): clare
    - Default username: clare

    On the top of the page, a message should appear saying `Bot user added!`.

4. Click on the `Install App` menu item on the left. Then click on the `Install App to Workspace` button.

    This opens a page where the permissions of the bot can be reviewed. Click Allow.
    The next page displays the access tokens for the app.

5. Copy the `Bot User OAuth Access Token`. This token needs to be used when connecting to the Slack RTM.
