Burp Suite Request Interception Report

Target Information

| Item | Details |
|---|---|
| Target URL | http://localhost:3000 |
| Tool Used | Burp Suite Community Edition |
| Testing Type | HTTP Request Interception |


Captured Requests

| Request Type | Endpoint | Observation |
|---|---|---|
| GET | / | Homepage request captured successfully |
| GET | /assets | Static resource request identified |
| GET | /rest/products/search | Product search API request observed |
| POST | /rest/user/login | Login API request captured successfully |


Headers Observed

- Host Header
- User-Agent Header
- Cookie Header
- Accept Header
- Connection Header



Cookies Observed

- Session cookies were visible during request interception.
- Browser request information was observable.
- HTTP request headers were captured successfully.


Security Observations

- Burp Suite successfully captured HTTP traffic between browser and Juice Shop.
- API endpoints were visible through request interception.
- Request headers and cookies were observable.
- Login requests and API communication were analyzed successfully.


Findings

| Finding | Description |
|---|---|
| Visible API Endpoints | Multiple REST API endpoints were observable |
| Request Header Visibility | Browser headers and request metadata were visible |
| Session Cookie Exposure | Session cookies could be viewed during interception |
| Traffic Monitoring | HTTP requests were successfully monitored |



Conclusion

Burp Suite Community Edition successfully intercepted and analyzed HTTP requests from the OWASP Juice Shop application running on localhost. The testing demonstrated how web traffic, API requests, headers, and cookies can be inspected during security assessments.