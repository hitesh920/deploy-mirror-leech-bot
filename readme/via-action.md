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
- Scroll down and copy the api key

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
