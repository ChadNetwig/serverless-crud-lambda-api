# Serverless CRUD API with AWS Lambda and DynamoDB

## Overview
This project implements a complete CRUD (Create, Read, Update, Delete) API using AWS Lambda functions, DynamoDB, and API Gateway. Each operation is encapsulated in a separate Lambda function, demonstrating a modular, serverless approach to managing data in a NoSQL database.

The API is designed to store and manage questions and answers, providing endpoints for inserting, updating, retrieving, filtering, and deleting records.

---

## Key Features
- **Serverless Architecture:** All operations are implemented as AWS Lambda functions behind API Gateway endpoints.
- **CRUD Operations:** 
  - *Create & Update:* Insert or modify questions and answers.
  - *Read:* Retrieve a single record, query with filters, and scan the table.
  - *Delete:* Remove records by ID.
- **DynamoDB Integration:** Utilizes DynamoDB as a scalable NoSQL backend.
- **Modular Functions:** Each Lambda performs one clear responsibility:
  - `DeleteRecord`: Delete items by ID.
  - `FindOneQuestion`: Retrieve a question by ID.
  - `GetSingleRecord`: Fetch a single record.
  - `TableScan`: List all records.
  - `UpsertQuestion`: Insert or update questions.
  - `UpsertAnswer`: Insert or update answers.
- **Test Coverage:** Includes screenshots of successful test executions for each endpoint.

---

## Screenshots

### Test: Query With Filter
<img src="assets/QuestionWithFilter-Test%20results.png" alt="QuestionWithFilter Test Results" width="700"/>

---

### Test: Delete Answer
<img src="assets/TestDeleteAnswer-Test%20results.png" alt="Delete Answer Test Results" width="700"/>

---

### Test: Get Answer
<img src="assets/TestGetAnswer-Test%20results.png" alt="Get Answer Test Results" width="700"/>

---

### Test: Get Question
<img src="assets/TestGetQuestion-Test%20results.png" alt="Get Question Test Results" width="700"/>

---

## Technologies Used
- AWS Lambda
- AWS API Gateway
- AWS DynamoDB
- Node.js

---

## How to Build and Run

1. **Set up AWS resources:**
   - Create a DynamoDB table with a partition key (e.g., `id`).
   - Configure API Gateway endpoints for each Lambda function.

2. **Deploy Lambda functions:**
   - Upload each folder (`DeleteRecord`, `FindOneQuestion`, `GetSingleRecord`, `TableScan`, `UpsertAnswer`, `UpsertQuestion`) as a separate Lambda.
   - Ensure each function has permissions to read/write to DynamoDB.

3. **Test endpoints:**
   - Use Postman or AWS API Gateway console to invoke each operation.
   - Refer to the screenshots in `/assets` for sample request/response flows.

---

## Important Notes
- This project is intended for demonstration and portfolio purposes.
- The code may require adjustments to match your specific DynamoDB table schema, IAM roles, and API Gateway configuration.
- For production use, consider adding validation, authentication, and error handling.

---

## License
This project is shared for educational and illustrative purposes. No warranty is provided.
