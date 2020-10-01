# Notify-telegram

I created 2 ways to push a notification to telegram.
1. When a new commit is made.
2. When a new pull request is made.

<br/>

## Setting up telegram
1. Search for 'BotFather' on [telegram](https://telegram.org/).
2. Create and name your bot.
3. Create a new telegram channel.
4. Add the bot created to your new channel.

## Setting up ifttt
1. Create an account and login to [ifttt](https://ifttt.com)

<br/>
<br/>

## 1. Pushing a notification when a new commit is made

### The webhooks setup
1. Login to [webhooks settings](https://ifttt.com/maker_webhooks/settings)
2. Copy and paste URL into browser.
3. Fill in the blanks. (event: devops3 -- I used my telegram channel name)
4. Copy the curl, replace the last line of test1.yml file with this. 

### The ifttt setup <br/>
This requires 2 applets to be created. <br/>

<br/>

_The first applet_ <br/>
This is to create a web request when a new commit is made.

1. Click on 'create' to create a new applet.
2. Click on 'if this' and search for github. 
3. Follow authorization process to connect github and ifttt.
4. Choose your trigger.
5. Key in your repository name. (eg. Huiling97/notify-telegram)
6. Click on 'create trigger'.
7. CLick on 'then that' and search for webhook.
8. Choose an action.
9. Set URL.
10. Set method to POST.
11. Set content type as application/json.
12. Enable web page preview. (no idea what this does)
13. Click on 'create action'.

<br/>

_The second applet_<br/>
This is to send a notification to telegram when a web request is created.

1. Click on 'create' to create a new applet.
2. Click on 'if this' and search for webhook. 
3. Choose your trigger.
4. Key in your event name. (For event name, refer to step 3 under webhooks setup.)
5. Click on 'create trigger'.
6. CLick on 'then that' and search for telegram.
7. Choose an action.
8. Change target chat to your newly created telegram channel.
9. Enable web page preview. (still no idea what this does)
11. Click on 'create action'.

<br/>

### Testing it
If the setup is done correctly, your newly created telegram channel will receive a notification each time a new commit is made.

<br/>
<br/>

## 2. Pushing a notification when a new pull request is made

### The ifttt setup
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

### Testing
To test if the setup works, create a trigger based on the one you have chosen under step 5. <br/>
If the setup is done correctly, your newly created telegram channel will receive a notification.
