# DBMS-Group-Project
Final Project of DBMS 110 or Intro to Data Analytics

The Goal of this project was to work with a team, use critical thinking, apply skills, and design a database from the scenerio given. 

FINAL GRADE: 77/85 

Scenario 

After building a successful Real Estate Investment business your parents decide it's time to retire and has asked you take over the family business.  You weren’t sure if you were ready to leave your lucrative career as a Database Administrator but after careful deliberation, you’ve agreed to take over. You realize that the business was not functioning at its most optimal level, as several staff members are still using the primitive file and cabinet method to maintain records. After thorough evaluation, you've decided to apply the knowledge you've acquired as a DBA to improve the day-to-day operations of your family-owned business. In doing so, you recruit a couple of your IT friends to assist with designing a new application.

Business Requirements

Your new application will support all the business operations; this includes maintaining records of buyers, properties acquired, contractors, sales agent, agreements, and employees.  Over the years there has been thousands of properties acquired and sold. Staff members have worked with a number of contractors consisting of Interior Designers and General Contractors.  Your business also employs five employees (accountant, lawyers, secretary, and two maintenance worker). In addition, over the years your parents have worked with several independent Real Estate Sales Agents.
Your database should contain details from previous and potential buyers including account number, name, address, contact info, occupation, salary, and credit score.
You also need to maintain Employee details employer code, employer name, employer address, employer phone number, etc...
It should also contain data for contractors such as id, name, address, phone number. In addition, you also need to include sales agents id, name, address, phone number.
You also should maintain data for contract agreements between various contractors and your company.  These agreements should include an agreement number, contractor id, contractor name, contractor address, contractor phone number, and a description of the agreement.
A contractor can enter into several agreements, but each agreement can only be associated with one contractor. 
Lastly, the database schema should contain all the properties acquired and sold, each property should have a parcel number, address, specification such as the number of rooms, square feet, purchase date, purchase amount, and market value, and architecture style description. The architectural styles include Cope Code, Colonial Contemporary, Ranch and etc… For the architecture style description, you need to store information such as the style and description of each style to provide additional characteristics for each property.
The property should also be associated with details for both the buyer and sales agent (id, name, address, phone).
You've also noted that a buyer can purchase one or more properties from you and the property can have one or more buyers.
The sale of a property can conducted by one agent, but an agent can sale many properties. 
