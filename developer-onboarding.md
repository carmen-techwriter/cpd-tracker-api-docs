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

All integrations require a bearer token. Reach out to the admin team at Hunting Stewart to provision your access credentials.

Tokens must be included in the Authorization header for all requests:

Authorization: Bearer YOUR_TOKEN_HERE

## Next Steps

Once authenticated, you can begin by exploring the `/care-workers/{id}/cpd-progress` endpoint to retrieve CPD data for a given worker.

