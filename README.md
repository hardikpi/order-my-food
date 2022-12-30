# OrderMyFood

An online food ordering system developed using MEAN (MongoDB, ExpressJS, Angular, NodeJS) with jwt authentication enabled and password encrypted.
  
Live Demo: https://food.devopshardik.ml/

## How to run the application?

  ### Prerequisites:
  - Node LTS version
  - git
  - Angular CLI

  1. Clone the repository in your local machine.
  2. Navigate to 'client' directory and run the command 'npm i'. Do the same for 'server' directory.
  3. Navigate to 'server' directory , create a file named '.env'.
  4. Inside the '.env' file, add your mongodb remote string as 'DB_CONNECTION' and a secret key (any string) for your jwt token as 'SECRET_KEY' (refer this file - https://github.com/hardikpi/order-my-food/blob/main/server/.env.example )
  5. Go to your atlas mongodb, create a new collection called 'hotels' under the database that you created and copy the contents of the hotel details from here - https://github.com/hardikpi/order-my-food/tree/main/client/src/assets/api/data.json and insert it in your 'hotels' collection.
  6. Run the command 'node server' from the 'server' directory and navigate to your localhost url, i did it on 8080 port, so localhost:8080
  7. Now, you should see the application running in your browser.

## How to make any changes in the UI?

### To make changes and verify it locally
  
  1. Go to `server.js`, uncomment the lines from 10 to 14 and comment out the lines from 18 to 26.
  2. Save the changes and run `node server` under the `server` directory.
  3. Go to `client/src/environments/environment.ts`, comment out the line no. 8 and uncomment line 7.
  4. Do whatever changes you want in the application and save it.
  5. Run the command `ng serve` under the `client` directory.
  6. Open the localhost URL shown in your terminal.
  7. Now, you should see the changes that you made in the application.
  
### To run the changes in the production environment

  1. Once the changes that you made are okay for you, go to `client/src/environments/environment.ts`, uncomment line no. 8 and comment out the line 7.
  2. Save the changes and run the command `ng build --prod` in the `client` directory.
  3. After the successful build, replace the contents of the `public` folder under the `server` directory with the contents of `dist/order-my-food` in the `client` directory.
  4. Go to `server.js`, comment out the lines from 10 to 14 and uncomment the lines from 18 to 26.
  4. Run the command `node server` under the `server` directory.
  5. Open the localhost URL shown in your terminal.
  6. Now, you can verify the changes that you made and deploy it wherever you want.

### To make it containerize

	1. Make a Dockerfile as per requirement.
	2. Install cli and attach IAM role to that Ec2 instance.
	3. Install docker and Build the docker image with docker file.
	4. Upload the image Amazon Elastic container Registry.
	5. Go to Elastic Container Service and Create a Cluster.
	6. Create a task defination and run a service which include this particular container in it.
	7. Attach the Application Load Balancer with the Elastic Container Service.
	8. Hit the load balancer url with the port you are running your service.
	
### 	To Make CI/CD using Codepipeline

	1. Create a code Pipeline in AWS Codepipeline.
	2. Create Appspec file and push it in Repo.
	3. Create deployment group also IAM role for CodeDeploy.
	4. Build a Pipeline with the stages Source, Build and Deploy for CI/CD.
	

## Screenshots

- **Minimalist Registration and Login Page**
  https://github.com/hardikpi/order-my-food/blob/main/Screenshot%20from%202022-12-30%2019-04-15.png
  
  https://github.com/hardikpi/order-my-food/blob/main/Screenshot%20from%202022-12-30%2019-04-45.png
  
  https://github.com/hardikpi/order-my-food/blob/main/Screenshot%20from%202022-12-30%2019-18-02.png
  
- **Home Page having list of hotels**
	https://github.com/hardikpi/order-my-food/blob/main/Screenshot%20from%202022-12-30%2019-18-09.png
	
	
- **Individual Hotel Page having list of menus - we can add the menus to the cart**
	https://github.com/hardikpi/order-my-food/blob/main/Screenshot%20from%202022-12-30%2019-18-23.png

- **Adding menus to the basket/cart**
	https://github.com/hardikpi/order-my-food/blob/main/Screenshot%20from%202022-12-30%2019-18-30.png

	https://github.com/hardikpi/order-my-food/blob/main/Screenshot%20from%202022-12-30%2019-18-42.png
	
- **Basket of menus**
	https://github.com/hardikpi/order-my-food/blob/main/Screenshot%20from%202022-12-30%2019-18-57.png


- **Payment acknowledgement**
	https://github.com/hardikpi/order-my-food/blob/main/Screenshot%20from%202022-12-30%2019-19-15.png

- **Order History**
	https://github.com/hardikpi/order-my-food/blob/main/Screenshot%20from%202022-12-30%2019-27-48.png
