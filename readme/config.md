- Go [here](https://github.com/anasty17/mirror-leech-telegram-bot/raw/master/config_sample.env) and copy all the content.
- Then goto [Github Gist](https://gist.github.com/)
- Give your gist a name `config.env`

![image](https://user-images.githubusercontent.com/77688759/161727093-6bac51cf-f26d-46e7-950b-f85700b71be5.png)

- And paste the previously copied content here

![image](https://user-images.githubusercontent.com/77688759/161727191-4f5038e8-aaee-49f4-bba7-cbe849386853.png)

- Now remove line no 2. `_____REMOVE_THIS_LINE_____=True`
  
![image](https://user-images.githubusercontent.com/77688759/161783724-04062575-c742-4500-9eb4-b703363bb037.png)  

- Then start filling the config vars.
- For now i will only show the necessary config values for the proper working of the mirror leech bot.

<b>BOT_TOKEN</b>:
- Search @BotFather on telegram, start the bot and send `/newbot` then follow the on screen instruction to create a new bot.

![image](https://user-images.githubusercontent.com/77688759/161728194-f12dd4e5-dab2-426d-a8af-b672ac7d3f69.png)

- This will be the value of BOT_TOKEN 

  
<b>GDRIVE_FOLDER_ID</b>:
- Search @MSGuite_SD_Creator_Bot on telegram, start the bot click on `genrate td` now send your email address, give your drive a good name for eg `hitesh920's drive` and done.
- Now go inside the shared drive you just created by `google drive` > `shared drive` > `the shared drive you created`.

![image](https://user-images.githubusercontent.com/77688759/161728959-fa766198-0e34-4d4d-bd51-f30f357d7d78.png)
  
- Now copy the root id of your shared drive
- For eg https://drive.google.com/drive/folders/xxxxxxxxxxx then the code after `folders/` will be the your root id

![image](https://user-images.githubusercontent.com/77688759/161729686-d9e79a8f-4479-46ae-84dc-1989df4c75f9.png)

- This will be the value of GDRIVE_FOLDER_ID 

<b>OWNER_ID</b>:
- Search @MissRose_bot on telegram, start the bot then type `/id` bot will send your account's id
- Use that for OWNER_ID
  
<b>DOWNLOAD_DIR</b>:
- Keep the default values, no need to change anything here.

<b>DOWNLOAD_STATUS_UPDATE_INTERVAL</b>:
- Keep the default values, no need to change anything here.

<b>AUTO_DELETE_MESSAGE_DURATION</b>:
- Keep the default values, no need to change anything here.
  
<b>IS_TEAM_DRIVE</b>:
- Set this to `True` as we are using shared drive.
  
</b>TELEGRAM_API & TELEGRAM_HASH</b>:
- Go [here](my.telegram.org) and register with your number connected to telegram account fill with your number , choose desktop,  fill app title and short name to any name you want.

![image](https://user-images.githubusercontent.com/77688759/161731080-bff37137-e53a-4774-a1bd-6288491ca494.png)

- Then goto https://my.telegram.org/apps 
  
![image](https://user-images.githubusercontent.com/77688759/161785532-bef462f6-1416-42ab-b0c7-48c2d6001baa.png)
  
- This will give the values of `TELEGRAM_API` and `TELEGRAM_HASH`

`App api_id` will be your TELEGRAM_API 

`App api_hash` will be your TELEGRAM_HASH

<b>TOKEN_PICKLE_URL</b>:
- Go to your index link and click on the token.pickle u just hosted in step 4 and copy the direct download link.
  
![image](https://user-images.githubusercontent.com/77688759/161749786-d71ab726-51b9-49b7-9dae-b584cd3177e2.png)

- And use that url for TOKEN_PICKLE_URL

<b>BASE_URL_OF_BOT</b>:
- `https://yourappname.herokuapp.com`, suppose if my heroku app name is <b>hitesh920-mirrorbot</b> then the BASE_URL_OF_BOT will be <b>https://hitesh920-mirrorbot.herokuapp.com</b>

<b>UPSTREAM_REPO</b>:
- Your forked repository link, if your repo is private add `https://username:{githubtoken}@github.com/{username}/{reponame}` format. Get token from [Github settings](https://github.com/settings/tokens). So your bot can update from filled repository on each restart.

<b>UPSTREAM_BRANCH</b>:
- Fill `h-code` in UPSTREAM_BRANCH var

We are done with the all necessary configs for the proper working of your mirror leech bot.

It should look like this after filling all the necessary values
  
![image](https://user-images.githubusercontent.com/77688759/161732551-fe9424b4-d141-481c-9de3-d0cb368c1c96.png)

- Then click on create secret gist to save the gist.
  
![image](https://user-images.githubusercontent.com/77688759/161732712-6c3741ac-494b-496d-8fea-3ae21fc8ef3f.png)

- We have successfully created our config.env
