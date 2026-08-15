# NginX-Node.js-PostgreSQL Stack

A self-hosted REST API stack: Nginx serving static content and reverse-proxying a Node.js REST API, with SSL encryption and a PostgreSQL backend.

## Overview

My first fully working REST API setup with Nginx-controlled static + API hosting and SSL. Includes a working PostgreSQL database with real schema/trigger design, a handful of drafted API endpoints, and a sample front-end submissions form (vanilla JS/HTML/CSS) that reads live from the database.

## What's in here

- Nginx config for static + reverse-proxied API hosting with SSL
- Node.js REST API using the `pg` package for connection pooling
- PostgreSQL schema with a trigger-based backup/log table for each main table
- Environment variables handled independently of the API files, so credentials aren't baked into the codebase
- A sample dynamic front-end form/display table (vanilla JS) pulling live data from the API

## Background

Built and iterated on this as my own dev server setup — it's where I actually learned Nginx configuration, SSL, database triggers, and structuring a REST API from scratch. It's not polished, but everything in it runs.

## Next up

- Separate the database pooling logic from the request-handling/listener files
- Build out a real user/auth flow (registration, login, password hashing)
- Clean up the Nginx config (drop the `.html` extensions from URLs)

--Nick
