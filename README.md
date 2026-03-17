# PM-04-PS01
SECTION 1: PM-04-PS01: Identify the process and objects from the process design document (PDD) pertaining to the software RPA solution
 
 
# Scenario
 
Welcome to your next major project. As an RPA Developer, your role is to identify and automate business processes to improve efficiency and reduce errors. For this activity, you are consulting for "Mzansi Mart," a fast-growing South African e-commerce company that sells locally-sourced goods.
Mzansi Mart is currently facing a significant operational bottleneck. All online orders are received as email attachments (CSV files) and are manually entered by an employee into their legacy "Order Management System" (a simple web portal). This manual process is slow, prone to data entry mistakes, and cannot keep up with the company's growth. Your task is to design and develop an RPA solution to automate this process.
 
## The Task
 
You will receive a Process Design Document (PDD) outlining the required automation steps. Your mission is to:
1.	Analyse the PDD to understand the business process.
2.	Select a suitable RPA tool from the list of approved applications (UiPath, Automation Anywhere, Blue Prism, Microsoft Power Automate, Kofax RPA, WorkFusion).
3.	Develop a functional software robot that automates the order processing.
4.	Complete the practical assessment tasks outlined below.
Project Deliverables
- A functional RPA solution (the software robot) developed using your chosen tool.
- A completed "Student Worksheet" (provided in a separate file).
Process Design Document (PDD) - Mzansi Mart Order Processing
This document outlines the high-level steps for the "Order Processing Automation" project.
Process Overview
- Trigger: New email arriving in the "shanonlutchman@gmail.com" mailbox.
- Input: CSV file attached to the email, containing order details.
- Output: Order successfully submitted in the Mzansi Mart Order Management System. A confirmation email is sent.
Step-by-Step Process
1.	Receive Orders Email: The bot should monitor the specified mailbox for new emails with the subject line containing "New Mzansi Mart Order."
2.	Extract Data: The bot must download the attached CSV file to a local folder and read its contents.
3.	Validate Data: The bot will perform a basic validation check on the customer_id column to ensure all values are valid 8-digit strings.
4.	Access Order Management System: The bot should open a web browser and navigate to the Mzansi Mart Order Management System URL -(https://mzansi-order-automata.lovable.app/orders/login)
5.	Login Details : username - admin, password- admin123
 
6.	Log In: The bot will enter the username and password stored in a secure credential vault and click the "Log In" button.
7.	Process Each Order: For each row of data from the CSV file, the bot will:
o	Navigate to the "New Order" page.
o	Enter the customer_id, product_sku, and quantity into the corresponding fields.
o	Click the "Add Item" button.
o	Repeat until all items for the order are added.
o	Click the "Submit Order" button.
8.	Confirmation: Upon successful submission, the bot should capture the Order Confirmation Number from the screen and send a confirmation email to the customer's email address (from the CSV data), with the subject "Your Mzansi Mart Order is Confirmed."
9.	Error Handling: If any step fails (e.g., website element not found, invalid data), the bot should log the error and send an alert email to the RPA support team.
Practical Assessment Tasks
This section details the practical tasks to be completed, aligning each with a specific learning outcome.
Task 1: PDD Analysis and Tool Selection (PA0103, PA0104, AK0103)
- PA0104 (Analyse PDD)
Using the provided PDD in the separate RPA_PDD_Diagram.md file, explain how you would break down the process into smaller, manageable automations. Describe the logic and flow of your solution.
- PA0103 (Select a suitable tool)
Choose one of the approved RPA tools. Justify your selection based on the requirements of the Mzansi Mart project. Consider factors like ease of integration with web applications, cost, and community support in South Africa.
- AK0103 (Processes and workflows)
Based on your PDD analysis, create the workflow diagram for your solution in your chosen RPA tool.
Task 2: Solution Development and Problem-Solving (AK0101, PA0106, PA0105)
- AK0101 (Scripting/Programming)
Provide a code snippet from your RPA solution that demonstrates how you handle the data validation for the customer_id field. You can use pseudocode or a real snippet from your chosen tool.
- PA0106 (Problem-Solving) 
Describe two approaches you would implement to handle a scenario where the "Submit Order" button on the website changes its HTML id attribute. Explain how your solution would adapt to this change.
- PA0105 (Attention to detail) 
The quantity column in the provided data sets can sometimes be empty. Detail the logic and steps your bot will take to handle this specific empty cell, preventing a runtime error.
Task 3: Integration and Documentation (PA0101, PA0107, IAC0101)
- PA0101 (Interaction) 
Describe how your RPA solution will interact with the different components of the system (Email client, File System, Web Application, and the secure credential vault). You can use a high-level component diagram or a detailed text description.
- PA0107 (Knowledge Base)
You have discovered a new scenario: a customer places an order for an item that is out of stock. Outline a new test case and a corresponding script (or pseudocode) to handle this scenario. Document how you would add this new information to the project's knowledge base for future use.
- IAC0101 (PDD Analysis)
From the provided PDD, extract and list all the "objects" (e.g., Email, CSV File, Web Page) and the "processes" (e.g., Log In, Enter Order Details) that your bot needs to interact with.
Data Sets
- sample_orders_batch_1.csv
- sample_orders_batch_2.csv
- Note: These files are provided as separate, downloadable artifacts. Use the sample_orders_batch_1.csv for your initial development and the sample_orders_batch_2.csv for your testing and error handling.
