# Udagram  [![HagarMohsen](https://circleci.com/gh/HagarMohsen/UdagramProject.svg?style=shield)](https://app.circleci.com/pipelines/gh/HagarMohsen/UdagramProject)



This application represents a social media app for posting photos like instagram. The application includes all the major components of a Full-Stack web application.
The app is hosted on Amazon AWS, and it uses the services: Elastic Beanstalk to host the server, along with S3 service to host both: the Photos and the Static website of HTML, JS, and CSS, it also uses the RDS service to hold all the application data.
Tha app is linked with Circleci ti insure that every change and update in code will be deplyed automatically.

## Live Preview
**You can access it by visiting the following Link:  [Udagram-API](http://myudagram-560402809124-bucket.s3-website-us-east-1.amazonaws.com)**

![Live Preview](https://user-images.githubusercontent.com/74413831/153217747-4965889b-2b76-4fa9-89ae-1eeac1e3f610.png)


## Overview

### RDS
![RDS](https://user-images.githubusercontent.com/74413831/153218232-a604aeb8-c68e-4bfe-a90d-f0eae6a7e61e.png)

### S3 Bucket
![Bucket](https://user-images.githubusercontent.com/74413831/153217801-cab78e04-c0ee-486e-96cd-2b9b2a233176.png)

### Elastic Beanstalk Environment
![EB](https://user-images.githubusercontent.com/74413831/153218085-f5d50dc8-b188-440c-b8e5-ff087d393a26.png)

### Success Pipeline
![Success Pipeline](https://user-images.githubusercontent.com/74413831/153218446-ee1ec08f-d470-4837-9bd0-6fd364fd90ad.png)


### Pipeline Environment Variables
![env](https://user-images.githubusercontent.com/74413831/153218512-54abfa3b-5f35-41ee-9215-3597b2cd8eed.png)

## Project Infrastructure
1. RDS that hosts the postgres DB which is built using postgres.
1. S3 Bucket that hosts both: The photos posted by the user and the frontend which is built using Angular framework.
1. Elastic Beanstalk that hosts the backend which is built using Node.js and Express.js in typescript.

![Project Infrastructure](https://user-images.githubusercontent.com/74413831/153284799-8aa9b13d-1595-456e-a439-10d83a632473.png)

## Pipeline Infrastructure
Whenever the developer pushes any code update the pipeline will be triggered.
1. CircleCi is triggered to start the build.
1. Checkout the code from the repository.
1. Install AWS & Elastic Beanstalk CLI.
1. Configure AWS Credentials.
1. Install frontend dependencies.
1. Install backend dependencies.
1. Build frontend.
1. Build backend.
1. Deploy frontend to S3.
1. Deploy backend to Elastic Beanstalk.
1. sit the eb environment variables.

![Pipeline Infrastructure](https://user-images.githubusercontent.com/74413831/153284808-87056606-3f46-4be4-96da-3f87bf75dae1.png)


## Dependencies

```
- Node v14.15.1 (LTS) or more recent. While older versions can work it is advisable to keep node to latest LTS version

- npm 6.14.8 (LTS) or more recent, Yarn can work but was not tested for this project

- AWS CLI v2, v1 can work but was not tested for this project

- A RDS database running Postgres.

- A S3 bucket for hosting uploaded pictures.

```

## Installation

### Install AWS CLI
Followed the instructions from [AWS CLI installation guide](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html).

### Install Elastic Beanstalk CLI
Followed the instructions from this [Github Repo](https://github.com/aws/aws-elastic-beanstalk-cli-setup).

### Create a new Elastic Beanstalk Application
you can choose to do so by one of the following ways:
1. The AWS console and you can find the instructions from [AWS develoer guide](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/GettingStarted.CreateApp.html).
1.By using the EB CLI, and you can fined the whole documentations and steps in detailed in the [AWS guidlines](https://www.amazonaws.cn/en/getting-started/tutorials/deploy-app-command-line-elastic-beanstalk/).


### Create a RDS postgres Database
1. **Lunching cloud gate**

![Lunching](https://user-images.githubusercontent.com/74413831/153222363-4229bf73-89c7-4927-8897-9839d673e63b.png)

2. **From AWS console, choose RDS service and then choosing the button: Create Database**

![Create Database](https://user-images.githubusercontent.com/74413831/153222416-96e5f2fb-bbc0-4010-bcaa-fc55956a7217.png)

3. **setting options in order as following:**

![options1](https://user-images.githubusercontent.com/74413831/153222437-b74f36a5-7aa9-4e9d-bfd3-1f425024f36b.png)

![options2](https://user-images.githubusercontent.com/74413831/153222464-27eff971-a4dd-448d-933b-25e70966791e.png)

![options3](https://user-images.githubusercontent.com/74413831/153222477-1803c8ad-4929-4931-91fc-55a9fae937c5.png)

4. **in the Additional configuration we’ll configure it as following:**

![Additional configuration1](https://user-images.githubusercontent.com/74413831/153222490-83cba02f-bb5c-4708-adb7-9772047ec42c.png)

![Additional configuration2](https://user-images.githubusercontent.com/74413831/153222507-2645ccff-eed7-40d6-8966-bb6a362455c4.png)

5. **After clicking create database, the status will be “creating” till it turns to be “available” and it would be ready to use.**

![using1](https://user-images.githubusercontent.com/74413831/153222538-9b3121cc-adc9-4e8a-8dc6-753f03a423f6.png)

![using2](https://user-images.githubusercontent.com/74413831/153222808-8c48ecbf-a432-482c-b72a-b5cab09a4d84.png)

6. **opening the data base instance and updating the VPC security group:**

![VPC1](https://user-images.githubusercontent.com/74413831/153222831-f0fe9922-299d-43e2-a41a-453eea584342.png)

![VPC2](https://user-images.githubusercontent.com/74413831/153222843-f2915ca9-2ad4-49b5-af07-7d9eefeb8e09.png)

![VPC3](https://user-images.githubusercontent.com/74413831/153222857-f94bccbd-6e5b-4432-a332-536f9d3121e9.png)


7. **Connecting the database by using the Postbird application:**

![Connecting1](https://user-images.githubusercontent.com/74413831/153222902-0275ed63-020b-4f20-a773-e2a7c71c3a04.png)

![Connecting2](https://user-images.githubusercontent.com/74413831/153222872-ebee65aa-8a8a-438b-84fd-edb975ac6335.png)

### Create a new S3 Bucket
1. **From AWS console, choose S3 service and then choosing the button: Create Bucket**

![Create Bucket1](https://user-images.githubusercontent.com/74413831/153236585-46847fd6-3b6d-4c29-bd14-a7a14ad343f4.png)

![Create Bucket2](https://user-images.githubusercontent.com/74413831/153236590-24211547-7789-4d4a-888f-05605e7b3cfb.png)

![Create Bucket3](https://user-images.githubusercontent.com/74413831/153236600-2f04b38b-34d5-48f7-8049-0aad59a229b4.png)

3. **Accessing the created bucket and navigate to the permissions tab and edit the policy:**

![policy1](https://user-images.githubusercontent.com/74413831/153236647-476acbce-bedb-42b3-8e2c-187720b133f2.png)

![policy2](https://user-images.githubusercontent.com/74413831/153236660-9d3c9f80-e0a6-4121-881f-b8683ed181b4.png)

![policy3](https://user-images.githubusercontent.com/74413831/153236676-87e80c82-dfee-4941-99f3-207d6d58cc5c.png)

![policy4](https://user-images.githubusercontent.com/74413831/153236685-c28305ef-45ea-4b39-a84a-3aea2e4b49a1.png)

4. **Configuring the website hosting by navigating to the properties tab**

![Configuring1 configuration1](https://user-images.githubusercontent.com/74413831/153236695-79238704-34a2-4b37-8be7-a9ab943042b8.png)

![Configuring2](https://user-images.githubusercontent.com/74413831/153236708-45b29854-2737-43ce-a459-810972267cbe.png)

![Configuring3](https://user-images.githubusercontent.com/74413831/153236719-3888dd4e-9ae0-42f3-85c3-4ae3ca168fe5.png)


5. **After Saving the changes, you'll be able to maintain the hosted website link**


## Getting Started In your local machine
1. Clone this repo locally into the location of your choice by running the following command:`https://github.com/HagarMohsen/UdagramProject.git`
1. Export the ENV variables needed or use a package like [dotnev] in udagram-api folder and add following line of code:
  1. `POSTGRES_USERNAME=<your_db_user>`
  1. `POSTGRES_PASSWORD=<your_db_password>`
  1. `POSTGRES_DB=<your_db_name>`
  1. `POSTGRES_HOST=<your_db_host>`
  1. `DB_PORT=<your_db_port>`
  1. `PORT=<your_preferred_server_port>`
  1. `JWT_SECRET=<your_jwt_secret>`
  1. `AWS_BUCKET=<your_aws_bucket_name>`
  1. `aws_region=<your_aws_region>`
1. From the root of the repo, navigate udagram-api folder `cd udagram-api` to install the node_modules `npm install`. After installation is done start the api in dev mode with `npm run dev`.
1. Without closing the terminal in step 1, navigate to the udagram-frontend `cd udagram-frontend` to intall the node_modules `npm install`. After installation is done start the api in dev mode with `npm run start`.


## Testing

This project contains two different test suite: unit tests and End-To-End tests(e2e). Follow these steps to run the tests.

1. `cd starter/udagram-frontend`
1. `npm run test`
1. `npm run e2e`

There are no Unit test on the back-end

### Unit Tests:

Unit tests are using the Jasmine Framework.

### End to End Tests:

The e2e tests are using Protractor and Jasmine.

## Built With

- [Angular](https://angular.io/) - Single Page Application Framework
- [Node](https://nodejs.org) - Javascript Runtime
- [Express](https://expressjs.com/) - Javascript API Framework 


