# notify-telegram

Sending a notification to my telegram channel when a new pull request is made.

# The telegram setup

* Search for 'BotFather' on telegram.
* Create and name your bot.
* Create a new telegram channel.
* Add the bot created to your new channel.

# The ifttt setup

* Create an account and login to [ifttt](https://ifttt.com)
* Click on create to create a new applet.
* Click on 'if this' and search for github. 
* Follow authorization process to connect github and ifttt.
* Choose your trigger.
* Key in your repository name. (eg. Huiling97/notify-telegram)
* Click on 'create trigger'.
* CLick on 'then that' and search for telegram.
* Follow authorization process to connect telegram and ifttt.
* Choose an action.
* Set target chat to newly created telegram channel.
* Modify message text to your liking.
* Enable web page preview. (no idea what this does)
* Click on 'create action'.

# Testing

To test if the setup works, create a trigger based on the one you have chosen under step 9.
If the setup is done correctly, your newly created telegram channel will receive a notification.
