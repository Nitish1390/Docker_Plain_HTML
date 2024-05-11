# Dockerizing-a-Plain-HTML-Page-with-Nginx
Dockerizing a Plain HTML Page with Nginx


Step 1: Install Docker
sudo apt install docker.io -y

Step 2: Create your plain html application
In our case it is .\index.html 

Step 3:
Create a docker file name  Dockerfile

Step 4: Build | Test | Push To ECR

docker build -t plain_html:latest .

docker run -it -d -p 8080:80 plain_html:latest

Step 5 Proceed to push the docker image into your public ECR repository
Use aws configure command to connect your aws cli
AWS Access Key ID:   AWS secret Acess Key:   Default region name: ap-south-1  


Step 6   Use command to tag your local docker image to ECR.
docker tag plain_html:latest public.ecr.aws/c3w1m1q2/plain_html:latest


Step 7 Use command to push the docker image
docker push public.ecr.aws/c3w1m1q2/plain_html:latest


DEPLOYENT IMAGES


Build Image 
![Screenshot 2024-05-11 163353](https://github.com/Nitish1390/Docker_Plain_HTML/assets/139607834/f618c4fd-3ba6-4e71-acb2-4ad35dd14750)


ECR Iamge 

<img width="689" alt="image" src="https://github.com/Nitish1390/Docker_Plain_HTML/assets/139607834/a2c179cc-1120-47d4-8b11-5e1e66d1479a">

ECR Push

![Screenshot 2024-05-11 170111](https://github.com/Nitish1390/Docker_Plain_HTML/assets/139607834/9e2bd370-7ad6-45eb-9d41-b2ddb25e4254)

App Image

![image](https://github.com/Nitish1390/Docker_Plain_HTML/assets/139607834/3c15ec92-a5de-4e5c-8e5c-9bbbfa5a293b)


