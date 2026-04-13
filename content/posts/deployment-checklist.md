+++
title = 'Pre-deployment Checklist'
date = 2026-03-24T12:52:34-05:00
draft = false
tags = ['unix']
Description = 'An app pre-deployment checklist'
ShowToc = true
weight = 0
+++

# Pre-deployment Checklist 

## Authorization

Users should only be able to access their resources and nothing else.

## Input validation

All inputs need to be validated and sanitized before making any kind of query or being executed in any capacity.

## CORS policy

Only requests by our domain will be processed by our APIs. 

## Rate limiting

Rate limit API endpoints.

## Password reset links

Set password reset links to expire after some time. 

## Catch unexpected errors 

Catch unexpected errors on the frontend.  
Make sure the user never sees a raw stack trace. 

## Indexing

Index on most commonly  queried fields.  
Don’t increase writing overhead if you don’t have to.

## Logging

Keep it simple. Don't add too much.

## Alerts

Add alerts. 

## Rollback 

I like to implement a Blue-Green deployment strategy.
