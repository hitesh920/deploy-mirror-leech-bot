## What Are Service Accounts?
- Service accounts can transfer 75 TB per day in shared drive where as normal account can only transfer 750 GB per day in shared drive.

## So How Service Accounts Works?
- Basically 1 project in google cloud console can genrate 100 service accounts
- Consider 1 service account as a normal account but x 100 so there will be 100 accounts to upload stuff
- 1 service/normal account can upload 750 GB per day in a shared drive so 100 service accounts can upload 75 TB pre day (`750 GB per day` x `100 service account` = `75 TB of upload limit`). 

## Create Service Account
- Goto your google cloud console [Click Here](https://console.cloud.google.com/)
- Search for `Identity and Access Management` and enable it.

![image](https://user-images.githubusercontent.com/77688759/162171043-265d8c13-6d84-411b-a660-8d5531eba886.png)
![image](https://user-images.githubusercontent.com/77688759/162171242-319e993d-b556-4cdd-9de5-636564b1cf8d.png)

- Once enabled, wait for 3-4 minutes
- Goto that extracted repo folder, now make sure that credentials.json file is there
- Then open the cmd from that extracted repo folder by typing <b>cmd</b> in the address bar then hit enter.
- Then run `python gen_sa_accounts.py --list-projects`
- One a windows will open in your default browser, just follow the on screen prompt.

![image](https://user-images.githubusercontent.com/77688759/162172650-3afdd3ce-002f-4d22-8273-689c1286b38d.png)
![image](https://user-images.githubusercontent.com/77688759/162172782-5f433420-575c-441f-9c5d-6a486f28eb37.png)
![image](https://user-images.githubusercontent.com/77688759/162172853-0690179c-3dab-43cf-8b8f-fd2151536574.png)
![image](https://user-images.githubusercontent.com/77688759/162173211-d12acf47-b795-4a20-90e6-f1bb135c76f6.png)

- Once your reach this screen, one file named `token_sa.pickle` will generate automatically. We need this file later.

![image](https://user-images.githubusercontent.com/77688759/162173264-b75023a8-8826-4445-9ab4-0002b45b040c.png)

- Now in the cmd window you will see the projects you have in your google cloud console.

![image](https://user-images.githubusercontent.com/77688759/162174163-fc8d55f3-941c-431e-a962-bbe60c03d86e.png)

- That will be your project id, note that project id because we need that in the next commands
- Now run `python gen_sa_accounts.py --enable-services <your project id>`. This command will enable all the services need for creating a service account.
- <b>Note</b>: Replace `<your project id>` with your project id. In my case, my project id is <b>personal-345709</b> so i will run <b>python gen_sa_accounts.py --enable-services personal-345709</b> 

![image](https://user-images.githubusercontent.com/77688759/162174671-a31d0c37-d347-4565-9a99-58f7aa84829b.png)

- Now you have to wait 4-5 minutes. before running the next command.
- After 4-5 minutes, run `python gen_sa_accounts.py --create-sas <your project id>` this will create 100 service accounts in your project

![image](https://user-images.githubusercontent.com/77688759/162175398-9f525136-7bdf-4a40-839f-ffe6bc956cb1.png)

- Now again,  wait for 2-3 minutes before running the next command.
- After 2-3 minutes, run `python gen_sa_accounts.py --download-keys <your project id>` this command will download all the 100 servie account under accounts folder

![image](https://user-images.githubusercontent.com/77688759/162175914-ed42ad68-8c34-413e-bbaf-100f9177f25d.png)

- Done, now if you check accounts folder you will see 100 json files. those are our service accounts.

![image](https://user-images.githubusercontent.com/77688759/162176093-985adcde-4b4d-4739-b623-dbfbe760e055.png)
![image](https://user-images.githubusercontent.com/77688759/162176238-d54c9bd8-0bdd-403c-a4c3-b12ab28b0876.png)

- And done! we have successfully created our 100 service accounts

## Add Service Accounts To Shared Drive.
- Now after creating our service accounts, we need to add them to our shared drive.
- Run `pip install progress`
- Then run `python add_to_team_drive.py -d <shared drive's root id>`. In my case my shared drive's root id is <b>0AD6zA275hmA7Uk9PVA</b> 

![image](https://user-images.githubusercontent.com/77688759/162176870-8b2e5cd6-669f-4e50-80b1-c49379dd7f1a.png)
![image](https://user-images.githubusercontent.com/77688759/162177338-89673e47-2b0b-49d6-a691-051c4dbf590b.png)

- And Done. we have successfully added our service accounts in our shared drive.

## Enable The Use Of Service Accounts For Our Mirror Bot
- Zip the accounts folder.
- Goto your extracted repo folder, right click on the accounts folder then zip the accounts folder using `7zip` software.

![image](https://user-images.githubusercontent.com/77688759/162178293-3d849de2-3eab-47ee-8496-d823d1a2caad.png)
![image](https://user-images.githubusercontent.com/77688759/162181945-40b9e421-f759-487e-a835-875cf5f9acb3.png)

- Then upload that accounts.zip file and token_sa.pickle file to that index folder you created in your google drive in step 3

![image](https://user-images.githubusercontent.com/77688759/162188136-f4d03c5f-7d8d-4b4f-ab43-e0a7b36b3b27.png)

- Now goto your config.env gist, look for `ACCOUNTS_ZIP_URL` var and fill it with the direct download link for your accounts.zip, its the same process you did for your <b>TOKEN_PICKLE_URL</b> in step 4
- You need to use token_sa.pickle instead of token.pickle, update the value for `TOKEN_PICKLE_URL` with the direct download link of your token_sa.pickle
- Then look for `USE_SERVICE_ACCOUNTS` var and set that to `True`

![image](https://user-images.githubusercontent.com/77688759/162179468-7c09fea9-2222-47d5-a909-d2d623161a7f.png)


- Done now just save the config.env gist and do `/restart` in your bot or you can just turn dynos off and on from heroku.


