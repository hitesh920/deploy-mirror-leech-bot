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
