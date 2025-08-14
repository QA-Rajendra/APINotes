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

# HTTP Methods – Summary Report

| Method  | Purpose (English)                 | Safe? | Idempotent? | Common Success Codes |
|---------|-----------------------------------|-------|-------------|----------------------|
| GET     | Retrieve data                      | Yes   | Yes         | 200, 304, 206        |
| POST    | Send new data / create resource    | No    | No          | 201, 200, 202        |
| PUT     | Update/replace entire resource     | No    | Yes         | 200, 201, 204        |
| PATCH   | Update partial data                | No    | Maybe       | 200, 204             |
| DELETE  | Remove resource                    | No    | Yes         | 204, 200, 202        |
| HEAD    | Retrieve headers only (no body)    | Yes   | Yes         | 200, 304             |
| OPTIONS | Check supported methods / CORS     | Yes   | Yes         | 200, 204             |

-------------------------------------------------------------------------------------------------------------------------------
### 

What is **API Testing** ?

1.  API testing checks if an API works as expected.
    
2.  It tests functionality, reliability, performance, and security.  
    
3.  It does not use a user interface.


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
