# Postman — Complete Guide (English → Marathi)

---

## 1. Introduction / ओळख
- **English:** Postman is a popular API client used to design, develop, test, and document APIs with a friendly GUI and automation features.  
- **Marathi:** Postman हा एक प्रसिद्ध API क्लायंट आहे जो API डिझाइन, डेव्हलप, टेस्ट आणि डॉक्युमेंट करण्यासाठी GUI आणि ऑटोमेशन सुविधा देतो.

---

## 2. What is Postman? / Postman म्हणजे काय?
- **English:** Postman lets you send HTTP requests, inspect responses, write automated tests (JavaScript with the `pm` API and Chai-style assertions), save requests in collections, and run suites with the Collection Runner or Newman (CLI).  
- **Marathi:** Postman तुम्हाला HTTP विनंत्या पाठवण्याची, रिस्पॉन्स तपासण्याची, ऑटोमेटेड टेस्ट लिहिण्याची (`pm` API आणि Chai-स्टाइल assertion वापरून), विनंत्या संग्रहात (collections) जतन करण्याची आणि Collection Runner किंवा Newman (CLI) ने सुइट चालवण्याची परवानगी देतो.

---

## 3. Basic API Operations in Postman / Postman मध्ये मूलभूत API ऑपरेशन्स

### How to Call a REST API / REST API कशी कॉल करावी
- **English:**  
  1. Select HTTP method (GET, POST, PUT, DELETE, etc.).  
  2. Enter API endpoint URL.  
  3. Add path/query parameters, headers, and body as needed.  
  4. Click **Send** and inspect the status, headers, and body in the response.  
- **Marathi:**  
  1. HTTP पद्धत निवडा (GET, POST, PUT, DELETE इ.).  
  2. API एंडपॉइंट URL टाका.  
  3. गरजेनुसार path/query parameters, headers आणि body जोडा.  
  4. **Send** क्लिक करा आणि रिस्पॉन्समधील स्टेटस, हेडर्स व बॉडी तपासा.

### Path Parameter / पाथ पॅरामिटर
- **English:** Insert variables directly in the endpoint URL. Example:  
https://api.example.com/users/{userId}

markdown
Copy
Edit
- **Marathi:** एंडपॉइंट URL मध्ये थेट व्हेरिएबल्स जोडा. उदाहरण:  
https://api.example.com/users/{userId}

markdown
Copy
Edit

### Query Parameter / क्वेरी पॅरामिटर
- **English:** Add key-value pairs in the Params tab. Example:  
?status=active&page=2

markdown
Copy
Edit
- **Marathi:** Params टॅबमध्ये key-value जोड्या टाका. उदाहरण:  
?status=active&page=2

markdown
Copy
Edit

### Set Headers / हेडर्स सेट करा
- **English:** Go to Headers tab → Add key/value. Example:  
Content-Type: application/json

markdown
Copy
Edit
- **Marathi:** Headers टॅब → key/value जोडा. उदाहरण:  
Content-Type: application/json

markdown
Copy
Edit

### Pass JSON/XML Payload / JSON/XML पेलोड पाठवा
- **English:** Body tab → raw → Select JSON/XML → Paste data.  
- **Marathi:** Body टॅब → raw → JSON/XML निवडा → डेटा पेस्ट करा.

### Check Response Status Code / रिस्पॉन्स स्टेटस कोड तपासा
- **English:** Shown in the response section (e.g., `200 OK`, `404 Not Found`).  
- **Marathi:** रिस्पॉन्स सेक्शनमध्ये दिसते (उदा. `200 OK`, `404 Not Found`).

### Check JSON/XML Response Messages / रिस्पॉन्स मेसेज तपासा
- **English:** View in Body tab after request execution.  
- **Marathi:** रिक्वेस्ट पूर्ण झाल्यावर Body टॅबमध्ये पाहा.

### Response Headers / रिस्पॉन्स हेडर्स
- **English:** Shows metadata like `Content-Type`, `Server`, etc.  
- **Marathi:** `Content-Type`, `Server` इत्यादी मेटाडेटा दाखवते.

### Cookies Manipulation / कुकीज मॅनिप्युलेशन
- **English:** Manage cookies in Cookies tab.  
- **Marathi:** Cookies टॅबमध्ये कुकीज व्यवस्थापित करा.

### Header Presets / हेडर प्रीसेट्स
- **English:** Save frequently used headers for quick reuse.  
- **Marathi:** वारंवार वापरले जाणारे हेडर्स सेव्ह करा, जेणेकरून पुन्हा पटकन वापरता येतील.

