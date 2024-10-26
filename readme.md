This 3-tier rule engine application makes it easy to determine user eligibility based on attributes like age, department, income, and spending habits. What makes it powerful is that it uses an Abstract Syntax Tree (AST) to represent rules, allowing for dynamic creation, modification, and combination of these rules on the fly.

Key Features
Create Rules: You can define rules using conditions like age > 30 or department = 'Sales'.
Combine Rules: Need something more complex? Multiple rules can be merged into one, giving you endless flexibility.
Evaluate Rules: The system compares user data against the defined rules and tells you whether a user meets the conditions.
Error Handling: If there's a problem—like incorrect rule syntax or data format—you’ll get meaningful feedback.
How the System is Organized
The project is organized into three clear layers for better structure:

App Layer: This contains everything that runs the backend logic—such as rule creation, combination, evaluation, and API functions.
Database Layer: Manages data storage using SQLite, ensuring persistence for rules and configurations.
Frontend Layer: The user interface makes it easy to create rules and run evaluations via a web interface.
You’ll find folders for:

Static files (like CSS and JavaScript to enhance the user interface)
Templates (where the main UI lives)
Unit tests (to make sure everything works as expected)
Why This Design Works Well
3-Tier Architecture: This setup separates the logic into three layers—backend, database, and frontend—making the app easier to maintain and scale.
AST-based Rules: Using an Abstract Syntax Tree gives the flexibility to create, edit, and combine rules efficiently.
Error Handling: Instead of crashing, the app will provide clear feedback if the rule syntax or data input isn’t correct.
User-Friendly Interface: The UI is built to be simple and intuitive, with clear feedback to guide users through the rule creation and evaluation process.
How to Get Started
Set Up Your Environment:

Make sure you have Python (version 3.6 or higher) and SQLite installed.
Install dependencies by running the command pip install -r requirements.txt.
Initialize the Database:

This only takes a second. Run the database script and you're good to go.
Launch the App:

Run the main script, and you can access the app on your browser at http://127.0.0.1:5000/.
Testing the System
You can try out a sample rule in the app:
((age > 30 AND department = 'Sales') OR (age < 25 AND department = 'Marketing')) AND (salary > 50000 OR experience > 5)

Once the rule is created successfully, input the following data to test it:

json
Copy code
{
  "age": 50,
  "department": "Sales",
  "salary": 60000,
  "experience": 10
}
If everything is working, you’ll see a result confirming whether the user meets the conditions.

Improvements You Could Consider
Performance Optimization: Cache frequently used rules to make the app faster.
Security Measures: Make sure input data is sanitized to prevent malicious input.
UI Enhancements: Add design elements like progress spinners or success notifications for better feedback.
Database Flexibility: Consider using SQLAlchemy to make database management more scalable and organized.
