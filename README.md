# FinalProject

This web app consists of an application to order food plates out of different restaurants in your area. 

Backend-Entities
--------------
1. User
2. Restaurants
3. Plates
4. DeliveryOrder
5. OrderQuantity
5. Allergens
6. AllergenValues
7. PrimeCategories
8. Payment Method
9. Paypal
10. CreditCard

The backend side is built around different kind of relations among entities (many to many, one to many...). This side prevents the user from modifying an order when more than 5 minuts have passed since the order was placed. As a particularity, the way the model is built needs to follow certain logic when posting in the database. For example, to create an order, it has to be created first empty, and then add the plates set and the order quantity list.

It also consumes a microservice to get the contact help info of the site in the port 8081.

Frontend
-----------------
The login page is prompted, once logged the homepage view is activated with the following menu available:
- Make an order: 
  1. First the user is asked to write a zipCode. The restaurant list available for that area appears. 
  2. Then the user has to select one, and the plates set will appear on the right, where the user has to select a quantity for each one. We can also see here the total amount for the order and the cart displaying the total items added to the foregoing order.
  3. When clicking the cart, the checkout view appears with the selected plates and its quantity. Here the user has to select a payment method available for him, that has to be previously posted in the database via its route. After this the order can be posted.
- My orders: list of orders created by the user, when clicking in one the checkout view for the order appears but the quantities can't be modified here. The modification of the order can happen via its patch route and whitin the time range formerly specified.
- Payment options: list of payment systems available for the user, its only a list
- Help: contact info provided by the microservice
- Log out: goes to the homepage


REPOSITORIES:
https://github.com/Danielpnz92/FinalProject-back
https://github.com/Danielpnz92/FinalProject-back-micro
https://github.com/Danielpnz92/FinalProject-front
