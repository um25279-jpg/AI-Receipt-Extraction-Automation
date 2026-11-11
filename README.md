# AI-Powered Receipt Data Extraction Automation

## Project Overview
An automated receipt processing system built using n8n, Google Gemini and Google Sheets. It extracts transaction information from receipt images and automatically stores the data in a spreadsheet.

## Problem Statement
Manual entry of receipt information is time-consuming and prone to human errors.

## Solution
Developed an AI-powered workflow that processes receipt images, extracts relevant information and automatically updates Google Sheets.

## Workflow Architecture
1. **Receipt Upload:** Users upload receipt images through an n8n form.
2. **AI Processing:** Google Gemini analyses the receipt image.
3. **Data Structuring:** JavaScript converts the AI response into structured JSON.
4. **Data Storage:** Google Sheets automatically stores the extracted information.

## Information Extracted
- Merchant Name
- Receipt Date
- Receipt Number
- Total Amount
- Tax Amount
- Payment Method

## Technology Stack
- n8n – Workflow automation
- Google Gemini API – Image analysis and information extraction
- JavaScript – JSON parsing
- Google Sheets – Data storage

## Testing and Results

Tested using two different receipt images.

| Test | Merchant | Result |
|---|---|---|
| 1 | THE GOURMET CORNER | Successful |
| 2 | THE HUNGRY SPOON | Successful |

Both receipts were successfully processed and their information was automatically stored in Google Sheets.

## Future Improvements
- Extract individual purchased items and quantities.
- Automatically categorise expenses.
- Detect duplicate receipts.
- Develop an expense analytics dashboard.

## How to Run
1. Import the workflow JSON into n8n.
2. Configure Gemini API credentials.
3. Connect your Google Sheets account.
4. Select your destination spreadsheet.
5. Upload a receipt through the form.

## Test Results

The workflow was tested using multiple receipt images to verify extraction accuracy and automated data storage.

| Test Case | Merchant | Receipt Number | Total Amount | Tax | Payment Method | Status |
|---|---|---|---:|---:|---|---|
| TC01 | THE GOURMET CORNER | 4519 | 111.02 | 7.52 | VISA | Passed |
| TC02 | THE HUNGRY SPOON | 5098 | 226.94 | 15.44 | AMEX | Passed |

### Test Observations
- Gemini successfully extracted the required receipt information.
- Extracted information was converted into structured JSON.
- Google Sheets successfully stored the extracted information.
- Multiple receipts were added as separate rows.

### Overall Result
2 out of 2 tested receipts were successfully processed and stored in Google Sheets.
