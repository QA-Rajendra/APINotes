# APINotes
Api notes
1) What is API?
   
-  API means Application Programming Interface. It is a set of rules and protocols. It lets different software applications communicate.
---------------------------------------------------------------------------------------------------------------------
2. What is Web Service?
- A Web Service works over the internet.
It helps two devices communicate.
It uses standard protocols like HTTP, XML, JSON.
---------------------------------------------------------------------------------------------------------------------
3. What is Backend Architecture ?
- Backend architecture runs behind the scenes.
It connects the server, database, and application logic.
It processes requests and sends responses.
---------------------------------------------------------------------------------------------------------------------

# REST vs SOAP APIs

| Feature       | REST API                                           | SOAP API                                         |
|---------------|----------------------------------------------------|--------------------------------------------------|
| **Protocol**  | Uses HTTP methods (GET, POST, PUT, DELETE)          | Uses only XML-based messaging                    |
| **Data Format** | Supports JSON and XML                              | Supports XML only                                |
| **Speed**     | Lightweight and faster                              | Heavier and slower                               |
| **Flexibility** | More flexible, easy to use                         | Strict standards and rules                       |
| **Security**  | Uses HTTP security (SSL/TLS)                        | Built-in security (WS-Security)                  |
| **Best For**  | Web/mobile apps, public APIs                        | Enterprise-level secure transactions             |

-------------------------------------------------------------------------------------------------------------------------------

# CRUD Operations

** CRUD stands for Create, Read, Update, Delete – the four basic operations for data.  

## Example Table

| Operation | HTTP Method | English Example       | 
|-----------|-------------|-----------------------|
| Create    | POST        | Add a new user        | 
| Read      | GET         | Get user details      | 
| Update    | PUT/PATCH   | Change user email     |
| Delete    | DELETE      | Remove user account   |

-------------------------------------------------------------------------------------------------------------------------------

# HTTP Methods 

| Method  | Purpose (English)                 | Safe? | Idempotent? | Common Success Codes |
|---------|-----------------------------------|-------|-------------|----------------------|
| GET     | Retrieve data                      | Yes   | Yes         | 200, 304, 206        |
| POST    | Send new data / create resource    | No    | No          | 201, 200, 202        |
| PUT     | Update/replace entire resource     | No    | Yes         | 200, 201, 204        |
| PATCH   | Update partial data                | No    | Maybe       | 200, 204             |
| DELETE  | Remove resource                    | No    | Yes         | 204, 200, 202        |
| HEAD    | Retrieve headers only (no body)    | Yes   | Yes         | 200, 304             |
| OPTIONS | Check supported methods / CORS     | Yes   | Yes         | 200, 204             |

# 🌐 HTTP Status Codes 

| **Code** | **Emoji** | **Meaning** |
|----------|-----------|-------------|
| **2xx – Success** | ✅ | Request was successful. |
| 200 OK | 🟢 | The request succeeded. |
| 201 Created | 🆕 | A new resource was successfully created. |
| 204 No Content | 📭 | Request succeeded but no content returned. |

| **4xx – Client Error** | ⚠️ | The request has an error from the client side. |
| 400 Bad Request | ❌ | Malformed syntax or invalid data in the request. |
| 401 Unauthorized | 🔑 | Authentication is required or has failed. |
| 403 Forbidden | 🚫 | You don’t have permission to access the resource. |
| 404 Not Found | 🕵️ | The requested resource does not exist. |

| **5xx – Server Error** | 🛑 | Server failed to fulfill a valid request. |
| 500 Internal Server Error | 💥 | A generic server-side error occurred. |
| 502 Bad Gateway | 🌩️ | Server received an invalid response from an upstream server. |
| 503 Service Unavailable | 💤 | Server is overloaded or under maintenance. |


-------------------------------------------------------------------------------------------------------------------------------
### 

What is **API Testing** ?

1.  API testing checks if an API works as expected. 
2.  It tests functionality, reliability, performance, and security. 
3.  It does not use a user interface. 
It is important because it helps with:

*   Early defect detection
*   Faster feedback loop
*   Decoupled testing
*   Improved test coverage
*   Enhanced reliability


-------------------------------------------------------------------------------------------------------------------------------
### 🔍 GET – Retrieve data

### 

📌 **What it does:** Fetches data from the server **without changing it**.  
📱 **Example:** Viewing your profile details in an app.  
💻 **Sample:**