### API History / API इतिहास
- **English:** Access past requests from the History tab.  
- **Marathi:** History टॅबमधून मागील विनंत्या पाहा.

---

# 4\. Postman Advanced Features / Postman च्या प्रगत वैशिष्ट्ये

## Environment Variables / एन्व्हायर्नमेंट व्हेरिएबल्स

*   **English:** Environments (Local, Global, Collection, Data) let you switch base URLs, credentials, tokens, and other dynamic values without editing each request. Use `{{variableName}}` syntax.
    
*   **Marathi:** Environments (Local, Global, Collection, Data) वापरून base URL, credentials, tokens इत्यादी बदलता येतात, आणि प्रत्येक विनंती संपादित न करता पर्यावरण बदलले तरी काम चालू राहते. `{{variableName}}` हा सिंटॅक्स वापरा.
    

## Pre-request Scripts / प्री-रिक्वेस्ट स्क्रिप्ट

*   **English:** JavaScript that runs before a request — used to set auth headers, generate timestamps, sign requests, or set variables. Example: generate JWT or add timestamp.
    
*   **Marathi:** विनंतीपूर्वी चालणारे JavaScript — auth headers सेट करण्यासाठी, timestamp निर्माण करण्यासाठी, request साइन करण्यासाठी किंवा व्हेरिएबल सेट करण्यासाठी वापरतात.
    

**Pre-request example:**

`// set current timestamp pm.environment.set("now", new Date().toISOString());`

## Test Scripts (JavaScript + Chai) / टेस्ट स्क्रिप्ट (JavaScript + Chai)

*   **English:** Write assertions in the Tests tab to validate status, schema, headers, body fields, or response time. Use `pm.expect(...)` or `pm.response.to.have.jsonBody(...)`.
    
*   **Marathi:** Tests टॅबमध्ये assertion लिहून status, schema, headers, बॉडी फील्ड किंवा response time तपासा. `pm.expect(...)` किंवा `pm.response.to.have.jsonBody(...)` वापरा.
    

**Test examples:**

`// status code is 200 pm.test("Status is 200", function () {   pm.response.to.have.status(200); });  // JSON field check pm.test("User email is present", function () {   var json = pm.response.json();   pm.expect(json.email).to.exist; });  // set token for later requests pm.environment.set("authToken", pm.response.json().token);`

## Automated Test Runs & Reports / ऑटोमेटेड टेस्ट रन आणि रिपोर्ट्स

*   **English:** Use Collection Runner for data-driven runs (CSV/JSON). Export and review run results; combine with Newman to generate HTML or JUnit reports.
    
*   **Marathi:** Collection Runner वापरून CSV/JSON डेटा-आधारित रन करा. रन रिजल्ट्स एक्सपोर्ट करा; Newman सह HTML किंवा JUnit रिपोर्ट जनरेट करा.
    

* * *

# 5\. Advanced Postman / Newman (CLI) / प्रगत — Newman (CLI)

## Newman Introduction / Newman काय आहे

*   **English:** Newman is Postman’s CLI runner that executes Postman collections from the command line, integrates in CI, and produces machine-readable reports.
    
*   **Marathi:** Newman हा Postman चा CLI रनर आहे जो कमांड-लाइनवरून collections चालवतो, CI मध्ये इंटिग्रेट करतो आणि रिपोर्ट जनरेट करतो.
    

## Installation & Setup / इन्स्टॉलेशन व सेटअप

*   **English:** Install via NPM:
    

`npm install -g newman`

*   **Marathi:** NPM ने इन्स्टॉल करा:
    

`npm install -g newman`

## Run Collections from Newman / Newman ने कलेक्शन कसे चालवायचे

*   **English:** Basic command:
    

`newman run collection.json`

*   **Marathi:** बेसिक कमांड:
    

`newman run collection.json`

## Common Command-Line Options / सामान्य CLI पर्याय

*   **English:** `--environment <env.json>`, `--iteration-data <data.csv>`, `--reporters cli,html,junit`, `--reporter-html-export report.html`.
    
*   **Marathi:** `--environment <env.json>`, `--iteration-data <data.csv>`, `--reporters cli,html,junit`, `--reporter-html-export report.html`.
    

**Full example:**

`newman run collection.json \   --environment env.json \   --iteration-data users.csv \   --reporters cli,html \   --reporter-html-export newman-report.html`

