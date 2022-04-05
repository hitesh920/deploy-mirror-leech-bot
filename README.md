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
</details>