`GET /users/101`

* * *

### ✉️ POST – Send new data

### 

📌 **What it does:** Sends data to the server to **create** a new resource or trigger an action.  
📱 **Example:** Registering a new account.  
💻 **Sample:**

`POST /users Body: { "name": "Asha", "email": "asha@example.com" }`

* * *

### 🔄 PUT – Update existing data completely

### 

📌 **What it does:** **Replaces** the entire resource with new data.  
📱 **Example:** Changing all details of a user profile.  
💻 **Sample:**

`PUT /users/101 Body: { "name": "Asha Patil", "email": "asha@new.com" }`

* * *

### 🛠️ PATCH – Update partial data

### 

📌 **What it does:** Updates **only specific fields** in a resource.  
📱 **Example:** Updating just your email address without changing other details.  
💻 **Sample:**

`PATCH /users/101 Body: { "email": "asha@update.com" }`

* * *

### 🗑️ DELETE – Remove data

### 

📌 **What it does:** Deletes the resource from the server.  
📱 **Example:** Removing a user account.  
💻 **Sample:**

`DELETE /users/101`


* * *

### 📄 HEAD – Retrieve metadata only

### 

📌 **What it does:** Similar to GET, but **returns only headers** (no content).  
📱 **Example:** Checking the last modified date of a file.  
💻 **Sample:**

`HEAD /files/report.pdf`

* * *

### ⚙️ OPTIONS – Check supported methods

### 

📌 **What it does:** Shows which HTTP methods are **allowed** for a specific resource.  
📱 **Example:** Checking if you can POST or DELETE to a certain URL.  
💻 **Sample:**

`OPTIONS /users Response: Allow: GET, POST, PUT, DELETE`
-------------------------------------------------------------------------------------------------------------------------------
## 🔐 What is Authentication?

### *   Authentication checks identity.
*   It is for a user or system.
*   It verifies using credentials.   
*   Examples: username, password, biometric data.

* * *
## 

**🍪 What is a Cookie?**
*   A cookie is small data   
*   It is stored in the browser.  
*   A website saves it.  
*   It remembers login status, preferences, or cart items.  
    **Example**    
    *    You log into an e-commerce site.   
    *   It remembers your cart after closing the browser.   
    *   This happens because of cookies.
 
  * * *

  # How to test API Testing –

| Step | Description                                  |
|------|------------------------------------------------------|
| 1    | Understand the API – Read documentation, endpoints, methods, parameters.|
| 2    | Choose a testing tool – Postman, SoapUI, cURL, RestAssured, etc. |
| 3    | Set up the request – Method, URL, headers, body.     | 
| 4    | Send request & check response – Status, headers, body. |
| 5    | Validate results – Status codes, data, headers, errors. | 
| 6    | Test functional, performance, security aspects.     | 
| 7    | Automate tests if needed – Scripts, collections.    |

-------------------------------------------------------------------------------------------------------------------------------

# API Request Components – Summary

| Component         | English Description                                                                                 | Marathi Description                                                                 |
|-------------------|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| Endpoint (URL/URI) | The address where the API is available, pointing to a specific resource.                           | API उपलब्ध असलेला पत्ता, जो विशिष्ट संसाधनाकडे निर्देशित करतो.                      |
| HTTP Method (Verb) | Action to perform on the resource (GET, POST, PUT, PATCH, DELETE, etc.).                            | संसाधनावर करावयाची कृती (GET, POST, PUT, PATCH, DELETE इ.).                        |
| Headers           | Key–value pairs carrying metadata like `Content-Type`, `Accept`, `Authorization`, `User-Agent`.    | `Content-Type`, `Accept`, `Authorization`, `User-Agent` यांसारखी मेटाडेटा असणारी जोड. |
| Body (Payload)    | Actual data sent to the server, usually in JSON/XML; used in POST, PUT, PATCH.                       | सर्व्हरला पाठवलेला वास्तविक डेटा, सहसा JSON/XML मध्ये; POST, PUT, PATCH मध्ये वापरला जातो. |
| Query Parameters  | Optional key–value pairs after `?` for filtering, sorting, or pagination.                            | `?` नंतरचे पर्यायी की–व्हॅल्यू जोड, फिल्टरिंग, सॉर्टिंग किंवा पेजिनेशनसाठी.          |
| Path Parameters   | Values in the URL path identifying a specific resource.                                              | विशिष्ट संसाधन ओळखण्यासाठी URL पाथमधील मूल्ये.                                     |

