# 🌐 Web Application Penetration Testing

## Objective

The objective of this project was to perform penetration testing on intentionally vulnerable web applications using Burp Suite Professional and the PortSwigger Web Security Academy. The assessment focused on identifying and exploiting common OWASP Top 10 vulnerabilities in a controlled lab environment.

---

## Tools Used

* Burp Suite Professional
* Mozilla Firefox
* PortSwigger Web Security Academy

---

## Environment

* Operating System: Windows 11
* Browser: Firefox
* Testing Platform: PortSwigger Web Security Academy

---

# SQL Injection – WHERE Clause Vulnerability

## Objective

To identify and exploit a SQL Injection vulnerability in a web application that allowed retrieval of hidden products.

---

## Lab

PortSwigger Web Security Academy

---

## Tools Used

* Burp Suite Professional
* Firefox Browser

---

## Methodology

1. Accessed the product category page.
2. Intercepted the HTTP request.
3. Modified the vulnerable category parameter inside the intercepted HTTP request using Burp Suite Repeater.
4. Injected the payload:

```sql
' OR 1=1--
```

5. Retrieved hidden and unreleased products.
6. Successfully solved the lab.

---

## Skills Learned

* SQL Injection
* HTTP Request Manipulation
* Database Query Logic
* Burp Suite Repeater


# Reflected Cross-Site Scripting (XSS)

## Objective

To identify and exploit a Reflected Cross-Site Scripting (XSS) vulnerability in a web application by injecting a malicious JavaScript payload into the application's canonical link tag.

---

## Description

The web application reflected user-supplied input within the HTML response without proper output encoding. By manipulating the vulnerable parameter, a JavaScript payload was injected into the canonical link tag, allowing arbitrary script execution in the browser. Successful execution confirmed the presence of a Reflected XSS vulnerability.

---

## Payload Used

```html
' accesskey='x' onclick='alert(1)
```

### Payload Explanation

* **`'`** closes the existing HTML attribute.
* **`accesskey='x'`** assigns a keyboard shortcut to the injected element.
* **`onclick='alert(1)'`** injects JavaScript that displays an alert dialog when the element is activated.

---

## Result

The injected payload executed successfully, displaying a JavaScript alert box (`alert(1)`). This confirmed that user input was reflected into the page without proper sanitization or output encoding, resulting in successful exploitation of the Reflected XSS vulnerability. The PortSwigger Web Security Academy lab was successfully solved.

---

## Skills Learned

* Reflected Cross-Site Scripting (XSS)
* HTML Attribute Injection
* JavaScript Payload Injection
* Client-Side Security Testing
* Input Validation Testing
* Output Encoding Concepts
* Web Application Security Testing


# Broken Authentication

## Objective

To identify and exploit a Broken Authentication vulnerability by performing username enumeration and password guessing attacks using Burp Suite Intruder, ultimately gaining unauthorized access to a valid user account.

---

## Description

The application returned different HTTP responses for valid and invalid usernames during the login process. This behavior allowed user enumeration by identifying valid usernames based on response differences. After discovering a valid username, a dictionary-based password attack was performed using Burp Suite Intruder to identify the correct password and successfully authenticate to the application.

---

## Method Used

### Username Enumeration

* Captured the login request using Burp Suite Proxy.
* Sent the request to Burp Suite Intruder.
* Used a username wordlist to test multiple usernames.
* Compared the HTTP responses to identify a valid username.

### Password Enumeration

* Reused the valid username obtained from the previous step.
* Performed a dictionary attack using a password wordlist.
* Identified the correct password based on the application's successful authentication response.

---

## Result

The assessment successfully identified a valid username and recovered the corresponding password using a dictionary attack. Login was successfully achieved, confirming the presence of a Broken Authentication vulnerability caused by distinguishable authentication responses and weak password security. The PortSwigger Web Security Academy lab was successfully solved.

---

## Skills Learned

* Broken Authentication Testing
* Username Enumeration
* Password Enumeration
* Burp Suite Intruder
* HTTP Response Analysis
* Dictionary-Based Password Attacks
* Authentication Security Assessment
* Web Application Security Testing


## Key Takeaways

- Learned to identify and exploit common OWASP Top 10 vulnerabilities.
- Gained hands-on experience with Burp Suite Professional.
- Improved understanding of HTTP requests and responses.
- Practiced secure testing in a controlled lab environment.

---

## Mitigation Strategies

- Validate and sanitize all user input.
- Use parameterized queries to prevent SQL Injection.
- Implement output encoding and Content Security Policy (CSP) to mitigate XSS.
- Enforce generic authentication error messages, strong password policies, account lockout mechanisms, and Multi-Factor Authentication (MFA) to reduce authentication-related risks.

---

## Disclaimer

All testing was performed in authorized PortSwigger Web Security Academy lab environments for educational purposes only.
