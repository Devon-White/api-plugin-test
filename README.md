# Yarn vs NPM Issue - Docusaurus OpenAPI Plugin

## Problem
Docusaurus with OpenAPI plugin works with Yarn but has React hook errors with NPM.

## Step-by-Step Testing

**Step 1: Test with Yarn first (to see it working):**
```bash
npm run test-yarn
```
- This will start the dev server successfully
- Navigate to the site and verify everything works

**Step 2: Test with NPM (to see the issue):**
```bash
npm run test-npm  
```
- This will start the dev server
- Navigate to the site and you'll see: `Hook useDoc is called outside the <DocProvider>`

## What Each Test Does
1. **Clean**: Removes node_modules and lock files
2. **Install**: Installs dependencies with chosen package manager
3. **Start**: Generates API docs and starts dev server

## Expected Results
- **Yarn**: Starts successfully, site works properly
- **NPM**: Starts but shows error: `Hook useDoc is called outside the <DocProvider>`

Use this to demonstrate the issue to maintainers. 