* * *

# 🧪 API Testing Types – English & Marathi

| **Type** | **Emoji** | **English (Short)** | **Marathi (Short)** |
|----------|-----------|---------------------|---------------------|
| **Functional Testing** | ✅ | Checks if API works as expected. Tests positive, negative, edge cases. | API अपेक्षित कार्य करते का ते तपासते. सकारात्मक, नकारात्मक, सीमेवरील चाचण्या. |
| **Performance Testing** | 🚀 | Measures speed, stability, scalability under different loads. | गती, स्थिरता, क्षमता विविध लोडमध्ये मोजते. |
| **Security Testing** | 🔒 | Finds security issues: auth bypass, SQL injection, XSS, encryption flaws. | सुरक्षा त्रुटी शोधते: प्रमाणीकरण बायपास, SQL इंजेक्शन, XSS, एन्क्रिप्शन समस्या. |
| **Reliability Testing** | ♻️ | Ensures API connects and works correctly every time. | API सतत जोडते आणि योग्य कार्य करते याची खात्री करते. |
| **Load Testing** | 📊 | Tests under normal user load. | सामान्य वापर लोडखाली तपासते. |
| **Stress Testing** | 💥 | Pushes API beyond normal limits. Finds breaking points. | API ला मर्यादेपलीकडे ढकलते. ब्रेकिंग पॉइंट शोधते. | 
| **Fuzz Testing** | 🎲 | Sends random or wrong data to find crashes or bugs. | यादृच्छिक किंवा चुकीचा डेटा पाठवते. क्रॅश किंवा त्रुटी शोधते. | 
| **Validation Testing** | ✔️ | Checks if response is correct and in right format. | प्रतिसाद योग्य आणि अपेक्षित स्वरूपात आहे का ते तपासते. |
| **UI Testing** (API context) | 🖥️ | Ensures UI talks to API and shows data correctly. | UI API शी योग्य संवाद साधते आणि डेटा योग्य दाखवते. |
| **Interoperability Testing** | 🔗 | Ensures API works with other APIs or systems. | API इतर API किंवा सिस्टीमसोबत योग्य कार्य करते. |
| **Contract Testing** | 📜 | Verifies API follows rules agreed between provider and consumer. | पुरवठादार-ग्राहक यांच्यातील ठरलेले नियम पाळते का ते तपासते. |
* * * *
# 🧪 API Testing – While doing API testing, a number of things need to be validated to confirm the quality of the API.

| **Category** | **Aspect** | **Description** |
|--------------|------------|-----------------|
| **🛠️ Functionality** | **Data Accuracy** | Ensure the API returns correct and expected data. |
| | **Business Logic** | Validate business rules, workflows, and calculations are enforced. |
| | **Input Validation** | Check handling of valid, invalid, missing, and edge-case inputs. |
| | **Response Structure** | Verify correct format, fields, and structure in the response. |
| | **Error Handling** | Confirm proper error codes/messages for failures. |
| | **Reliability** | API should work consistently under different conditions. |
| **⚡ Performance** | **Response Time** | Measure how fast the API responds. |
| | **Throughput** | Number of requests handled in a time period. |
| | **Scalability** | API performance when load increases. |
| **🔒 Security** | **Authentication & Authorization** | Validate that only authorized users can access data. |
| | **Vulnerability Testing** | Check for SQL Injection, XSS, CSRF, etc. |
| **📚 Usability** | **Documentation** | Ensure API docs are clear, accurate, and helpful. |
| **📏 Compliance** | **Standards/Regulations** | Validate adherence to industry or legal standards. |

****
# 🧰 Common Tools for API Testing

| **Category** | **Tool** | **Emoji** | **Strengths** |
|--------------|----------|-----------|---------------|
| **🖱️ Manual + Automation** | **Postman** | 📬 | User-friendly GUI, send requests, inspect responses, organize tests into collections, write test scripts. |
| | **SoapUI** | 🧼 | Open-source, supports SOAP & REST, good for functional, performance, and security testing. |
| **⚙️ Automation (Code-based)** | **REST Assured** | ☕ | Java library for REST API testing, readable syntax, integrates well with automation frameworks. |
| **📊 Performance + Functional** | **JMeter** | 📈 | Originally for performance testing, can send HTTP/HTTPS requests, supports functional API checks. |
| **📄 Documentation + Testing** | **Swagger / OpenAPI** | 📜 | Auto-generates interactive API docs, allows sending requests directly from docs (Swagger UI). |
| **💻 Command-line** | **curl** | 💡 | Lightweight CLI tool, quick API calls, great for scripting & automation in shell environments. |