* * *

# 6\. Postman Collections & Documentation / Collections आणि डॉक्युमेंटेशन

## Create Collection & Folders / कलेक्शन आणि फोल्डर तयार करा

*   **English:** Group related requests into a collection; use folders to organize endpoints by feature or resource. Collections can store pre-request and test scripts at folder or collection level.
    
*   **Marathi:** संबंधित विनंत्या collection मध्ये गटबद्ध करा; फोल्डर्सने endpoint फीचर/रिसोर्सनुसार आयोजित करा. प्री-रिक्वेस्ट व टेस्ट स्क्रिप्ट folder किंवा collection स्तरावर ठेवता येतात.
    

## Create Collection from API Schema / API स्कीमामधून कलेक्शन तयार करा

*   **English:** Import OpenAPI/Swagger or RAML to auto-generate requests and example payloads.
    
*   **Marathi:** OpenAPI/Swagger किंवा RAML इम्पोर्ट करून विनंत्या आणि उदाहरण पेलोड ऑटो-जनरेट करा.
    

## Maintain API Collections / कलेक्शन कसे राखायचे

*   **English:** Keep collections versioned, use environments, document examples and expected responses, and add descriptions for each request.
    
*   **Marathi:** कलेक्शनला व्हर्जनिंग द्या, environments वापरा, उदाहरणे आणि अपेक्षित रिस्पॉन्स डोक्युमेंट करा, प्रत्येक विनंतीसाठी description जोडा.
    

## Postman Console & Logs / Postman कन्सोल आणि लॉग्स

*   **English:** Open Postman Console (View → Show Postman Console) to inspect raw requests, network traffic, and `console.log()` outputs from scripts. Great for debugging auth or pre-request logic.
    
*   **Marathi:** Postman Console (View → Show Postman Console) उघडा ज्यात raw requests, नेटवर्क ट्रॅफिक आणि script मधील `console.log()` आउटपुट दिसतात. auth किंवा प्री-रिक्वेस्ट लॉजिक डिबग करण्यासाठी उपयुक्त.
    

## Test Code Snippets / टेस्ट कोड स्नेपेट्स

*   **English:** Postman shows common code snippets (cURL, JavaScript `fetch`, Python `requests`) for any request so you can copy examples into your app.
    
*   **Marathi:** Postman प्रत्येक विनंतीसाठी सामान्य कोड स्नेपेट्स (cURL, JavaScript `fetch`, Python `requests`) दाखवतो जे आपल्या ऍपमध्ये कॉपी करता येतात.
    

## API Monitoring / API मॉनिटरिंग

*   **English:** Postman monitors run scheduled collections from the cloud to check uptime, SLA, and response correctness over time.
    
*   **Marathi:** Postman मॉनिटर्स शेड्युलनुसार कलेक्शन्स चालवून uptime, SLA आणि रिस्पॉन्स बरोबर आहे का ते तपासतात.
    

## API Documentation & Publish / API डॉक्युमेंटेशन आणि प्रकाशन

*   **English:** Generate and publish API docs from collections; docs include endpoints, parameters, examples, and code samples. You can publish public or team docs.
    
*   **Marathi:** Collection वरून API docs जनरेट आणि प्रकाशित करा; docs मध्ये endpoints, parameters, उदाहरणे आणि कोड सॅम्पल्स असतात. सार्वजनिक किंवा टीम docs प्रकाशित करता येतात.
    

* * *

# 7\. Team Collaboration / टीम सहयोग

*   **English:** Postman offers Team & Enterprise features: shared Workspaces, role-based access, forking collections, commenting, mock servers, and version control via forking/merging. Workspaces help multiple engineers work on the same APIs.
    
*   **Marathi:** Postman मध्ये Team आणि Enterprise फीचर्स आहेत: shared Workspaces, role-based access, collection forking, commenting, mock servers, आणि forking/merging द्वारे version control. Workspaces अनेक इंजिनियर्सना एकाच API वर काम करण्यास मदत करतात.
    

* * *

# 8\. Mock Server Creation / Mock सर्व्हर तयार करणे

*   **English:** Create a mock server from collection examples to simulate API responses before backend is ready. Useful for frontend development and contract testing.
    
*   **Marathi:** Collection उदाहरणांवरून mock server तयार करा जेणेकरून backend तयार होण्यापूर्वी API responses सिम्युलेट करता येतील. frontend development आणि contract testing साठी उपयुक्त.
    

* * *

