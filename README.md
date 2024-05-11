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


<img width="772" alt="image" src="https://github.com/Nitish1390/Dockerizing-a-Plain-HTML-Page-with-Nginx/assets/139607834/a96a7e8d-1abd-419d-9fd7-6ea7fbb977c1">


<img width="532" alt="image" src="https://github.com/Nitish1390/Dockerizing-a-Plain-HTML-Page-with-Nginx/assets/139607834/259c02e0-e50f-407c-8ddd-a358ca65b791">


<img width="559" alt="image" src="https://github.com/Nitish1390/Dockerizing-a-Plain-HTML-Page-with-Nginx/assets/139607834/2f199abc-67cf-4584-8df5-aaf13fe7bc2e">






