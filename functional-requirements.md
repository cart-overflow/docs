
# CartOverflow - Functional Requirements

## 1. Customer Account Management
- **Visitors** can create an **Account** by signing in with any supported OpenID Connect provider
- System automatically retrieves **Customer's** name and email from the provider's profile
- First-time **Visitors** are automatically registered as **Customers** when they sign in
- **Customers** receive welcome email upon first OpenID Connect sign-in
- **Customers** log in exclusively through OpenID Connect - no separate password system
- **Customers** remain logged in until they explicitly log out
- **Visitors** must be authenticated to use the service
- **Customers** can view their **Profile** information (name, email, registration date)
- **Profile** information cannot be edited within the app

## 2. Product Discovery & Browsing
- **Customers** can browse **Products**
- Each **Product** shows name, price, and primary image
- **Customers** can search for **Products** by typing keywords
- Search looks through **Product** names and descriptions  
- **Customers** can filter **Products** by category and price range
- **Product** listing updates when search or filter criteria change
- **Customers** can clear all filters to return to full catalog view
- **Customers** can view detailed **Product** information

## 3. Shopping Cart Experience
- **Customers** can **Add Products to Cart**
- **Customers** can **Update Cart Quantities**
- **Customers** can **Remove Products from Cart**
- **Cart** actions are validated against **Stock**
- **Customers** can view all **Products** of their **Cart** with names, quantities, prices, and subtotals
- **Cart** automatically calculates and displays total price and item count

## 4. Checkout
- **Customers** can proceed to **Checkout** after they have at least one **Product** in their **Cart**
- **Cart** is validated against **Stock** when **Checkout** begins
- If any **Products** have insufficient **Stock**, system asks the **Customer** to **Update Cart Quantities**
- **Stock** is temporarily **Reserved** for the confirmed quantities during **Checkout**
- **Reserved Stock** is released if **Checkout** is abandoned or fails
- **Customers** provide **Shipping Address** during **Checkout**
- **Customers** provide credit card information for **Payment** (simulated)
- **Customers** review **Order Summary** showing **Products**, quantities, prices, and total before confirming
- **Customers** can return to **Cart** to make changes before final confirmation
- **Customers** see **Order** with summary information after successful **Checkout**
- **Orders** start in **Processing Status** after successful **Checkout**
- **Cart** is cleared after successful **Checkout**
- **Stock** is permanently reduced after successful **Checkout**
- **Customers** receive **Order Confirmation Email** immediately after successful **Checkout**

## 5. Tracking
- **Customers** can view list of all their previous **Orders**
- **Customers** can click on individual **Orders** to see detailed breakdown of **Products** purchased and all related information
- Each **Order** shows current **Order Status**: **Processing**, **Shipped**, or **Delivered**
- **Customers** can see **Order** progression through different **Order Statuses**
- **Customers** receive email notifications when **Order Status** changes

## 6. Administration
- **Administrators** can view list of all **Products**
- **Administrators** can **Add New Products** via **Admin Panel**
- **Administrators** can **Update Product Information** and **Stock Quantities**
- **Administrators** receive email alerts when **Stock** falls below 5 units for specific **Product**
- **Administrators** can view list of all **Orders**
- **Administrators** can manually **Update Order Status** through **Admin Panel**
- **Order Status** progression: **Processing** → **Shipped** → **Delivered**