* * * 
# 🔒 Handling Authentication & Authorization in API Testing

## 🧠 Understanding Authentication Mechanisms
- **🔑 API Keys** – Passed in headers or query parameters. Include directly in request.
- **📜 Basic Auth** – Username + password Base64 encoded in `Authorization` header.
- **🔄 OAuth (1.0/2.0)** – Obtain access tokens via separate flow; automate token generation and send Bearer token in `Authorization` header.
- **🪪 JWT (JSON Web Tokens)** – Obtain token, send in header, parse & validate structure and expiry.

---

## 🧪 Test Scenarios

### ✅ Positive Testing
- Access with valid credentials.
- Verify role-based access (e.g., Admin vs. User).

### ❌ Negative Testing
- Send requests **without authentication**.
- Use **invalid or expired tokens**.
- Try accessing resources **without proper permissions**.

### ⏳ Token Expiration & Refresh
- Test API behavior when tokens expire.
- Verify refresh token flow works correctly.

---

## 🛠 Tools Support
- **📬 Postman** – Built-in support for API keys, Basic Auth, OAuth, JWT.
- **☕ REST Assured** – Automates token handling in Java-based test frameworks.

-------------------------------------------------------------------------------------------------------------------------------------------

## 14️⃣ What is API Contract Testing? 📜

**Definition**: Verifies that API consumer (client) and provider (server) follow a predefined **contract** — specifying request format, response format, data types, and status codes.  
**Why Important?**  
- 🤝 Avoids integration issues in **microservices**.
- 🔍 Ensures both sides agree on **input/output rules** before deployment.
- 🛠 Detects breaking changes early.

**Benefits**:
- ⚡ Faster feedback in dev cycle.
- 📦 Reduced production bugs.
- 🔗 Maintains compatibility across services.

---

## 15️⃣ Handling Dynamic Values in API Testing 🔄

**Examples**: timestamps, session IDs, tokens, unique IDs.  

**Techniques**:
1. **Variable Extraction / Chaining**:
   - 📦 Postman: `pm.environment.set()` / `pm.collectionVariables.set()`
   - 📜 Rest Assured: `JsonPath` / `XPath` parsing.
2. **Parameterization**:
   - 💾 Use CSV, Excel, or JSON to inject values into requests.
3. **Generate Data at Runtime**:
   - ⏱ Timestamps: `Date.now()` (JS) / `System.currentTimeMillis()` (Java).
   - 🎲 Random strings/numbers via libraries.
4. **Regex Extraction**:
   - 🔍 For complex embedded patterns.

---

## 16️⃣ Challenges in API Testing 🚧

- 🔐 Complex **authentication & authorization** flows.
- 📄 Handling **multiple data formats** (JSON, XML, CSV).
- 🔄 Supporting **multiple API versions**.
- 📈 Performance & scalability under load.
- 🔗 Testing **dependent services** in microservice ecosystems.
- 🧪 Maintaining test environments with fresh data.

---

## 17️⃣ Deciding What API Test Cases to Write 📝

**Systematic Approach**:
1. 📖 **Review Documentation** (Swagger/OpenAPI).
2. ✅ **Positive Scenarios** – Valid data, successful operations.
3. ❌ **Negative Scenarios** – Invalid inputs, unauthorized access.
4. 📏 **Boundary & Edge Cases** – Min/max values, nulls, special chars.
5. 🔐 **Auth Tests** – Role-based access, token validity.
6. 🧮 **Data Validation** – Schema checks, field presence.
7. 📬 **Response Verification** – Status codes, body, headers.
8. ⚡ **Performance** – High-traffic endpoints.
9. 🛡 **Security** – SQL injection, XSS, data leaks.
10. 🔗 **Chained Workflows** – Passing data between calls.
11. 🧹 **Data Clean-up** – Maintain test environment.

---

## 18️⃣ Integrating API Tests into CI/CD 🔄

**Why?** Continuous feedback & quality assurance.

