Running a .NET Solution Locally with Docker using Docker Compose

1️.	Prerequisites
Ensure you have the following installed:
- Docker Desktop for Windows
- Docker Compose

2.	Running the Solution

Start the environment using:

Open powershell and run next command:

 docker compose  -f "<Full-path-to-folder-with code>\docker-compose.yml" -f "<Full-path-to-folder-with code>\docker-compose.override.yml" -p ekovalenkocompose103 --ansi never up -d --build --remove-orphans
 
 
after that in docker Desktop must be   

![GitHub Image](https://raw.githubusercontent.com/evgenkovalenko/images/refs/heads/main/dockercompose-1.png)

 
 
 
7️⃣ Testing the Application
Once the containers are up, you can check if your application is running correctly by making a POST request:
POST http://localhost:25331/match
Content-Type: application/json

{
    "UserId": "userid_1"
}



 
 
 

