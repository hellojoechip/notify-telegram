# Notify-telegram
Pushing a notification to telegram when a new commit is made.

<br/>
For updates subscribe to my telegram channel at https://t.me/Devops3_1
<br/>
To push notifications to the channel, run this in your web browser: https://maker.ifttt.com/trigger/devops3/with/key/k9VvAtBb7S7ZI2UTxTf3lk2H7LYllSoJuryAqzwLVWL

<br/>
<br/>

![telegram the botfather](https://user-images.githubusercontent.com/71744836/94844191-744c8a00-0450-11eb-9d30-d476724bc6c0.jpg) <br/>
Source: https://core.telegram.org/file/811140763/1/PihKNbjT8UE/03b57814e13713da37
<br/>
<br/>

# The steps 

## Setting up telegram
This is for creating a bot and channel.
1. Search for 'BotFather' on [telegram](https://telegram.org/).
2. Create and name your bot.
3. Create a new telegram channel.
4. Add the bot created to your new channel.

## Setting up ifttt
1. Create an account and login to [ifttt](https://ifttt.com).

## The webhooks setup
This is for creating the automated message and sending it a publicly accessible URL when a commit is made.
1. Login to [webhooks settings](https://ifttt.com/maker_webhooks/settings).
2. Copy and paste URL into browser.
3. Fill in the blanks. (event: devops3 -- I used my telegram channel name)
4. Copy the curl, replace the last line of test1.yml file with this. 

## The ifttt setup <br/>
This requires 2 applets to be created. <br/>
Each applet has a trigger (if) and response (then).
<br/>
<br/>
![Trigger   response process](https://user-images.githubusercontent.com/71744836/94854890-36576200-0460-11eb-94d8-c8ecb3158be1.png)

<br/>

### The first applet <br/>
This is to make a web request when a new commit is made in the repository.

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

### The second applet <br/>
This is to send a notification to telegram when a web request is received.

1. Click on 'create' to create a new applet.
2. Click on 'if this' and search for webhook. 
3. Follow the authorization process and connect telegram and ifttt.
4. Choose your trigger.
5. Key in your event name. (For event name, refer to step 3 under webhooks setup.)
6. Click on 'create trigger'.
7. CLick on 'then that' and search for telegram.
8. Choose an action.
9. Change target chat to your newly created telegram channel.
10. Enable web page preview. (still no idea what this does)
11. Click on 'create action'.

<br/>

### Testing it
If the setup is done correctly, your newly created telegram channel will receive a notification each time a new commit is made.

<br/>
<br/>
Please feel free to make pull requests if any of the steps are incorrect or missing.
