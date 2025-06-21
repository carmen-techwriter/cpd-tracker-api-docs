# Integration Guide

This guide walks local authority IT teams through integrating their systems with the CPD Progress Tracker API.

## Step 1: Get API Access

Contact Hunting Stewart support to request an API token and integration credentials.

## Step 2: Authentication

Include the provided bearer token in your API requests:

```http
GET /care-workers/12345/cpd-progress HTTP/1.1
Authorization: Bearer YOUR_TOKEN_HERE
### Step 3: Handle Responses

All responses are JSON. A typical success response:

```json
{
  "totalHours": 35,
  "completedHours": 28,
  "dueBy": "2025-12-31"
}

---

### ✅ **2. Developer Onboarding Guide → `developer-onboarding.md`**

This should be its own markdown file and already exists — just finish populating it with the following:

```markdown
# Developer Onboarding

Welcome to the CPD Progress Tracker API documentation.

This guide will help new developers:

- Understand available endpoints
- Get started with authentication
- Explore sample queries
- Use tools like Postman or curl

For full reference, see the `openapi.yaml`.

## Postman Collection

You can import the OpenAPI spec into Postman for easier testing.

## Token Setup

All integrations require a bearer token.  
Reach out to the admin team at Hunting Stewart to provision your token.

