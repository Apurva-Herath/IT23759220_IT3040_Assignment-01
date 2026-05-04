# IT23759220_IT3040_Assignment-01
Student: IT23759220
Target App: https://www.pixelssuite.com/chat-translator

Tool: Playwright (Python)
GitHub Repository: https://github.com/Apurva-Herath/IT23759220_IT3040_Assignment-01.git

Project Structure
Prerequisites
Python 3.11 or 3.12 — https://www.python.org/downloads/
Google Chrome (recommended) — https://www.google.com/chrome/
VS Code (recommended editor) — https://code.visualstudio.com/

Windows users: Make sure Python is added to your PATH during installation.

Setup & Installation (One-Time)

Open Command Prompt or VS Code Terminal, then run:

# Step 1 – Navigate into the project folder
cd path\to\IT23759220

# Step 2 – Upgrade pip
pip install -U pip

# Step 3 – Install required Python packages
pip install playwright openpyxl

# Step 4 – Install Playwright browsers
playwright install
How to Run the Tests

From inside the project folder in your VS Code terminal, run:

python IT23759220_test_automation.py --excel "IT23759220_Assignment 1 - Test cases.xlsx" --url "https://www.pixelssuite.com/chat-translator" --wait-ms 8000 --type-delay-ms 80 --slow-mo-ms 200 --save-every 1 --keep-open
What Happens When You Run It
Browser opens and loads https://www.pixelssuite.com/chat-translator
Each row in the Excel file is read in order
The Singlish input is typed into the Chat Sinhala input box
The Transliterate button is clicked
The actual Sinhala output is captured and written back to Excel
Status is set to PASS (actual == expected) or FAIL (mismatch)
Results are saved to the same Excel file after each row
Checking Results

After the run completes:

Open IT23759220_Assignment 1 - Test cases.xlsx
Check columns E (Actual Output) and F (Status)
All 50 negative test cases should show FAIL (they were designed to fail)
All 10 positive test cases should show PASS
Test Case Summary
Type	Count
Positive (expected Pass)	10
Negative (expected Fail)	50
Total	60
Singlish Input Types Covered (all 24 required)
Question forms
Command forms
Greetings
Requests
Responses
Repeated Words
Inputs with Punctuation Marks
Romanization / Spelling Variants
Isolated English Word Insertions in Singlish
Multi-Word English Phrases in Singlish
English Digital Terms in Singlish
Platform/App Names in Singlish
English Abbreviations/Acronyms in Singlish
English Clipped Forms in Singlish
Place Names Embedded in Singlish
Person Names Embedded in Singlish
Inputs with Numbers and Numeric Suffixes
Inputs with Currency
Inputs with Time Formats
Inputs with Dates
Inputs with Unit of Measurements
Inputs with Slang and Casual Phrasing
Online Identifiers in Singlish
Inputs Containing Emojis
Troubleshooting

"playwright: command not found"
→ Try:

python -m playwright install

Browser opens but no typing happens
→ Increase:

--wait-ms 10000 --slow-mo-ms 500

Excel not found error
→ Make sure IT23759220_Assignment 1 - Test cases.xlsx is in the same folder as IT23759220_test_automation.py

Output column stays empty
→ The site may have changed its layout. Try running without --headless to observe behavior.

Unicode/encoding errors on Windows
→ Run:

chcp 65001