**Steps**:
1. 🤖 **Automate** tests (Rest Assured, Postman + Newman, etc.).
2. 📂 Store scripts in **Version Control** (Git).
3. 🔔 Configure **CI Tool** (Jenkins, GitLab CI, Azure DevOps).
4. 🏃 Run tests on **every commit/merge** + scheduled runs.
5. ⚙ Setup **environments** & credentials.
6. 📊 **Reports** – TestNG/JUnit, Allure, Newman HTML.
7. 📢 **Notifications** – Email/Slack alerts on failure.
8. 🚧 **Quality Gates** – Block deployments if critical tests fail.

---

## 19️⃣ Data-Driven API Testing 📊

**Definition**: Running same API test case with multiple input datasets.  

**Data Sources**:
- 📄 CSV
- 📊 Excel
- 🗄 Databases
- 📦 JSON/XML

**Approach**:
- 🧩 **Parameterize** URLs, headers, and payloads.
- 🔄 Iterate through datasets using:
  - Postman Collection Runner
  - Rest Assured + TestNG DataProviders
  - Python loops with `requests`
- ✅ Validate output for each dataset.

---

## 20️⃣ Testing API Error Handling ⚠

**Why Important?** APIs must **fail gracefully** and return clear error messages.  

**Steps**:
1. Categorize **error types**:
   - 🚫 Client Errors (4xx)
   - 💥 Server Errors (5xx)
2. Create **test cases**:
   - Invalid/missing parameters
   - Unauthorized access
   - Non-existent resources
   - Malformed payloads
3. Verify:
   - 📜 **Error codes** are correct.
   - 📝 **Error messages** are meaningful.
   - 📄 Response follows JSON/XML format.

* * *

## 21️⃣ What is JSON and How Do You Test It in API? 📦

**JSON** (JavaScript Object Notation) → Lightweight, human-readable, and machine-parsable format for data exchange.  
**Testing JSON** involves:
- ✅ **Schema Validation** – Match response to predefined JSON schema.
- 🔍 **Data Validation** – Check correctness, completeness, and data types.
- 📋 **Mandatory Fields** – Verify required fields exist; ensure unwanted fields are absent.
- ⚠ **Error Responses** – Must also follow JSON format with proper codes/messages.
- ⏱ **Performance** – Test parsing & processing time, especially for large payloads.

---

## 22️⃣ How Do You Test Response Time in API Testing? ⏳

**Why Important?** Ensures API delivers results quickly for smooth UX & integration.

**Process**:
1. 📊 **Set Benchmarks** with stakeholders.
2. 🎯 **Target Key APIs** – high traffic, large data, or business-critical.
3. 🛠 **Choose Tools** – Postman, JMeter, REST Assured, etc.
4. 🧪 **Design Test Cases** – Load, stress, and spike scenarios.
5. 📈 **Analyze Results** – Compare to benchmarks.
6. 🔍 **Investigate Bottlenecks** – API code, DB queries, network latency.

---

## 23️⃣ What is the Role of Headers in API Testing? 🏷

**Headers** → Key-value pairs with **metadata** about request/response.

**Purpose**:
- 🔐 Authentication & Authorization
- 📄 Content Negotiation (e.g., JSON vs XML)
- 🗄 Caching Control
- 📝 Request Info (e.g., User-Agent)
- 🕵 Debugging & Tracing

---

## 24️⃣ How Do You Perform Load Testing on APIs? 📈

**Definition**: Tests API behavior under expected or peak load.

**Steps**:
1. 🎯 Identify **critical endpoints**.
2. 📊 Estimate **concurrent users / RPS**.
3. 🛠 Select tools (JMeter, k6, Locust, Gatling).
4. ✍ Create **realistic test scripts** (methods, headers, bodies).
5. ⚙ Configure **load parameters** – users, ramp-up, duration.
6. ▶ Run tests (possibly distributed).
7. 📉 Monitor performance & errors.

**Metrics**: Response time, throughput, error rate, resource utilization.

---

## 25️⃣ How Do You Prioritize API Test Cases for Regression? 📌

**Why?** Limited time/resources require focusing on most impactful tests.

**Prioritization Criteria**:
- 🏢 **Business Criticality**
- 💰 High-value features
- 📈 High usage / traffic endpoints
- 🛠 Recently changed APIs
- 🐞 Defect-prone areas (history)
- 🔗 Dependency-heavy APIs
- 🧮 Complex business logic

