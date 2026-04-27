Follow the below steps. refer the commits/folders for code.
Step 1: Create Project Folder
  Open Terminal / Command Prompt
  mkdir microservices-docker
  cd microservices-docker
Step 2: Create Folder Structure
  Create folders for services.
  mkdir user-service
  mkdir product-service
Project structure:
microservices-docker
│
├── user-service
│ ├── app.js
│ ├── package.json
│ └── Dockerfile
│
├── product-service
│ ├── app.js
│ ├── package.json
│ └── Dockerfile
│
└── docker-compose.yml
Step 3: Create User Service
  Move into folder
  cd user-service
  npm init -y
  npm install express
Step 4: Write User Service Code in app.js (create a new file inside user-service folder)
Step 5: Create Dockerfile for User Service
  Create file by name Dockerfile inside user-service folder and write the docker code in it

Step 6: Create Product Service
  Move back to main folder
  cd ..
  cd product-service
  npm init -y
  npm install express
Step 7:  Write Product Service Code in app.js (create a new file inside product-service folder) 
Step 8: Create Dockerfile for Product Service
  Create file by name Dockerfile inside product-service folder and write the docker code in it
Step 9: Create Docker Compose File
  Go back to main folder using cd ..
  Create a file by name docker-compose.yml and write the yaml code

Step 10: Build and Run Containers
  Run command
  docker-compose up --build
  look for the output in terminal as below:
    Building user-service
    Building product-service
    Creating microservices-docker_user-service_1
    Creating microservices-docker_product-service_1
    User service running on port 3001
    Product service running on port 3002
Step 11: Test Services in Browser or Postman
Test User Service
http://localhost:3001/users
Output
[
{ "id":1, "name":"Alice"},
{ "id":2, "name":"Bob"}
]
Test Product Service
http://localhost:3002/products
Output
[
{ "id":1, "name":"Laptop"},
{ "id":2, "name":"Phone"}
]
