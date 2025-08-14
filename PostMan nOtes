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

## 4. Postman Advanced Features / Postman प्रगत वैशिष्ट्ये

### Environment Variables / एन्व्हायर्नमेंट व्हेरिएबल्स
- **English:** Local, Global, and Collection-level variables for dynamic values.  
- **Marathi:** डायनॅमिक व्हॅल्यूसाठी Local, Global आणि Collection-स्तरीय व्हेरिएबल्स.

### Test Scripts (JavaScript + Chai Assertions) / टेस्ट स्क्रिप्ट्स
- **English:** Example:  
```javascript
pm.expect(pm.response.code).to.equal(200);
Marathi: उदाहरण:

javascript
Copy
Edit
pm.expect(pm.response.code).to.equal(200);
Automated Test Runs & Reports / ऑटोमेटेड टेस्ट रन आणि रिपोर्ट्स
English: Use Collection Runner to execute multiple APIs with datasets.

Marathi: Collection Runner वापरून अनेक API डेटासेटसह चालवा.

5. Advanced Postman / Newman
Newman Introduction / Newman परिचय
English: Newman is a CLI tool to run Postman collections.

Marathi: Newman हे Postman कलेक्शन चालवण्यासाठी CLI टूल आहे.

Installation & Setup / इन्स्टॉलेशन व सेटअप
English:

bash
Copy
Edit
npm install -g newman
Marathi:

bash
Copy
Edit
npm install -g newman
Run Collections from Newman / Newman मधून कलेक्शन चालवा
English:

bash
Copy
Edit
newman run collection.json
Marathi:

bash
Copy
Edit
newman run collection.json
Command Line Options / कमांड लाइन पर्याय
English:

--environment

--iteration-data

--reporters

Marathi:

--environment

--iteration-data

--reporters

Generate HTML Test Report / HTML टेस्ट रिपोर्ट तयार करा
English:

bash
Copy
Edit
newman run collection.json -r html
Marathi:

bash
Copy
Edit
newman run collection.json -r html
6. Postman Collections & Documentation / Postman कलेक्शन आणि दस्तऐवजीकरण
Create collections & folders.

Create from API schema.

Maintain collections.

Use Postman Console & Logs.

Pre-request scripts.

Code snippets for testing.

API monitoring.

Publish documentation.

7. Team Collaboration / टीम सहकार्य
Mock server creation.

Team & personal workspaces.

Import/export Postman data.

8. Integration & Automation / एकत्रीकरण आणि ऑटोमेशन
Collection Runner & summary reports.

Run with Docker.

Run with Jenkins.

9. Browser Developer Tools for API Debugging / ब्राउझर डेव्हलपर टूल्स
What is Developer Tool (Chrome/Firefox).

Check request/response in Network tab.

Inspect backend API calls.

10. HTTP Status Codes / HTTP स्टेटस कोड्स
1xx – Informational (उदा. 100 Continue)

2xx – Success (उदा. 200 OK, 201 Created)

3xx – Redirection (उदा. 301 Moved Permanently)

4xx – Client Error (उदा. 400 Bad Request, 401 Unauthorized)

5xx – Server Error (उदा. 500 Internal Server Error)
