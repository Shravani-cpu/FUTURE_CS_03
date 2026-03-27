# API Security Analysis Report

---

## 1. Objective
To analyze the security of a public API and identify potential vulnerabilities, including authentication issues, data exposure, and improper access control.

---

## 2. API Selected
- **API Name:** JSONPlaceholder  
- **Base URL:** https://jsonplaceholder.typicode.com  

---

## 3. Tools Used
- Postman (Mobile Application)  
- Mobile Browser (Chrome)

---

## 4. Methodology
1. Selected a public API.  
2. Reviewed API documentation.  
3. Tested endpoints using Postman.  
4. Inspected requests, responses, and headers.  
5. Identified security risks.  
6. Classified risk severity.  
7. Suggested remediation steps.

---

## 5. API Testing Details
- **Endpoint Tested:** `/posts`  
- **Method Used:** `GET`  
- **Status Code:** `200 OK`  

---

## 6. Identified Security Risks

| Risk | Description |
|------|------------|
| Missing Authentication | API does not require login or token. |
| Broken Authorization | No restrictions on accessing other users' data. |
| Excessive Data Exposure | Complete dataset is exposed without limitation. |
| Open Endpoint | API endpoints are publicly accessible. |
| Missing Rate Limiting | Unlimited requests are allowed, which can lead to abuse. |

---

## 7. Risk Severity Classification

| Risk | Severity |
|------|---------|
| Missing Authentication | High |
| Broken Authorization | High |
| Excessive Data Exposure | Medium |
| Open Endpoint | Medium |
| Missing Rate Limiting | Low |

---

## 8. Remediation Suggestions
- Implement authentication using mechanisms such as JWT or API keys.  
- Enforce proper authorization checks to ensure users can only access their own data.  
- Limit API responses to only necessary data fields.  
- Restrict access to sensitive endpoints.  
- Apply rate limiting and request throttling to prevent abuse.

---

## 9. Conclusion
The analyzed API is publicly accessible and does not implement authentication or authorization mechanisms. While this is acceptable for a demo/testing API, similar issues in production environments can result in serious security vulnerabilities such as unauthorized data access and misuse. Proper security practices should be followed to ensure safe API usage, in alignment with industry standards such as the OWASP API Security Top 10.
