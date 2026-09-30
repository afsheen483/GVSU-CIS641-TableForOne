Team name: Table for One

Team members: Afsheen Afsheen

# Introduction

Many small restaurants still take orders by phone and on paper tickets. The restaurant this project is based on, Corner Table Kitchen, receives orders in three ways: phone calls, walk in customers at the counter, and two third party delivery apps. Each channel works separately. Delivery app orders arrive on their own tablets and have to be retyped for the kitchen, and phone orders are handwritten. During busy hours this causes wrong and missed orders. The delivery apps also keep 25 to 30 percent of every order as commission, which is a large cost for a small business. Inventory is counted by hand once a week, so the kitchen sometimes runs out of popular items or throws away food that was over ordered.

The system is a web application that brings ordering, the kitchen queue, and inventory into one system. Customers will be able to view the menu, place pickup or delivery orders, and pay online or at pickup through the restaurant's own site. Staff will enter phone and counter orders into the same system, so every order appears on one kitchen display screen in the order it was received. Kitchen staff can mark orders as in progress or ready, and can mark menu items as sold out, which removes them from the online menu right away.

Behind each menu item is a simple recipe that lists the ingredients it uses. When an order is completed, the system reduces ingredient quantities automatically and alerts the manager when an item falls below a set level. The owner will also have a reporting page that shows daily and weekly sales, best selling items, and the busiest hours, so staffing and supply orders can be based on real data instead of guesses.

The goal of the project is a working system that a small restaurant could realistically use, along with the full set of analysis and design artifacts expected in this course, including a requirements definition, use case, activity, class, and sequence diagrams, and a test plan. The main users are customers, counter and kitchen staff, and the owner or manager, and each group will have its own view with only the functions it needs.

# Anticipated Technologies

* Front end: HTML, CSS, and JavaScript for the customer site, staff order entry, and kitchen display
* Back end: PHP 8 for the server side logic and a simple REST style API between the pages and the database
* Database: MySQL for menu items, orders, customers, ingredients, and stock levels
* Payments: Stripe in test mode, so no real card data is stored or handled by the system
* Development tools: XAMPP for local development, Visual Studio Code, Git and GitHub for version control
* Modeling: draw.io or Lucidchart for UML diagrams
* Project website: GitHub Pages (github.io)
* Testing: PHPUnit for unit tests and manual test cases for the user interface

# Method/Approach

I will follow an iterative, agile style approach with two week sprints. Since I am working alone, I will act as project manager, analyst, developer, and tester, and I will use the weekly meeting notes to record progress, decisions, and goals for the next week. Work will be tracked with GitHub Issues and a simple project board.

The first sprint focuses on analysis. I will refine the system request into a full requirements definition with functional and non functional requirements, then create the use case diagram, use case descriptions, and activity diagrams for the main processes such as placing an order, preparing an order, and restocking. The second sprint focuses on design: the class diagram, sequence diagrams for the key use cases, the database schema, and simple wireframes for each screen.

Implementation will then be done in order of business value. The first build will cover the menu, customer ordering, and the kitchen display, since that is the core problem the restaurant has. The next build adds staff order entry, sold out items, and payment in test mode. The last build adds inventory tracking, low stock alerts, and the sales reports. Each build will be tested before moving on, and the UML models will be updated if the design changes during development.

# Estimated Timeline

| Milestone | Target date | Description |
|---|---|---|
| Proposal and repository setup | Sept 30 | Team repository, README, and this proposal |
| Requirements definition | Oct 11 | Functional and non functional requirements, use cases |
| Functional and structural models | Oct 25 | Use case, activity, and class diagrams, database schema |
| Behavioral models and UI design | Nov 1 | Sequence diagrams and screen wireframes |
| Build 1 | Nov 15 | Menu, customer ordering, kitchen display |
| Build 2 | Nov 29 | Staff order entry, sold out items, test payments |
| Build 3 and testing | Dec 6 | Inventory, low stock alerts, reports, full testing |
| Final delivery | Mid December | Project website, final artifacts, presentation |

These dates are estimates and will be adjusted as the course checkpoints are announced.

# Anticipated Problems

* Working alone: All roles fall on one person, so the scope has to stay realistic. If time runs short, loyalty points and delivery tracking will be moved to a list of future enhancements rather than rushing the core features.
* Real time kitchen updates: The kitchen display needs to show new orders without staff refreshing the page. I plan to start with short interval polling and only move to a more complex approach if needed.
* Inventory accuracy: Automatic stock reduction depends on each menu item having a correct recipe. Wrong recipe data will lead to wrong stock levels, so the system needs an easy way for the manager to correct counts.
* Payments and security: Card payments must go through Stripe so the system never stores card numbers. Staff and manager pages will need proper login and role based access so customers cannot reach them.
* Delivery app orders: Connecting directly to third party delivery apps is outside what is realistic for this course, so those orders will be entered manually by staff in this version.
* Limited real user feedback: Without a real restaurant to test with, requirements are partly assumed. I will validate them by walking through realistic scenarios for each type of user.
