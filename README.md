# online_shopping
# implementation:
We implemented an online shopping application using EJBs with java ee and microservices and payara (or glassfish) server  and frontend angular .
#Functional Requirements:
Since the shopping application will need products to be added by their selling companies, and will need shipping 
companies for delivering the products, some administrative activities need to be supported.
- Admins in the system should have the following abilities
	1. Creation of product selling companies representative accounts.
		a. Given a range of company unique names
		b. Password for each company is auto generated
	2. Creation of Shipping companies
		a. Companies should have a geographic coverage including specific regions (i.e., a 			customer cannot request shipping from a company that doesn’t cover his geographic 			location)
	3. Listing of customer accounts
	4. Listing of shipping companies
	5. Listing of selling companies representative accounts
#As a selling company representative, you should be able to:
	1. Login into the system using the generated credentials as sent by the admin
	2. View products that are currently offered for sale.
	3. View previously sold products, including information about the customers who bought each 	product and the shipping company.
	4. Add new products.
#As a shipping company, it should be able to process shipping requests as long as the customer who purchased that order  falls within its supported geographic region(s). Customers should be notified, once the shipping request is processed.
#As a customer, you should be able to
	1. Register as a new customer through the system.
	2. Login into the system using the credentials used during registration.
	3. View current and past purchase orders.
	4. Make new purchase orders. Orders should be handled in a special way to avoid situations of 	server failure
	5. Both orders processing and their shipping should be confirmed back to customers
