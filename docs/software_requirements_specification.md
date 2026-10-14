# Overview

This document is the Software Requirements Specification (SRS) for Table for One, an online ordering and kitchen inventory system for a small restaurant. It lists what the system must do (functional requirements) and the qualities it must have (non-functional requirements), grouped by feature. Since the team has only one member, it combines my individual requirements from Homework 3 along with additional requirements needed to cover the whole system. This document will be updated as the project moves forward.

# Functional Requirements

1. Customer Account
   1. FR1.1: The system shall allow a customer to create an account by entering a name, email address, phone number, and password.
   2. FR1.2: The system shall allow a registered customer to log in using an email address and password.
   3. FR1.3: The system shall display a list of the customer's past orders on the Order History page.
   4. FR1.4: The system shall add one loyalty point to the customer's account for every whole dollar spent on a completed order.
2. Menu and Ordering
   1. FR2.1: The system shall display menu items grouped by category, showing each item's name, description, and price.
   2. FR2.2: The system shall add a menu item to the customer's cart when the customer selects the "Add to Cart" button for that item.
   3. FR2.3: The system shall allow a customer to change the quantity of an item or remove an item from the cart before checkout.
   4. FR2.4: The system shall require the customer to choose either pickup or delivery before the order can be submitted.
   5. FR2.5: The system shall require a delivery address when the customer chooses delivery.
   6. FR2.6: The system shall show an order confirmation page with an order number after the order is submitted.
3. Payment
   1. FR3.1: The system shall allow a customer to choose either "Pay Online" or "Pay at Pickup" at checkout.
   2. FR3.2: The system shall record each order's payment status as Unpaid, Paid, or Refunded.
   3. FR3.3: The system shall allow counter staff to mark a "Pay at Pickup" order as Paid when the customer pays.
4. Staff Order Entry
   1. FR4.1: The system shall allow counter staff to enter phone and counter orders using the same menu that customers see online.
   2. FR4.2: The system shall record whether each order came from the website, the phone, or the counter.
5. Kitchen Display
   1. FR5.1: The system shall display each new order on the kitchen display screen in the order it was received.
   2. FR5.2: The system shall allow kitchen staff to change an order's status to In Progress, Ready, or Completed.
   3. FR5.3: The system shall allow kitchen staff to mark a menu item as sold out.
   4. FR5.4: The system shall hide a sold out item from the online menu until a staff member marks it as available again.
6. Inventory
   1. FR6.1: The system shall reduce the stock quantity of each ingredient used in an order when kitchen staff mark the order as Completed.
   2. FR6.2: The system shall allow the manager to update the stock quantity and minimum level of each ingredient.
   3. FR6.3: The system shall display an alert on the manager dashboard when an ingredient's stock quantity falls below its minimum level.
7. Sales Reports
   1. FR7.1: The system shall show the manager a daily and weekly sales report with total sales and number of orders.
   2. FR7.2: The system shall show the ten best selling menu items for a date range chosen by the manager.
   3. FR7.3: The system shall show the number of orders received in each hour of the day for a chosen date.

# Non-Functional Requirements

1. Performance
   1. NFR1.1: The menu page shall load within 3 seconds on a standard broadband connection.
   2. NFR1.2: A new order shall appear on the kitchen display within 10 seconds of being submitted.
   3. NFR1.3: The system shall support at least 50 customers placing orders at the same time without errors.
2. Security
   1. NFR2.1: The system shall process all card payments through a PCI DSS compliant payment provider and shall not store full card numbers in its database.
   2. NFR2.2: The system shall allow only users with the Manager role to view sales reports and change stock levels.
   3. NFR2.3: The system shall store all passwords in hashed form.
   4. NFR2.4: The system shall log out a staff or manager account after 15 minutes of inactivity.
3. Operational
   1. NFR3.1: The customer website shall work on the current versions of Chrome, Safari, Firefox, and Edge on both desktop and mobile devices.
   2. NFR3.2: The customer website shall be usable on screens as narrow as 360 pixels without horizontal scrolling.
   3. NFR3.3: The system shall back up its database once every day.
4. Usability
   1. NFR4.1: A new kitchen staff member shall be able to update an order's status after a training session of no more than 30 minutes.
5. Cultural and Political
   1. NFR5.1: The system shall display all prices in US dollars and add Michigan sales tax at checkout.
