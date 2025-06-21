# Integration Guide

This guide walks local authority IT teams through integrating their systems with the CPD Progress Tracker API.

## Step 1: Get API Access

Contact Hunting Stewart support to request an API token and integration credentials.

## Step 2: Authentication

Include the provided bearer token in your API requests:

```http
GET /care-workers/12345/cpd-progress HTTP/1.1
Authorization: Bearer YOUR_TOKEN_HERE

