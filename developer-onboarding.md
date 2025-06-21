# Developer Onboarding

Welcome to the CPD Progress Tracker API documentation.

This guide helps new developers:

- Understand available endpoints  
- Get started with authentication  
- Explore sample queries  
- Use tools like Postman or curl  

---

## 1. OpenAPI Spec

The API reference is defined using an OpenAPI 3.0 spec (`openapi.yaml`) located in this repository. You can import it into tools like:

- [Postman](https://www.postman.com/)  
- [Insomnia](https://insomnia.rest/)  
- [Swagger UI](https://swagger.io/tools/swagger-ui/)  

---

## 2. Authentication

All endpoints require a bearer token.

To request access, contact your organisation’s admin or the Hunting Stewart support team.

Once you’ve received your token, include it in the `Authorization` header like this:

```
Authorization: Bearer your_token_here
```

---

## 3. Base URL

Use the following base URL for all API requests:

```
https://api.huntingstewart.co.uk/v1/
```

---

## 4. Quick Start Example

### Get CPD Progress for a Care Worker

**Endpoint:**

```
GET /careworkers/{id}/cpd-progress
```

**Sample Request:**

```
curl -X GET https://api.huntingstewart.co.uk/v1/careworkers/12345/cpd-progress \
  -H "Authorization: Bearer your_token_here"
```

**Sample JSON Response:**

```json
{
  "totalHours": 35,
  "completedHours": 28,
  "dueBy": "2025-12-31"
}
```

**Possible Errors:**

- `401 Unauthorized` – Invalid or expired token  
- `404 Not Found` – Care worker ID not found  

---

## 5. Best Practices

- Always use HTTPS  
- Rotate tokens regularly  
- Log errors locally and include the full response for debugging  
- Never expose tokens in client-side code  

---

## 6. Support

For help with integration or sandbox access, contact:

📧 api.support@huntingstewart.co.uk


