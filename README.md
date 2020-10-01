# Notify-telegram

Sending a notification to my telegram channel when a new pull request is made.

# The telegram setup

1. Search for 'BotFather' on [telegram](https://telegram.org/).
2. Create and name your bot.
3. Create a new telegram channel.
4. Add the bot created to your new channel.

# The ifttt setup

1. Create an account and login to [ifttt](https://ifttt.com)
2. Click on create to create a new applet.
3. Click on 'if this' and search for github. 
4. Follow authorization process to connect github and ifttt.
5. Choose your trigger.
6. Key in your repository name. (eg. Huiling97/notify-telegram)
7. Click on 'create trigger'.
8. CLick on 'then that' and search for telegram.
9. Follow authorization process to connect telegram and ifttt.
10. Choose an action.
11. Set target chat to newly created telegram channel.
12. Modify message text to your liking.
13. Enable web page preview. (no idea what this does)
14. Click on 'create action'.

# Testing

To test if the setup works, create a trigger based on the one you have chosen under step 5.
If the setup is done correctly, your newly created telegram channel will receive a notification.
