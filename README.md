# OG Hemp — WordPress Development Repo

## About
This is the core WordPress repository for OG Hemp. It contains custom themes, plugins, and configuration templates.

## Local Setup Steps

1. **Clone the repository:**
   ```bash
   git clone https://github.com/OG-HEMP/OG.git wp-content
   cd wp-content
   git submodule update --init --recursive
   ```

2. **Configure Database:**
   - Copy `wp-config.example.php` to your WordPress root (one level above this repo).
   - Fill in your local database credentials.
   ```bash
   cp wp-config.example.php ../wp-config.php
   ```

3. **Import Database:**
   ```bash
   wp db import your-dump.sql --path=../
   wp search-replace 'https://www.oghemp.in' 'http://localhost:PORT' --all-tables --path=../
   ```

## Branching Strategy
- `main`: Production-ready code.
- `antigravity-dev`: Active development branch for Antigravity edits.

## MCP Setup
This repo uses the [WordPress MCP Adapter](https://github.com/WordPress/mcp-adapter) to allow Antigravity to interact with the site via the Model Context Protocol.
