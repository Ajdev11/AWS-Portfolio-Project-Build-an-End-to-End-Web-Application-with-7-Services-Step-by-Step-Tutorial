# Full-Stack Ride Sharing Web Application on AWS

## Services to Be Used
- **GitHub** – Code repository and version control  
- **AWS IAM (Identity and Access Management)** – Manage permissions and security  
- **AWS Amplify** – Hosting the frontend and continuous deployment  
- **Amazon Cognito** – User authentication (sign-up, login, and session management)  
- **AWS Lambda** – Serverless backend logic (ride-sharing functionality)  
- **Amazon API Gateway** – Expose Lambda functions as APIs  
- **Amazon DynamoDB** – NoSQL database for storing ride details and results  

---

## Requirements and Mapping to Services

### 1. Store, Update, and Pull Code  
✅ **GitHub**  
- Use GitHub to maintain version control of the application code.  
- Push changes to trigger deployment pipelines in **Amplify**.  

---

### 2. Host Website and Manage Updates  
✅ **AWS Amplify**  
- Deploy the frontend (React/Angular/Vue, etc.).  
- Enable automatic updates from GitHub commits.  

---

### 3. User Registration and Login  
✅ **Amazon Cognito**  
- Provide secure sign-up, login, and user session handling.  
- Enable multi-factor authentication (MFA) if needed.  

---

### 4. Ride Sharing Functionality  
✅ **AWS Lambda**  
- Write serverless functions to handle core ride-sharing logic (e.g., match drivers with riders).  

---

### 5. Store and Retrieve Ride Results  
✅ **Amazon DynamoDB**  
- Store ride requests, available drivers, and ride history.  
- Query and return data for the frontend.  

---

### 6. Invoke Ride-Sharing Functionality  
✅ **Amazon API Gateway**  
- Create RESTful endpoints to invoke Lambda functions.  
- Secure endpoints with **Cognito authentication**.  

---

## Architecture Flow (High-Level)

1. **Frontend (Amplify)** calls API Gateway endpoints.  
2. **API Gateway** routes requests to **Lambda functions**.  
3. **Lambda** executes ride-sharing logic.  
4. **DynamoDB** stores and retrieves ride data.  
5. **Cognito** handles user authentication/authorization.  
6. **GitHub + Amplify** ensure continuous deployment of frontend updates.  

---
