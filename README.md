# To The Power of Math — Serverless Web Application

A serverless web application built on AWS that calculates the power of a number using a fully serverless backend. Users enter a base number and an exponent, and the application calculates the result using AWS Lambda, stores the calculation and timestamp in Amazon DynamoDB, and displays the result in the browser.

The project demonstrates my practical experience with **AWS serverless architecture, API integration, Python, NoSQL databases, and CI/CD deployment**.

🔗 **Live Demo:** [To The Power of Math](https://main.dq00xqarr8zue.amplifyapp.com/)

---

## Architecture

The application uses AWS services to handle frontend hosting, API requests, computation, and data storage without managing servers.

```text
                 ┌──────────────────┐
                 │   Web Browser    │
                 └────────┬─────────┘
                          │
                          ▼
                 ┌──────────────────┐
                 │   AWS Amplify    │
                 │ Frontend Hosting │
                 └────────┬─────────┘
                          │
                     POST / JSON
                          │
                          ▼
                 ┌──────────────────┐
                 │ Amazon API       │
                 │ Gateway          │
                 └────────┬─────────┘
                          │
                          ▼
                 ┌──────────────────┐
                 │  AWS Lambda      │
                 │  Python          │
                 │                  │
                 │ Calculates power │
                 └────────┬─────────┘
                          │
                          ▼
                 ┌──────────────────┐
                 │ Amazon DynamoDB  │
                 │ Calculation Log  │
                 └──────────────────┘
```

### How It Works

1. The user enters a base number and an exponent in the web application.
2. The frontend sends a POST request containing the input values to Amazon API Gateway.
3. API Gateway invokes an AWS Lambda function.
4. Lambda calculates the result using Python's mathematical operations.
5. The calculation and its timestamp are stored in Amazon DynamoDB.
6. The result is returned to the browser and displayed to the user.

---

## AWS Services Used

| Service | Purpose |
|---|---|
| **AWS Amplify** | Hosts the frontend and supports continuous deployment. |
| **Amazon API Gateway** | Exposes the REST API endpoint for calculation requests. |
| **AWS Lambda** | Runs the Python calculation logic without managing servers. |
| **Amazon DynamoDB** | Stores calculation records and timestamps. |
| **GitHub** | Stores the source code and supports the development workflow. |

---

## Key Features

- **Serverless computation:** Calculates powers without provisioning or managing servers.
- **REST API integration:** Connects the frontend to the backend using HTTP requests.
- **Persistent data storage:** Saves calculation records and timestamps in DynamoDB.
- **Cloud deployment:** Makes the application accessible through a public URL.
- **CI/CD workflow:** Supports deploying frontend changes through GitHub and AWS Amplify.

---

## Technologies

- Python
- AWS Lambda
- Amazon API Gateway
- Amazon DynamoDB
- AWS Amplify
- Git and GitHub
- REST APIs and JSON

---

## What I Learned

Building this project helped me understand how to:

- Design and deploy a serverless application on AWS.
- Connect a web frontend to a cloud-based backend.
- Build an API-driven workflow using Amazon API Gateway and AWS Lambda.
- Persist application data using Amazon DynamoDB.
- Deploy and update a frontend using a GitHub-based CI/CD workflow.
- Understand how managed cloud services work together to deliver an application.

---

## Live Application

Try the application here:

**[Launch To The Power of Math](https://main.dq00xqarr8zue.amplifyapp.com/)**

---

## Future Improvements

- Add input validation and clearer error messages.
- Display calculation history retrieved from DynamoDB.
- Add automated tests for the Python Lambda function.
- Improve monitoring and logging for failed requests.
- Add infrastructure as code to automate AWS resource provisioning.



