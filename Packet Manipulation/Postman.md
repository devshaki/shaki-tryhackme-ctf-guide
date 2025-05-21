Postman is **the** tool for sending custom packets and interacting with API's.
It allows us to craft and modify our HTTP requests and view the response

With Postman you can:
- Modify request methods, headers, cookies, and payloads
- Test authentication mechanisms
- Directly interact with the backend skipping browser side limitations
- Inspect full HTTP responses including status codes, headers, and body

### Use case example: 
**Bypassing Client-Side SQL Injection Protection**
Some web applications attempt to prevent SQL injection by using JavaScript-based input validation on the login form, This kind of validation runs only in the browser.

By using Postman we can bypass the browser and test the server for SQL injection directly
