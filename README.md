# deploy-mirror-leech-bot

## Requirements

- Telegram Account
- Heroku Account
- Github Account
- Install Python on Windows
- Google Drive Account

## Repo Link: [Here](https://github.com/anasty17/mirror-leech-telegram-bot)

Now first thing first, fork the repo.

![image](https://user-images.githubusercontent.com/77688759/161710615-c450b852-6acc-481b-a84f-5b3d054b6b05.png)

Now download that repo to your pc.

![image](https://user-images.githubusercontent.com/77688759/161710894-b2840ddf-c186-4a9f-bcb0-e301ffd2d253.png)

the downloaded repo will be in zip file, extract it.

## Required files for the mirror leech bot

Now there are 3 files needed for the working of mirror leech bot.
- credentials.json
- token.pickel
- config.env
will create those one by one

## Create credential.json

<details>
  
  <summary>Click Here</summary>
  
goto your google cloud console. [Here](https://console.cloud.google.com)
create a new project (if you already have a project then no need to create another one)

![image](https://user-images.githubusercontent.com/77688759/161712563-4a2e83ab-b2ba-4134-8d92-cef8e2c09af2.png)
![image](https://user-images.githubusercontent.com/77688759/161712650-1f2b0f7b-0a74-4527-a699-3e09feea2d3a.png)

now select the project you just create.

![image](https://user-images.githubusercontent.com/77688759/161712843-6c725354-c795-45d2-a008-6399d30df46b.png)
![image](https://user-images.githubusercontent.com/77688759/161712899-18bfe7d8-1454-483e-8d09-73bb2959b47e.png)

now search for drive api and enable it.

![image](https://user-images.githubusercontent.com/77688759/161713016-ebf934d5-e0a4-45b2-80f1-229f655feddb.png)
![image](https://user-images.githubusercontent.com/77688759/161713088-518e509c-340a-4786-9bd2-2d079e461f31.png)
![image](https://user-images.githubusercontent.com/77688759/161713346-688ebc8c-7335-4de8-8f6c-3ce75dc6a06b.png)

after enabling drive api
goto your oauth sonsent screen

![image](https://user-images.githubusercontent.com/77688759/161714067-b246af4e-d537-43cd-9604-88fc04c457a6.png)
![image](https://user-images.githubusercontent.com/77688759/161714348-7329c817-a7b3-40b3-b8b1-a51df465aae7.png)
![image](https://user-images.githubusercontent.com/77688759/161714421-3f64cc16-b1e3-4078-abdb-0f58e4a81113.png)
![image](https://user-images.githubusercontent.com/77688759/161714503-5d7cd60b-2a29-4b19-83c1-e409ebf22639.png)
![image](https://user-images.githubusercontent.com/77688759/161714557-6e35f134-fd76-4f3b-a22f-84df9b201c5f.png)
![image](https://user-images.githubusercontent.com/77688759/161714611-b6a066e0-820c-48f4-8591-90cbcc8774d0.png)
![image](https://user-images.githubusercontent.com/77688759/161714665-9acaf68f-a9de-4ab7-8e7f-e64d8db81cb1.png)
![image](https://user-images.githubusercontent.com/77688759/161714725-63cc7c7b-0473-4d47-b7a4-545a8eae1c8b.png)
![image](https://user-images.githubusercontent.com/77688759/161715003-997b25af-53d8-43a4-a25f-171ee4c0d50b.png)
![image](https://user-images.githubusercontent.com/77688759/161715060-4107aa1c-8f79-4e14-bcda-5c7dd7355892.png)
![image](https://user-images.githubusercontent.com/77688759/161715135-b6ccae58-eb01-40dd-989a-9b85df56e9dd.png)
![image](https://user-images.githubusercontent.com/77688759/161715506-734544a8-38d6-41fc-89a3-6ea25ee03e52.png)
![image](https://user-images.githubusercontent.com/77688759/161715635-5a915180-18b7-4487-b3d7-d9683c65d599.png)
![image](https://user-images.githubusercontent.com/77688759/161715762-dad89c26-6b64-46c6-a5ac-9eac373658cc.png)

and done now download your .json file 

![image](https://user-images.githubusercontent.com/77688759/161715944-34b24641-a2b9-4236-8f97-b1a292e5e3e5.png)

after download rename it to `credentials.json`
Now move that credentials.json file to the extracted repo folder

![image](https://user-images.githubusercontent.com/77688759/161720299-4ee43d15-f136-41e0-b5f7-2bb822429999.png)

we are done with the credentials.json file.

</details>
  
## Create token.pickel

<details>
  
  <summary>Click Here</summary>
  
for genrating token.pickel you will need python
so install python from this link [Here](https://www.python.org/downloads/)
while installing, make sure thagt `add to the path` option is selected.
onced installed, open cmd and type `python --version` to make that you have installed python correctly.
  
![image](https://user-images.githubusercontent.com/77688759/161721207-223e78f8-d9dc-4b76-9314-0fe76d5bc109.png)

ok, now goto your extracted folder click on the address bar and type cmd then hit enter.
  
![image](https://user-images.githubusercontent.com/77688759/161721454-52142434-4f3e-44b5-a3f5-7f0fd9b4f03f.png)
![image](https://user-images.githubusercontent.com/77688759/161721551-cf5d24b4-b518-4245-997b-a5b72409ed1e.png)
![image](https://user-images.githubusercontent.com/77688759/161721614-1a1af809-229c-49df-9f85-64f33debd543.png)

there you go.
now give command
`pip install google-api-python-client google-auth-httplib2 google-auth-oauthlib`

now make sure to set a default browser, in my case chrome is the default.

then run
`python generate_drive_token.py`

one browser window will open the follow the on screen prompt
  
![image](https://user-images.githubusercontent.com/77688759/161724909-723eac9b-3caa-46bf-803c-4dd0c42b3642.png)
![image](https://user-images.githubusercontent.com/77688759/161724965-ba3068e6-720e-4331-9b71-a890cb8e8731.png)
![image](https://user-images.githubusercontent.com/77688759/161725004-91f84911-ea58-426e-a0d4-ea28db5dc54b.png)
![image](https://user-images.githubusercontent.com/77688759/161725045-d16bcb9c-1f4b-49e0-a18e-af7e6dc66103.png)

now after you reach this screen 
  
![image](https://user-images.githubusercontent.com/77688759/161725108-78da920f-70f8-4f46-9cb7-b2015651cfcf.png)

token.pickel will be available in the ectracted repo folder
  
![image](https://user-images.githubusercontent.com/77688759/161725413-bfd6dc6f-2d0c-4668-98ba-525d73467c65.png)

</details>  

## Create config.env

<details>
  
  <summary>Click Here</summary>
  
go [here](https://github.com/anasty17/mirror-leech-telegram-bot/raw/master/config_sample.env) and copy all the content.
then goto [github gist](https://gist.github.com/)

give your gist a name `config.env`

![image](https://user-images.githubusercontent.com/77688759/161727093-6bac51cf-f26d-46e7-950b-f85700b71be5.png)

and paste the previously copied content here

![image](https://user-images.githubusercontent.com/77688759/161727191-4f5038e8-aaee-49f4-bba7-cbe849386853.png)

now remove line no 2. `_____REMOVE_THIS_LINE_____=True`
then start filling the config values

for now i will only show the necessary values for the proper working of the mirror leech bot.

## BOT_TOKEN
search @BotFather on telegram, start the bot and type `/newbot` then follow on the in screen instruction to create a new bot.

![image](https://user-images.githubusercontent.com/77688759/161728194-f12dd4e5-dab2-426d-a8af-b672ac7d3f69.png)

this will be your BOT_TOKEN

## GDRIVE_FOLDER_ID
search @MSGuite_SD_Creator_Bot on telegram, start the bot click on `genrate td` now send your email address, give your drive a good name for eg `hitesh920's drive` and done.

![image](https://user-images.githubusercontent.com/77688759/161728959-fa766198-0e34-4d4d-bd51-f30f357d7d78.png)

now click here to go to your shared drive you just created.
now copy the root id of your shared drive
for eg https://drive.google.com/drive/folders/xxxxxxxxxxx then the code after `folder/` will be the your root id

![image](https://user-images.githubusercontent.com/77688759/161729686-d9e79a8f-4479-46ae-84dc-1989df4c75f9.png)

this will be the value of GDRIVE_FOLDER_ID 

## OWNER_ID
search @MissRose_bot on telegram, start the bot then type `/id` bot will send your account's id
use that for OWNER_ID

## DOWNLOAD_DIR
keep the default values, no need to change anything here.

## DOWNLOAD_STATUS_UPDATE_INTERVAL
keep the default values, no need to change anything here.

## AUTO_DELETE_MESSAGE_DURATION
keep the default values, no need to change anything here.

## IS_TEAM_DRIVE
set the to `True` as we are using shared drive.

## TELEGRAM_API & TELEGRAM_HASH
got [here](my.telegram.org) register with your number connected to telegram account fill with your number , choose desktop,  fill app title and short name to any name you want.

![image](https://user-images.githubusercontent.com/77688759/161731080-bff37137-e53a-4774-a1bd-6288491ca494.png)

this will give the values of `TELEGRAM_API` and `TELEGRAM_HASH`

<b>App api_id</b> will be your TELEGRAM_API and <b>App api_hash</b> TELEGRAM_HASH

and we are done with the all necessary configs for the proper working of the mirror leech bot.
  
</details>  
