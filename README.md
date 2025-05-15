Running a .NET Solution Locally with Docker using Docker Compose

1️.	Prerequisites
Ensure you have the following installed:
- Docker Desktop for Windows
- Docker Compose

2.	Running the Solution

Start the environment using:

Open powershell and run next command:

 docker compose  -f "{Full-path-to-folder-with code}\docker-compose.yml" -f "{Full-path-to-folder-with code}\docker-compose.override.yml" -p ekovalenkocompose103 --ansi never up -d --build --remove-orphans
 
After that in Docker Desktop must be created next containers  

![GitHub Image](https://raw.githubusercontent.com/evgenkovalenko/images/refs/heads/main/dockercompose-1.png)

 
  
3. Testing the Application
Once the containers are up, you can check if your application is running correctly by making a POST request:

![GitHub Image](https://raw.githubusercontent.com/evgenkovalenko/images/refs/heads/main/AddMatchingSearch-2.png)

CMD :
curl -X POST http://localhost:25331/match -H "Content-Type: application/json" -d "{\"UserId\":\"userid_1\"}"

For Matchmaking.Service application port 25331 was set in docker-compose.yml configuration, so it will be static.


To retreive match information can be used browser, postman    

![GitHub Image](https://raw.githubusercontent.com/evgenkovalenko/images/refs/heads/main/RetreiveMatchingResult-3.png)

OR CMD

curl -X GET "http://localhost:25331/match?userId=userid_1" -H "Accept: application/json"


4. To check application logs can be used Docker Desktop functionality :

![GitHub Image](https://raw.githubusercontent.com/evgenkovalenko/images/refs/heads/main/ServicesLogs-4.png)




 
 
 

