# Deploy Mirror Leech Bot

## Requirements

- Telegram Account.
- Heroku Account.
- Github Account.
- Install Python on Windows.
- Google Drive Account.

## Repo Link: [Here](https://github.com/anasty17/mirror-leech-telegram-bot)

In this guide, we will deploy our mirror bot on heroku using github action. keep this thing in mind that deploying mirror bot on heroku may result in suspension of the heroku account. <br>
If you starting fresh, then this guide will easily take your 1-2 hours.

<b>Ok then lets start</b>.

- First thing first, goto bot repo [Click Here](https://github.com/anasty17/mirror-leech-telegram-bot) and fork the bot repo.

![image](https://user-images.githubusercontent.com/77688759/161710615-c450b852-6acc-481b-a84f-5b3d054b6b05.png)

- Now download that repo.

![image](https://user-images.githubusercontent.com/77688759/161710894-b2840ddf-c186-4a9f-bcb0-e301ffd2d253.png)

- The downloaded repo will be in zip file, so extract it.

### Step 1: Create credentials.json

<details>
  
  <summary>Click Here</summary>

<br>
  
- Goto your google cloud console. [Click Here](https://console.cloud.google.com)
- Create a new project (if you already have a project then no need to create another one)

![image](https://user-images.githubusercontent.com/77688759/161712563-4a2e83ab-b2ba-4134-8d92-cef8e2c09af2.png)
![image](https://user-images.githubusercontent.com/77688759/161712650-1f2b0f7b-0a74-4527-a699-3e09feea2d3a.png)

- Now select the project you just create.

![image](https://user-images.githubusercontent.com/77688759/161712843-6c725354-c795-45d2-a008-6399d30df46b.png)
![image](https://user-images.githubusercontent.com/77688759/161712899-18bfe7d8-1454-483e-8d09-73bb2959b47e.png)

- Now search for drive api and enable it.

![image](https://user-images.githubusercontent.com/77688759/161713016-ebf934d5-e0a4-45b2-80f1-229f655feddb.png)
![image](https://user-images.githubusercontent.com/77688759/161713088-518e509c-340a-4786-9bd2-2d079e461f31.png)
![image](https://user-images.githubusercontent.com/77688759/161713346-688ebc8c-7335-4de8-8f6c-3ce75dc6a06b.png)

- After enabling drive api, goto your oauth consent screen `cloud console home screen` > `hamburger menu on the left` > `api and services` > `oauth consen screen`

![image](https://user-images.githubusercontent.com/77688759/161765925-c5a9efd6-f24a-4d7f-b335-7e798ddffffe.png)
![image](https://user-images.githubusercontent.com/77688759/161714348-7329c817-a7b3-40b3-b8b1-a51df465aae7.png)
![image](https://user-images.githubusercontent.com/77688759/161714421-3f64cc16-b1e3-4078-abdb-0f58e4a81113.png)
![image](https://user-images.githubusercontent.com/77688759/161714503-5d7cd60b-2a29-4b19-83c1-e409ebf22639.png)
![image](https://user-images.githubusercontent.com/77688759/161714557-6e35f134-fd76-4f3b-a22f-84df9b201c5f.png)
![image](https://user-images.githubusercontent.com/77688759/161714611-b6a066e0-820c-48f4-8591-90cbcc8774d0.png)
![image](https://user-images.githubusercontent.com/77688759/161714665-9acaf68f-a9de-4ab7-8e7f-e64d8db81cb1.png)
![image](https://user-images.githubusercontent.com/77688759/161714725-63cc7c7b-0473-4d47-b7a4-545a8eae1c8b.png)
![image](https://user-images.githubusercontent.com/77688759/161715003-997b25af-53d8-43a4-a25f-171ee4c0d50b.png)
  
- Once the oauth consent screen app is published, now we can create the credentials.json
  
![image](https://user-images.githubusercontent.com/77688759/161715060-4107aa1c-8f79-4e14-bcda-5c7dd7355892.png)
![image](https://user-images.githubusercontent.com/77688759/161715135-b6ccae58-eb01-40dd-989a-9b85df56e9dd.png)
![image](https://user-images.githubusercontent.com/77688759/161715506-734544a8-38d6-41fc-89a3-6ea25ee03e52.png)
![image](https://user-images.githubusercontent.com/77688759/161715635-5a915180-18b7-4487-b3d7-d9683c65d599.png)
![image](https://user-images.githubusercontent.com/77688759/161715762-dad89c26-6b64-46c6-a5ac-9eac373658cc.png)

- And done now download your .json file. 

![image](https://user-images.githubusercontent.com/77688759/161715944-34b24641-a2b9-4236-8f97-b1a292e5e3e5.png)

- After download rename it to `credentials.json`
- Make sure you have enabled "file name extensions"
  
![image](https://user-images.githubusercontent.com/77688759/161918765-1f570e63-3492-4d97-a5f9-720f0915b8a8.png)
  
- Most users basically rename credentials.json to credentials.json.json
- Make sure that its credentials.json and not credentials.json.json.  
  
- Now move that credentials.json file to the extracted repo folder.

![image](https://user-images.githubusercontent.com/77688759/161720299-4ee43d15-f136-41e0-b5f7-2bb822429999.png)

- We have sucessfully created our credentials.json file.

</details>
  
### Step 2: Create token.pickle

<details>
  
  <summary>Click Here</summary>
 
<br>  
  
- For genrating token.pickle you will need python.
- So install python from this link [Click Here](https://www.python.org/downloads/). (while installing, make sure that `add to the path` option is selected.)
- Once installed, open cmd and run `python --version` to make that you have installed python correctly.
  
![image](https://user-images.githubusercontent.com/77688759/161721207-223e78f8-d9dc-4b76-9314-0fe76d5bc109.png)

- Ok, now goto your extracted repo folder click on the address bar and type cmd then hit enter.
  
![image](https://user-images.githubusercontent.com/77688759/161721454-52142434-4f3e-44b5-a3f5-7f0fd9b4f03f.png)
![image](https://user-images.githubusercontent.com/77688759/161721551-cf5d24b4-b518-4245-997b-a5b72409ed1e.png)
![image](https://user-images.githubusercontent.com/77688759/161721614-1a1af809-229c-49df-9f85-64f33debd543.png)

- There you go.
- Now give command
`pip install google-api-python-client google-auth-httplib2 google-auth-oauthlib`
- Now for the next command make sure to set a default browser, in my case chrome is the default.
- Then run
`python generate_drive_token.py`
- One browser window will open, just follow the on screen prompt.
  
![image](https://user-images.githubusercontent.com/77688759/161724909-723eac9b-3caa-46bf-803c-4dd0c42b3642.png)
![image](https://user-images.githubusercontent.com/77688759/161724965-ba3068e6-720e-4331-9b71-a890cb8e8731.png)
![image](https://user-images.githubusercontent.com/77688759/161725004-91f84911-ea58-426e-a0d4-ea28db5dc54b.png)
![image](https://user-images.githubusercontent.com/77688759/161725045-d16bcb9c-1f4b-49e0-a18e-af7e6dc66103.png)

- Now after you reach this screen.
  
![image](https://user-images.githubusercontent.com/77688759/161725108-78da920f-70f8-4f46-9cb7-b2015651cfcf.png)

- token.pickle will be available in the extracted repo folder.
  
![image](https://user-images.githubusercontent.com/77688759/161725413-bfd6dc6f-2d0c-4668-98ba-525d73467c65.png)

</details>  

### Step 3: Hosting token.pickle

<details>
  
  <summary>Click Here</summary>
  
<br>
  
- Now we need to host our token.pickle 
- For that we will use google drive index.
- This is the [repo](https://gitlab.com/ParveenBhadooOfficial/Google-Drive-Index) we will be using for our google drive index.
- Go to [this](https://bdi-generator.hashhackers.com/) link.
- Sign in to get the Authentication Code.
  
![image](https://user-images.githubusercontent.com/77688759/161735755-06598ea0-0683-4a46-932c-02f1047721cb.png)
![image](https://user-images.githubusercontent.com/77688759/161735885-5fd3e64b-9e1b-4b0e-99d0-2b045055d13b.png)
![image](https://user-images.githubusercontent.com/77688759/161735955-afaad737-526c-4d3d-81c8-aa3eee18dc9d.png)
![image](https://user-images.githubusercontent.com/77688759/161736007-c3719cd2-0669-4eba-9632-573b4a4f6138.png)

- Paste that code in `Authentication Code` var.

![image](https://user-images.githubusercontent.com/77688759/161736264-f68a9e54-e495-4a16-aaea-351334164ff0.png)

- For `Site Name` var, you can give any name for eg `personal`.
- For `Share Drive ID or root` var, goto your drive and create a new folder for your index (don't create this folder in the shared drive).

![image](https://user-images.githubusercontent.com/77688759/161736709-0adeca7d-f0d1-4caf-813a-a320822bdfe4.png)

- Go inside that folder and copy the id of that folder.

![image](https://user-images.githubusercontent.com/77688759/161736798-f24dda46-9f26-4724-bdcf-3601a19c70ba.png)

- Use it for `Share Drive ID or root` var.

![image](https://user-images.githubusercontent.com/77688759/161736899-c38cfa61-e55f-423e-a747-d169f6d31eab.png)

- Then click on submit and copy the genrated code for your index.

![image](https://user-images.githubusercontent.com/77688759/161737009-ea620aef-7e44-436a-b84e-d6d5e6143daa.png)

- Now goto [cloudflare](https://www.cloudflare.com/) and sign up for an account.
- Then goto  `workers`

![image](https://user-images.githubusercontent.com/77688759/161737351-e2324694-a145-4a14-850b-43f3e718d024.png)
![image](https://user-images.githubusercontent.com/77688759/161737457-28bedba5-5e0b-4c53-84d9-89629a0467a6.png)
![image](https://user-images.githubusercontent.com/77688759/161737508-e8021e09-89ef-4da9-bb5e-1e8b2a58a6dc.png)

- Then complete the verification process and come back to the `workers` section again.

![image](https://user-images.githubusercontent.com/77688759/161737755-d5475d08-0b2d-4b32-8b63-a6c57674f7b6.png)
![image](https://user-images.githubusercontent.com/77688759/161737848-9cbc23d0-edeb-424c-a9e5-73bbb8480b23.png)
![image](https://user-images.githubusercontent.com/77688759/161737948-9c5f1dc2-5a81-4e71-8721-de03fe813b99.png)

- Remove all the default content from here.

![image](https://user-images.githubusercontent.com/77688759/161738144-1f6c94c6-7753-459d-8fe3-0ceb2d60ece0.png)

- And paste the code u genrated for your index then click on `save and deploy`.

![image](https://user-images.githubusercontent.com/77688759/161738371-a344f75a-da78-49a3-ac30-2bd886df9b50.png)
![image](https://user-images.githubusercontent.com/77688759/161738430-03e9d198-c810-457c-8315-db54b900b5c3.png)

- Now wait for 10 seconds your index will be online.
- Then go here and save the link for your index, it will come handy later.  
  
![image](https://user-images.githubusercontent.com/77688759/161738546-de13a74a-36cf-4949-b13e-74a650681f8f.png)  

- Now goto that drive folder u create for the index and upload your token.pickle 

![image](https://user-images.githubusercontent.com/77688759/161742717-3864b06b-8715-4799-bf77-7267bef39725.png)

- Then open your index link click on `drive one` you will see your token.pickle file u just uploaded.

![image](https://user-images.githubusercontent.com/77688759/161739501-b250a124-5d75-45f2-8b5b-e10091cb7635.png)
![image](https://user-images.githubusercontent.com/77688759/161742804-90ebd60c-1f4f-48ff-8b99-7755a9fc2ffc.png)

- We successfully hosted our token.pickle in our index. (Just dont share this index link, as it has confidential file.)

  </details>

### Step 4: Create config.env

<details>
  
  <summary>Click Here</summary>
  
<br>
  
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
- Go to your index link and click on the token.pickle u just hosted in step 3 and copy the direct download link.
  
![image](https://user-images.githubusercontent.com/77688759/161749786-d71ab726-51b9-49b7-9dae-b584cd3177e2.png)

- And use that url for TOKEN_PICKLE_URL

<b>BASE_URL_OF_BOT</b>:
- https://yourappname.herokuapp.com, suppose if your heroku app name will be `hitesh920-mirrorbot` then the BASE_URL_OF_BOT will be `https://yourappname.hitesh920-mirrorbot.com`

- We are done with the all necessary configs for the proper working of your mirror leech bot.
- It should look like this after filling all the necessary values
  
![image](https://user-images.githubusercontent.com/77688759/161732551-fe9424b4-d141-481c-9de3-d0cb368c1c96.png)

- Then click on create secret gist to save the gist.
  
![image](https://user-images.githubusercontent.com/77688759/161732712-6c3741ac-494b-496d-8fea-3ae21fc8ef3f.png)

- We have successfully created our config.env
  
</details>
  
### Step 5: Setting Up Secrets For Github Action

<details>
  
  <summary>Click Here</summary>
  
<br>
  
- Goto your forked repo > settings > secrets > action

![image](https://user-images.githubusercontent.com/77688759/161750596-e539db44-2a42-4ac9-bc0d-b593777f84ee.png)
![image](https://user-images.githubusercontent.com/77688759/161753272-ddad44c9-2c98-40d0-b06a-67027ab222dd.png)

<b>Now here under secrets, you need to create four secrets</b> 
- HEROKU_EMAIL
- HEROKU_API_KEY
- HEROKU_APP_NAME
- CONFIG_FILE_URL

![image](https://user-images.githubusercontent.com/77688759/161753685-a8e1da3a-8647-4f71-8221-b8d83c9977d8.png)
![image](https://user-images.githubusercontent.com/77688759/161753909-6b6c8c59-7d8a-4920-88e4-53d212099efe.png)

<b>Do the same for other three secrets.</b>

### HEROKU_API_KEY
- Goto your heroku account settings [Here](https://dashboard.heroku.com/account)
- Scroll down and copy thr api key

![image](https://user-images.githubusercontent.com/77688759/161752797-4a3c4798-352e-4c33-af23-ac0b5b9af3bf.png)

### HEROKU_APP_NAME:
- Name you would like to give to your heroku app (must be unique)

### CONFIG_FILE_URL:
- Goto that gist you created for the config.env

- Then click on raw
  
![image](https://user-images.githubusercontent.com/77688759/161732830-d9489120-9d3c-4f74-8619-8c1fb94b8478.png)

- And copy the url then remove the commit id
- For eg `https://gist.githubusercontent.com/ghostmirrorlab/f9b1e6xxxxxxxxxxxxxaaac04520/raw/200d4a93e0eb5ee8d4b0e5a377ce0396a131843e/config.env` then the commit id will the one after `raw/` and before `/config.env`


`original config.env url`:<br> 
https://gist.githubusercontent.com/ghostmirrorlab/f9b1e6xxxxxxxxxxxxxaaac04520/raw/200d4a93e0eb5ee8d4b0e5a377ce0396a131843e/config.env

`url after removing commit id`:<br>
https://gist.githubusercontent.com/ghostmirrorlab/f9b1e6xxxxxxxxxxxxxaaac04520/raw/config.env

- After removing the commit id use that url for the CONFIG_FILE_URL
- Once all the four secrets have been added, it should look like this

![image](https://user-images.githubusercontent.com/77688759/161755355-afcda2b7-3fb1-4e52-8876-162932213e40.png)

- And we are done with the action secrets.
  
</details>  

### Step 6: Deploy Bot

<details>
  
  <summary>Click Here</summary>

We will use github action to deploy bot. 
  
- Goto your `forked repo` > `action` 

![image](https://user-images.githubusercontent.com/77688759/161756057-44ec2639-8519-47ea-ac9f-e0d78bdd7d78.png)
![image](https://user-images.githubusercontent.com/77688759/161756181-1abf90aa-a540-4594-a7ca-6d6bbf946f19.png)
![image](https://user-images.githubusercontent.com/77688759/161756250-8f6cbf90-bedb-4bb5-8884-ee8bb9da120a.png)
![image](https://user-images.githubusercontent.com/77688759/161756350-05bb6617-4c36-4133-915f-ee460cc1046e.png)
![image](https://user-images.githubusercontent.com/77688759/161756393-a5c09aaf-2e9b-4e81-a009-d11715eb1dad.png)

- Now your workflow will start, deploy will take arround 3-4 minutes.
- You can check the workflow logs at

![image](https://user-images.githubusercontent.com/77688759/161756625-5d687723-c6a1-4bd7-b74e-8e2f27fe6611.png)
![image](https://user-images.githubusercontent.com/77688759/161756690-acff8feb-f84d-4424-ae67-9812dc2cc4b1.png)
![image](https://user-images.githubusercontent.com/77688759/161756737-0d68d550-ec89-42f4-a95d-9b023d69fa82.png)
  
- Once deployment done

![image](https://user-images.githubusercontent.com/77688759/161757135-f49d1799-a564-4688-a5e8-3adf879691e3.png)

- Goto your heroku account, click on the app you just created then click on more and then click on view logs.

![image](https://user-images.githubusercontent.com/77688759/161757321-d591434d-a54d-47c9-9270-c40ac314e075.png)
![image](https://user-images.githubusercontent.com/77688759/161757417-e7205bb8-8bf2-43f2-a392-5affed3e2c8c.png)

- Wait for few seconds your bot will start if your config.env is correct.

![image](https://user-images.githubusercontent.com/77688759/161757509-937e2389-a704-43c6-8862-f9444b525304.png)

- Now search the username of the bot u created with @BotFather and start the bot

![image](https://user-images.githubusercontent.com/77688759/161757727-e0a45cad-cf5a-4dd3-a1cc-a93adf2bf3b9.png)

- And done, congratulations.

</details>

### Extra:

- If you facing error while deploying or have any other doubt then you can ask for help at [@mirrorsociety](https://t.me/mirrorsociety) by tagging @hitesh920.
- If you want to update your bot then just do `/restart` or you can also turn dynos off and on from your heroku app.
- If you want to update config.env then goto your config.env gist > edit > save > then `/restart` the bot.
- If you want to redeploy the just follow the step 6 and start the workflow again.
- To know more about all the optional configs then read the README.md file of the bot repo.
- To set bot commands, then you can use @BotFather using `/setcommands`. All the commands are listed in the README.md file of the bot repo.


## Credits
 
 - [Anasty](https://github.com/anasty17) for the mirror leech bot repo.
 - [ParveenBhadooOfficial](https://gitlab.com/ParveenBhadooOfficial) for the google drive index.
