# IDOR / Broken Access Control Notes

## What is IDOR?

IDOR stands for **Insecure Direct Object Reference**.

It happens when an application exposes an object identifier such as:

- User ID
- Order ID
- Invoice ID
- Document ID
- File ID

and the server does not properly verify whether the logged-in user is allowed to access that object.

---

## Simple Example

User A owns:

```http
GET /api/orders/1001
