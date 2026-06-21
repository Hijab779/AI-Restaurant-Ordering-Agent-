## AI Restaurant Ordering Agent

An AI-powered restaurant assistant built with n8n, Google Gemini, and Google Sheets.

## Features
Accepts food orders
Checks inventory availability
Confirms or rejects orders
Stores orders in a database
Answers restaurant FAQs
Maintains conversation memory
## Tech Stack
n8n
Google Gemini API
Google Sheets
AI Agent
## How I Built This Project

This project was built using n8n as the automation platform, Google Gemini as the AI model, and Google Sheets as the database.

### Workflow Overview

1. The workflow starts when a customer sends a message through the chat interface.

2. The message is passed to an AI Agent powered by Google Gemini.

3. The AI Agent follows a custom system prompt that allows it to:

   * Greet customers
   * Take food orders
   * Answer restaurant FAQs
   * Check inventory availability
   * Track order status

4. The AI Agent is connected to Google Sheets tools:

   * Inventory Sheet for checking stock levels
   * Orders Sheet for storing customer orders

5. When a customer places an order:

   * The AI first searches the Inventory Sheet.
   * It verifies whether the requested item is available in sufficient quantity.
   * If stock is available, the order is confirmed.
   * If stock is unavailable, the order is rejected and alternative items can be suggested.

6. Confirmed orders are automatically stored in the Orders Sheet with:

   * Customer Name
   * Food Item
   * Quantity
   * Order Status
   * Description

7. Memory nodes are used to maintain conversation context, allowing the AI Agent to handle multi-step interactions naturally.

### Example Flow

Customer → AI Agent → Inventory Check → Order Validation → Google Sheets Update → Customer Confirmation

### Key Learning Outcomes

* Building AI-powered business workflows using n8n
* Integrating Large Language Models (Google Gemini) with external databases
* Designing conversational AI systems
* Implementing inventory validation logic
* Automating order management processes
* Creating multi-step AI agent workflows with memory
