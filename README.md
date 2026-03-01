Workflow Automation Overview	
	
Quick Summary
This is a fully automated ticketing system that converts user concerns from Google Sheets directly into Jira tickets with minimal manual intervention. The system is currently in Run mode and includes 11 integrated steps.

📊 High-Level Workflow
User Concerns Submitted
        ↓
Level 1 Support Reviews
        ↓
Check "RUN" Checkbox
        ↓
✅ Automatic Processing:
   • Email sent to reporter
   • Work Type → Jira Issue Type
   • Priority → Jira Priority Level
   • Module → Auto-assigns to right person
   • Creates Jira Ticket
   • Converts & attaches Google Drive file
   • Stores Ticket ID in both sheets

🔧 The 10 Steps Explained
 # 	 Action 	 What It Does 
 1 	 Google Sheets Trigger 	 Watches '[Lvl 1] User Concerns' sheet for RUN column changes 
 2 	 Send Email (Gmail) 	 Notifies reporter that their concern has been ticketed 
 3  Formatter: Issue Type 	 Converts Task/Story/Bug → Jira ID (10003/10004/10005) 
 4 	 Formatter: Priority 	 Converts Highest/High/Medium/Low/Lowest → Jira ID (1-5) 
 5	 Formatter: Assignee 	 Converts Module → Person (Admissions→Peter, Finance→John, Academic→April) 
 6 	 Create Jira Issue 	 Creates ticket with dynamic Issue Type, Priority, Assignee, and description 
 7 	 Code: URL Converter 	 Converts Google Drive view links to direct download URLs 
 8	 Add Attachment 	 Attaches the converted Google Drive file to the Jira ticket 
 9	 Update [Lvl 1] Sheet 	 Stores Jira Ticket ID in Column M of '[Lvl 1] User Concerns' 
 10 	 Update User Concerns Sheet 	 Stores Jira Ticket ID in Column I of 'User Concerns' sheet 
 
📈 Data Flow
Input: User fills '[Lvl 1] User Concerns' sheet with:

Module (Admissions/Finance/Academic)
Priority (Highest to Lowest)
Work Type (Task/Story/Bug)
Issue description
Reporter email
Google Drive attachment link
RUN checkbox (the trigger)
Output: Automatic creation of:

🎯 Key Features
✅ Smart Assignment: Right person gets the ticket based on module
✅ Automatic Formatting: User-friendly inputs convert to Jira-compatible IDs
✅ File Handling: Google Drive attachments automatically converted and attached
✅ Audit Trail: Ticket IDs stored for tracking
✅ Reporter Notification: Automatic email confirmation

⚙️Current Status
Mode: Run (actively processing)

For the sheets used for trial runs, see 'User Concerns' [User Concerns.xlsx](https://github.com/user-attachments/files/25663898/User.Concerns.xlsx)
 and '[Lvl 1] User Concerns' [[Lvl 1] User Concerns.xlsx](https://github.com/user-attachments/files/25663906/Lvl.1.User.Concerns.xlsx)
added in this repository.
