- Now Clone that repo in your vps.

![image](https://user-images.githubusercontent.com/77688759/172315040-d05d0e0f-2105-43e6-b5b8-a266350b4ba9.png)

- You need to install docker and other packages. Give this command
  
```
wget https://github.com/ghostmirrorlab/scripts/raw/main/docker.sh
```
  
![image](https://user-images.githubusercontent.com/77688759/172317282-297f28bc-36cd-40dc-aedb-c628979f9134.png)

- Now bash the sh file using this command
  
```
bash docker.sh
```
  
press `y` if asked for confirmation. and wait for the process to complete, it might takes few minutes.
  
- And we are dont with setting up the vps.
  
</details>  

### Step 6: Deploy Bot

<details>
  
  <summary>Click Here</summary>
  
<br>  

- We need to build the docker first. Use this command
  
```
sudo docker build . -t mirror-bot
```
  
- After docker build successfully. 
  
![image](https://user-images.githubusercontent.com/77688759/172319463-8ac8026d-9b8a-470f-8daf-bb8a3e57d15b.png)
  
- You just need to run the docker by this command
  
```
sudo docker run mirror-bot
  
```
  
![image](https://user-images.githubusercontent.com/77688759/172320658-a70964f8-86c7-4318-8fb7-8d944271189e.png)
  
here i haven't uploaded my token.pickel and my config.env thats why its showing like this. but if you do all the steps properly this it should show something like this
  
![image](https://user-images.githubusercontent.com/77688759/172320895-529da55d-30d7-48b8-948f-9c04ebbb916e.png)

- And done, congratulations.
