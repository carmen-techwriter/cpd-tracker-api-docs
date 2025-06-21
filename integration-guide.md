# Integration Guide

This guide walks developers through integrating with the CPD Progress Tracker API.

## Step 1: Authentication

All endpoints require a bearer token. Contact the Hunting Stewart admin team to request API access and credentials.

Once obtained, include your token in the request header:

```
Authorization: Bearer YOUR_TOKEN_HERE
```

## Step 2: Retrieve CPD Progress

To get a worker's CPD data, use the following endpoint:

```
GET /care-workers/{worker_id}/cpd-progress
```

Replace `{worker_id}` with the relevant care worker’s ID.

### Example Request

```
GET /care-workers/12345/cpd-progress HTTP/1.1
Authorization: Bearer YOUR_TOKEN_HERE
```

## Step 3: Handle Responses

All responses are returned in JSON format.

### Success Response

```json
{
  "totalHours": 35,
  "completedHours": 28,
  "dueBy": "2025-12-31"
}
```

## Step 4: Error Handling

You may receive the following errors:

- **404** – Care worker ID not found  
- **401** – Invalid or expired token  
- **500** – Internal server error



