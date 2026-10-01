# Network Request Analysis: HTTP Status Codes

**Context:** This document demonstrates the analysis and monitoring of HTTP requests using the browser's Developer Tools (DevTools - Network tab). The goal is to identify how the application behaves depending on the status code returned by each request, and which side (client or server) is responsible when something goes wrong.

---

## Analyzed Requests

| Request Name | Method | Request URL | Status Code | Category |
| :--- | :---: | :--- | :--- | :--- |
| `index.json` | GET | `https://conduit.mate.academy/_next/data/.../index.json` | **200 OK** | 2xx – Success |
| `admin.json` | GET | `https://conduit.mate.academy/_next/data/.../admin.json` | **304 Not Modified** | 3xx – Redirection (cache) |
| `dummy` | GET | `https://example.com/dummy?data=someData` | **404 Not Found** | 4xx – Client Error |
| `500` | GET | `https://mock.httpstatus.io/500` | **500 Internal Server Error** | 5xx – Server Error |

---

## Practical Analysis

* **200 OK:** The communication with the server was successful and the data was returned as expected.
* **304 Not Modified:** The requested resource has not changed since the last access, so the server tells the browser to reuse its cached version instead of downloading it again (performance optimization). It belongs to the 3xx class, not to the 2xx success class.
* **404 Not Found:** The client requested a route or file that does not exist on the server. A 4xx code means the problem is in the *request* (wrong URL, missing resource, invalid data), not necessarily in the front-end code.
* **500 Internal Server Error:** The server failed to process a valid request, which points to a back-end failure that must be investigated in the application logs.

**How this helps when reporting bugs:** checking the Network tab makes it possible to attach the failing request, its status code, and the response to the bug report, helping the team route the defect to the right side (front-end or back-end) faster.
