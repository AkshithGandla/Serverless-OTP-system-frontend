# Serverless-OTP-System

Serverless-OTP-System is a web based application for email verification through OTP.

- You can register/login using your email ID.
- It generates a 6 digit numeric OTP which will be sent for the mail used for registration/login.
- It is hosted on scalable AWS cloud services, so it can handle any number of requests.

![GitHub last commit](https://img.shields.io/github/last-commit/saicharith2012/Serverless-OTP-system-backend?style=plastic)

## Screenshots

![Sign Up Page](https://i.imgur.com/XCY7Osd.png)
![Verify Page](https://i.imgur.com/Pmv23l6.png)
![Alert Message](https://i.imgur.com/MZJaUz9.png)
![Alert Message](https://i.imgur.com/goCCKNw.png)
![Verification Email](https://i.imgur.com/GA5lrVX.png)

## Hosted URL

You can access the site [here](https://serverless-otp-system-team-16.netlify.app/).

## Features Implemented

### Frontend Features

- Users can register/login using your email ID
- Users can complete their registration by OTP verification. OTP will be mailed to them.

### Frontend Features

- Backend hosted on AWS lamba will trigger on a frontend request and create an OTP and will send the verification mail to the user.
- It hosts all the data of the users in AWS DynamoDB.

## Technologies/Libraries/Packages Used

- React.js
- Node.js
- AWS lambda
- AWS API gateway
- AWS DynamoDB
- ExpressHandleBars

## Local Setup

### Frontend

- Clone this repository to your computer
- Go to the Frontend folder and install all the dependencies using `npm install`.
- Start the application using `npm run`.

### Backend

- Make an AWS account.
- Create a new lambda function for node.js and paste the [gen-OTP.js](backend/gen-OTP.js) code into it.
- Make another lambda function and paste the [ver-OTP.js](backend/ver-OTP.js) code into it.
- Make a DynamoDB table with **Email** as partition key. Add this DynamoDB as trigger to both the lambda functions after assigning them the **DynamoDBFullAccess** role.
- Create a new AWS API gateway and integrate the methods with the respective lambda functions to get the desired endpoint URL.

## Team Members

### Team - 16

- Gandla Akshith (2020BCS-030)
- P Sai Charith (2020BCS-54)
- J J Loknath (2020BCS-041)