# 9\. Integration & Automation / इंटिग्रेशन आणि ऑटोमेशन

## Collection Runner & Summary Reports / Collection Runner आणि सारांश रिपोर्ट्स

*   **English:** Run collections locally with data files (CSV/JSON). The runner shows pass/fail counts, response times, and logs. Export run results for CI.
    
*   **Marathi:** CSV/JSON डेटा फाइल वापरून collection स्थानिकरित्या रन करा. Runner पास/फेल गणना, रिस्पॉन्स वेळ आणि लॉग दाखवतो. CI साठी रन निकाल एक्सपोर्ट करा.
    

## Run with Docker / Docker सह रन करणे

*   **English:** Use a Docker image with Newman to run tests inside containers for isolated CI jobs.
    
*   **Marathi:** Newman सह Docker इमेज वापरून कंटेनरमध्ये टेस्ट रन करा जे CI जॉबसाठी आयसोलेटेड असते.
    

## Run with Jenkins / Jenkins सह रन करणे

*   **English:** Integrate Newman into Jenkins pipeline (shell step) to run collections on each commit or nightly. Example pipeline snippet below.
    
*   **Marathi:** Newman Jenkins pipeline मध्ये (shell स्टेप) इंटिग्रेट करा जेणेकरून प्रत्येक कमिट किंवा नाईटली रन करता येईल. खाली pipeline snippet आहे.
    

**Jenkins shell step example:**

`# install newman (if needed) and run npm install -g newman newman run /path/to/collection.json \   --environment /path/to/env.json \   --reporters cli,junit,html \   --reporter-junit-export /path/to/junit.xml \   --reporter-html-export /path/to/report.html`

* * *

# 10\. Postman Console & Debugging Tips / कन्सोल आणि डिबग टिप्स

*   **English:** Use `console.log()` in pre-request/tests, view raw request/response in Postman Console, check authorization headers, and compare with browser DevTools network tab for CORS issues.
    
*   **Marathi:** प्री-रिक्वेस्ट/टेस्टमध्ये `console.log()` वापरा, Postman Console मध्ये raw request/response पहा, authorization headers तपासा, आणि CORS समस्या तपासण्यासाठी ब्राउझर DevTools नेटवर्क टॅबशी तुलना करा.
    

* * *

# 11\. Postman Best Practices / सर्वोत्तम पद्धती

*   **English:**
    
    *   Use environment variables for all dynamic values.
        
    *   Keep secrets out of shared collections (use secure variables / Postman Secret manager).
        
    *   Write small, focused tests per request.
        
    *   Use data files for data-driven tests.
        
    *   Version control collections (use forking) and document requests.
        
*   **Marathi:**
    
    *   सर्व डायनॅमिक मूल्यांसाठी environment variables वापरा.
        
    *   गुप्त माहिती shared collections मध्ये ठेवू नका (secure variables / Postman Secret manager वापरा).
        
    *   प्रत्येक विनंतीसाठी लहान, लक्ष केंद्रीत टेस्ट लिहा.
        
    *   डेटा-आधारित टेस्टसाठी डेटा फाइल्स वापरा.
        
    *   कलेक्शनचे व्हर्जनिंग करा (forking वापरा) आणि विनंत्या दस्तऐवजीकरण करा.
        

* * *

# 12\. Browser Developer Tools for API Debugging / API डिबगसाठी ब्राउझर डेव्हलपर टूल्स

*   **English:** Open DevTools → Network tab to inspect API requests made by the web app, view request/response headers, payload, timing, and CORS errors. Compare these to Postman to isolate client vs server issues.
    
*   **Marathi:** DevTools → Network टॅब उघडा आणि वेब अॅपने केलेल्या API विनंत्या तपासा; request/response headers, payload, timing आणि CORS त्रुटी पाहा. हे Postman शी तुलना करून client vs server समस्या वेगळ्या करा.
    

* * *

# 13\. HTTP Status Codes — Explained / HTTP स्टेटस कोड — स्पष्टीकरण

*   **English:**
    
    *   **1xx — Informational:** Request received; server continuing process. (e.g., `100 Continue`)
        
    *   **2xx — Success:** Request succeeded. `200 OK` (standard success), `201 Created` (resource created).
        
    *   **3xx — Redirection:** Further action required (e.g., `301 Moved Permanently`, `302 Found`).
        
    *   **4xx — Client Error:** Problem with request (e.g., `400 Bad Request`, `401 Unauthorized`, `403 Forbidden`, `404 Not Found`, `422 Unprocessable Entity`).
        
    *   **5xx — Server Error:** Server failed to fulfill a valid request (e.g., `500 Internal Server Error`, `502 Bad Gateway`, `503 Service Unavailable`).
        
