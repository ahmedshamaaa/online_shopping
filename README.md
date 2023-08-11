# Project Idea: "E-Commerce Marketplace with Advanced Shipping and Administrative Functionality"

# Description:
Create a comprehensive E-Commerce marketplace application that incorporates EJBs, Java EE, microservices, and Payara/GlassFish servers on the backend, and Angular for the frontend. The application will support the buying and selling of products while also integrating advanced shipping features and administrative functionalities.

# Key Features:

1. **User Authentication and Registration:**
   - Customers, selling company representatives, and administrators can register and log in with unique credentials.
   - User authentication will be securely handled to ensure data privacy and security.

2. **Admin Panel:**
   - Admins will have a dedicated panel to manage administrative activities.
   - They can create representative accounts for selling companies with auto-generated passwords.
   - Shipping companies can be created with specific geographic coverage and regions.

3. **User Management:**
   - Admins can list and manage customer accounts, selling company representative accounts, and shipping companies.

4. **Selling Company Representative:**
   - Representatives can log in using credentials provided by the admin.
   - They can view the list of products currently offered for sale.
   - Access to information about previously sold products, including customer and shipping company details.
   - Add new products to the marketplace.

5. **Shipping Company:**
   - Shipping companies can process shipping requests for customers within their supported geographic regions.
   - Customers will be notified once shipping requests are processed.
   
6. **Customer:**
   - Customers can register and log in using their credentials.
   - View current and past purchase orders.
   - Make new purchase orders with robust handling to avoid data loss in case of server failure.
   - Receive confirmation of order processing and shipping.

7. **Advanced Order Handling:**
   - Implement a resilient order handling mechanism to ensure that orders are not lost even in case of server failures.
   - Use transaction management to ensure data consistency during order processing.

8. **Geographic Region Matching:**
   - Implement a system that matches customers' locations with the supported geographic regions of shipping companies.
   - Prevent customers from selecting shipping companies that don't cover their location.

9. **Real-time Notifications:**
   - Set up real-time notifications for customers regarding order processing and shipping status.
   - Use WebSocket or other technologies to achieve this functionality.

10. **Scalability and Performance:**
    - Design the application with scalability in mind to accommodate a growing user base and product catalog.
    - Optimize the performance to provide a seamless user experience.

11. **Security and Data Privacy:**
    - Implement robust security measures to protect user data and transactions.
    - Use encryption and secure communication protocols for sensitive data.

12. **User-Friendly Frontend:**
    - Develop a responsive and intuitive Angular frontend that allows users to easily navigate through products and manage their orders.

This project will provide a comprehensive E-Commerce platform with advanced features for both buyers and sellers while incorporating administrative tools for managing the platform effectively. It will showcase your skills in backend development using EJBs and microservices, frontend development with Angular, and your ability to design complex systems that handle user interactions and data processing securely and efficiently.

#Functional Requirements:
Since the shopping application will need products to be added by their selling companies, and will need shipping 
companies for delivering the products, some administrative activities need to be supported.
1. **Admins in the system should have the following abilities**
	- Creation of product selling companies representative accounts.
		a. Given a range of company unique names
		b. Password for each company is auto generated
	- Creation of Shipping companies
		a. Companies should have a geographic coverage including specific regions (i.e., a customer cannot request 			shipping from a company that doesn’t cover his geographic location)
	- Listing of customer accounts
	- Listing of shipping companies
	- Listing of selling companies representative accounts
2. **As a selling company representative, you should be able to**
	- Login into the system using the generated credentials as sent by the admin
	- View products that are currently offered for sale.
	- View previously sold products, including information about the customers who bought each product and the shipping 		company.
	- Add new products.

3. **As a shipping company, it should be able to process shipping requests as long as the customer who purchased that order  falls within its supported geographic region(s). Customers should be notified, once the shipping request is processed.**

1. **As a customer, you should be able to**
	- Register as a new customer through the system.
	- Login into the system using the credentials used during registration.
	- View current and past purchase orders.
	- Make new purchase orders. Orders should be handled in a special way to avoid situations of 	server failure
	- Both orders processing and their shipping should be confirmed back to customers

# implementation:
**We implemented an online shopping application using EJBs with java ee and microservices and payara (or glassfish) server  and frontend angular and  we used these 4 different bean types to fulfill the above functional requirements.**
- Stateless
- Stateful
- Singleton
- Message Driven.
