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

