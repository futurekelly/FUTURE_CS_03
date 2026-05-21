# 🔐 API Security Risk Analysis and Vulnerability Assessment

## 📋 Project Overview

This project documents a practical **API Security Risk Analysis and Vulnerability Assessment** conducted using industry-standard cybersecurity tools including Burp Suite, Postman, OWASP ZAP, and Kali Linux.

The assessment focused on:
- API traffic interception
- Request manipulation
- HTTP method testing
- Response analysis
- Validation testing
- Burp Suite Repeater testing
- Security header inspection

Testing activities were performed against the educational demo API:

https://jsonplaceholder.typicode.com

The primary objective of the project was to demonstrate professional API security testing methodology and document the assessment process in a structured and ethical manner.

> ⚠️ Disclaimer: This assessment was conducted strictly for educational and internship purposes using a public demo API within a controlled testing environment. No malicious exploitation or unauthorized attacks were performed.

---

# 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|
| **Burp Suite Community Edition** | API interception, manipulation, and repeater testing |
| **Postman** | Sending and managing API requests |
| **OWASP ZAP** | Additional API and web security testing |
| **Kali Linux** | Penetration testing operating system |

---

# 🔍 Assessment Methodology

The assessment followed a structured API security testing workflow consisting of the following phases:

| Phase | Description |
|------|-------------|
| **Environment Setup** | Configuring Burp Suite proxy integration with Postman |
| **API Reconnaissance** | Discovering endpoints and observing API behavior |
| **Traffic Interception** | Capturing requests and responses using Burp Suite |
| **Request Manipulation** | Modifying requests, headers, and endpoints |
| **HTTP Method Testing** | Testing GET, PUT, and DELETE request methods |
| **Response Header Analysis** | Inspecting response headers and server information |
| **Burp Repeater Testing** | Replaying and modifying requests repeatedly |
| **Validation Testing** | Testing invalid object references and API responses |
| **Documentation & Reporting** | Recording findings, screenshots, and observations |

---

# 🚨 Key Testing Activities

| Activity | Status |
|---|---|
| API Traffic Interception | ✅ Completed |
| Endpoint Manipulation | ✅ Completed |
| Request Header Modification | ✅ Completed |
| HTTP Method Testing | ✅ Completed |
| Burp Repeater Testing | ✅ Completed |
| Validation & Error Handling Testing | ✅ Completed |
| Response Header Analysis | ✅ Completed |

---

# 🔑 Key Findings & Observations

## 🟡 Technology Disclosure

The API response headers exposed backend framework information through:

```http
X-Powered-By: Express

### Observation
Technology disclosure through HTTP response headers may reveal backend technologies used by the application infrastructure.

Attackers can use this information during reconnaissance to identify known vulnerabilities associated with specific frameworks or server technologies.

### Severity
Low

---

## 🟢 Security Headers Present

The API included security-related headers such as:

```http
X-Content-Type-Options: nosniff
```

### Observation
The presence of security headers helps improve browser-side protection and reduces the risk of MIME-type confusion attacks.

This indicates that basic security hardening mechanisms are implemented within the API infrastructure.

### Severity
Positive Observation

---

## 🟢 Rate Limiting Controls Observed

The API responses included rate limiting headers such as:

```http
X-RateLimit-Limit
X-RateLimit-Remaining
```

### Observation
The presence of rate limiting headers indicates that request throttling mechanisms are implemented to help reduce abuse, automated attacks, and excessive API consumption.

### Severity
Informational

---

## 🟢 Proper Validation & Error Handling

Invalid object requests such as:

```http
GET /users/999999
```

returned controlled responses:

```http
HTTP/2 404 Not Found
{}
```

### Observation
The API demonstrated proper validation handling and controlled error responses without exposing backend stack traces, database errors, or sensitive implementation details.

### Severity
Positive Observation

---

## 🟢 Successful Request Interception

API requests were successfully intercepted using Burp Suite proxy integration between Postman and the target API.

### Observation
Traffic interception allowed detailed inspection of:
- request headers
- HTTP methods
- API endpoints
- response structures
- server behavior

This demonstrated effective API traffic analysis methodology using professional security testing tools.

### Severity
Informational

---

## 🟢 HTTP Method Manipulation Testing

HTTP methods including GET, PUT, and DELETE were tested during the assessment.

Example tested methods:

```http
PUT /users/4
DELETE /users/4
```

### Observation
The API processed modified HTTP methods and returned simulated responses as expected for the educational testing environment.

This demonstrated practical API method manipulation and response analysis techniques.

### Severity
Informational

---

## 🟢 Burp Repeater Testing

Burp Suite Repeater was used to replay and modify requests repeatedly for validation testing and response analysis.

### Observation
Repeater testing enabled:
- endpoint manipulation
- invalid object testing
- response comparison
- repeated request analysis

The API consistently returned controlled responses during replay testing.

### Severity
Informational

---

# 📸 Evidence Screenshots

The repository contains screenshots demonstrating:

- Burp Suite proxy configuration
- API request interception
- HTTP history analysis
- Request manipulation
- HTTP method testing
- PUT and DELETE request handling
- Burp Repeater testing
- Validation testing
- Response header analysis
- Controlled error handling behavior

---

# 📁 Repository Structure

```bash
📦 api-security-risk-analysis/
├── 📁 screenshots/
├── 📄 API_Security_Risk_Analysis_Report.pdf
├── 📄 README.md
```
## 👤 Author

**Kelvin Mbise**


BSc Computer system and networking — Ardhi university(ARU)

Dar es Salaam, Tanzania

Internship: Future Interns

📧 [futurekelly360@gmail.com](mailto:futurekelly360@gmail.com)

📞 +255 616 802 135

🔗 [LinkedIn Profile](https://www.linkedin.com/in/kelvin-mbise-392034349/)

---

## 📄 License

This project is intended for **educational and academic purposes only**. 