*   **Marathi:**
    
    *   **1xx — माहितीपर:** विनंती प्राप्त झाली; सर्व्हर प्रक्रिया जारी ठेवतो. (उदा., `100 Continue`)
        
    *   **2xx — यश:** विनंती यशस्वीरित्या पार पडली. `200 OK` (सामान्य यश), `201 Created` (रिसोर्स तयार झाला).
        
    *   **3xx — पुनर्निर्देशन:** पुढची क्रिया आवश्यक आहे (उदा., `301 Moved Permanently`, `302 Found`).
        
    *   **4xx — क्लायंट त्रुटी:** विनंतीत समस्या आहे (उदा., `400 Bad Request`, `401 Unauthorized`, `403 Forbidden`, `404 Not Found`, `422 Unprocessable Entity`).
        
    *   **5xx — सर्व्हर त्रुटी:** वैध विनंती पूर्ण करण्यात सर्व्हर अयशस्वी. (उदा., `500 Internal Server Error`, `502 Bad Gateway`, `503 Service Unavailable`).
        

* * *

# 14\. Example Postman Workflow (step-by-step) / Postman वर्कफ्लो (टप्प्याटप्प्याने)

*   **English:**
    
    1.  Import or create collection for your API.
        
    2.  Create environments (dev/stage/prod) with base URLs and credentials.
        
    3.  Add requests grouped by resource; add sample request bodies and descriptions.
        
    4.  Write pre-request script to set auth token; write tests to validate schema and status.
        
    5.  Run collection with sample data in Collection Runner locally.
        
    6.  Export collection and environment; integrate with CI using Newman.
        
    7.  Publish docs and set up monitors for uptime checks.
        
*   **Marathi:**
    
    1.  तुमच्या API साठी collection इम्पोर्ट किंवा तयार करा.
        
    2.  dev/stage/prod environment तयार करा ज्यात base URLs आणि credentials असतील.
        
    3.  resource नुसार विनंत्या गटबद्ध करा; नमुना बॉडी आणि वर्णन जोडा.
        
    4.  auth token सेट करण्यासाठी pre-request स्क्रिप्ट लिहा; schema आणि status पडताळण्यासाठी टेस्ट लिहा.
        
    5.  Collection Runner ने डेटा वापरून स्थानिकरित्या कलेक्शन चालवा.
        
    6.  कलेक्शन आणि एन्व्हायर्नमेंट एक्सपोर्ट करा; Newman वापरून CI मध्ये इंटिग्रेट करा.
        
    7.  डॉक्युमेंट प्रकाशित करा आणि uptime तपासण्यासाठी मॉनिटर सेट करा.
        

* * *

# 15\. Extra: Sample Assertions & Utilities / अतिरिक्त: नमुना assertions व उपयोगी कोड

*   **English (tests):**
    

`// check response time < 500ms pm.test("Response time is OK", function () {   pm.expect(pm.response.responseTime).to.be.below(500); });  // validate JSON schema (using ajv or a minimal check) const jsonData = pm.response.json(); pm.test("has user id", () => pm.expect(jsonData.id).to.be.a('number'));`

*   **Marathi (वर्णन):** वरील टेस्टमध्ये प्रतिसाद वेळ तपासतो आणि JSON मध्ये `id` हा नंबर असल्याची खात्री करतो.
    

* * *

# Closing / समारोप

*   **English:** This guide covers Postman basics through advanced automation with clear examples and real-world workflows. If you want, I can:
    
    *   produce a downloadable Markdown or PDF,
        
    *   create a compact cheat-sheet, or
        
    *   generate sample Postman collections and environment JSON files.
        
*   **Marathi:** हा मार्गदर्शक Postman च्या मूलभूत गोष्टींपासून प्रगत ऑटोमेशनपर्यंत खऱ्या जगातील वर्कफ्लो आणि उदाहरणांसह मांडतो. हवे असल्यास मी:
    
    *   Markdown किंवा PDF डाउनलोड करण्यासाठी तयार करू शकतो,
        
    *   संक्षिप्त चीट-शीट बनवू शकतो, किंवा
        
    *   नमुना Postman collection आणि environment JSON फाइल्स तयार करू शकतो.
