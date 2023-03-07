---
title: "Drink King - drink order system"
date: 2023-03-06T01:00:35+08:00
draft: false
---

# **Overview**
Drink King tries to help people who need drink order inspiration or suffer from group order chaos. Our users can easily search for drink shops around and see the drink lists offered today. They can also share their order with friends, who can add their customized orders themselves, making the group ordering process easier and more accurate.

# **Project Prompt**
The handshake drink culture is a part of Taiwanese life. Based on the massive demand in the market, we have devised a platform where people can do tea shopping online and share their orders with groups. And also, the partner-customer can easily join the shared order and customize their own drinks.

# **My Role**
- Project Ideation
- User Research
- User Case
- User Flow
- Wireflow
- Sequence Diagram


# **My Tool**
- Figma
- StarUML
- HackMD

# **Main Feature**
- Sign-in and Sign-up
- Drinks shopping (Search for teashops and drinks)
- Add to Cart (Add / Edit / Delete order)
- Organize group order(Share order)
- Place order
- Review order history

# **User Flow**
![image alt](https://drive.google.com/uc?export=view&id=1sKndeFPMzHE1z8c0A8LOjgG1SHrl1huF)

---

# **User Case**
> 📌 There are two types of users
> - Main-customer: The person who places the order and can edit all the items in it.
> - Partner-customer: The person who joins the order made by the main customer. They can only add items and submit them to the main order.

## Sign up & Sign in
| Item | Content |
| --- | --- |
| Name | Sign up |
| Actor | User (main-customer and partner-customer) |
| Goal | To create a new account on the system |
| Preconditions | The user has not previously signed up for an account. |
| Postconditions | The user is signed in automatically. |
| Main Success Scenario | The user successfully creates an account and signs in automatically. |
| Alternative Scenario | The user is unable to sign up. Provide instructions to the user for troubleshooting. |

| Item | Content |
| --- | --- |
| Name | Sign in |
| Actor | User (main-customer and partner-customer) |
| Goal | To sign in to the system |
| Preconditions | The user has signed up for an account. |
| Postconditions | The user's status is signed-in. The user can view their previous records on the system, such as the items added to their cart. |
| Main Success Scenario | The user successfully signs in and accesses their account. |
| Alternative Scenario | The user is unable to sign in, causing by account issue or technical issue. Provide instructions to the user for troubleshooting. |

## Drink shopping
| Item | Content |
| --- | --- |
| Name | Search for tea shops |
| Actor | User (main-customer and partner-customer) |
| Goal | To search for tea shops based on the title or offered items |
| Preconditions | N/A |
| Postconditions | N/A |
| Main Success Scenario | The user receives search results that match the input title or offer the items the user searched for. |
| Alternative Scenario | No matched result found |
| Special Requirement | Each search result must include information about the teashop's title, description and minimum order amount. |

| Item | Content |
| --- | --- |
| Name | Browse teashop information and drink details |
| Actor | User (main-customer and partner-customer) |
| Goal | To browse teashop information and drink details |
| Preconditions | N/A |
| Postconditions | N/A |
| Main Success Scenario | The user can access the teashop information and drink details they need.  |
| Alternative Scenario | N/A |

## Add order (Add to cart)
| Item | Content |
| --- | --- |
| Name | Add an order (Add to cart) |
| Actor | User (main-customer and partner-customer) |
| Goal | To customize drinks and add them to the cart |
| Preconditions | The user must be in a signed-in status. |
| Postconditions | Newly added items are displayed on the cart page |
| Main Success Scenario | The user successfully add their customized drinks to the cart.  |
| Alternative Scenario | 1. The user is not signed in. Redirect to the sign-in page. |
| |2. The user is unable to add the drinks to the cart because they are sold out. Alert by the snack bar and disable the add button. |

## Organize group order (Share orders)
| Item | Content |
| --- | --- |
| Name | Share the order |
| Actor | Main-customer |
| Goal | To allow the main-customer to organize a group order by sharing their order with friends. |
| Preconditions | The main-customer has already added an order. |
| Postconditions | The system generates a link for order sharing and sends a notification to the assigned partner-customers |
| Main Success Scenario | The main-customer successfully shares the order by assigning partner-customers or sharing the link.  |
| Alternative Scenario | 1. The main customer is unable to share the order with the assigned customers, because the assigned account is not valid. |
| |2. The main customer is unable to share the order because it has been checked out. |

## Place order
| Item | Content |
| --- | --- |
| Name | Place order |
| Actor | Main-customer |
| Goal | To allow the main-customer to checkout the items in the cart and place an order.  |
| Preconditions | 1. The main-customer must be signed-in status |
| |2. The cart must not be empty. |
| |3. The selected teashop must be open. |
| Postconditions | Direct to the order history page, where the latest order is displayed.|
| Main Success Scenario | After the main customer checks the order details and places it. Direct to the order history page. |
| Alternative Scenario | 1. The order can't be placed because the selected teashop is closed. Display the error message. |
| |2. The order cannot be placed because the cart is empty or the total price is less than free delivery minimum. Alert by the snack bar. |
| |3. The order cannot be placed because the main customer is not signed-in. Redirect to the sign-in page. |

## View order history
| Item | Content |
| --- | --- |
| Name | View order history |
| Actor | Main-customer |
| Goal | To allow the main-customer to find their order history on this page. |
| Preconditions | The main customer-must be signed-in status. |
| Postconditions | N/A |
| Main Success Scenario | The main-customer successfully find their order history. |
| Alternative Scenario | The main-customer is not signed in. Redirect to the sign-in page. |

---

# **Data Dictionary**
## Teashop
| Field name | Data type (Length) | Primary key | Format |
| --- | --- | --- | --- |
| Teashop_id | int(4) | V | 0001~9999 |
| Teashop_title | char(10) |  | xxx |
| Teashop_tel | char(11) |  | (07)xxx-xxxx |
| Teashop_address | text(50) |  | No.xxx, xxx Rd, xxx Dist., xxxCity, xxx |
| Free_delivery_minimum  | int(4) |  | NTD |
| Teashop_Description | text |  | xxx |
| Open_hour | text |  | **Mon** hh:mm ~ hh:mm {{< line_break >}} **Tue**  hh:mm ~ hh:mm {{< line_break >}}**Wed** hh:mm ~ hh:mm {{< line_break >}} **Thu** hh:mm ~ hh:mm {{< line_break >}} **Fri** hh:mm ~ hh:mm {{< line_break >}} **Sat** hh:mm ~ hh:mm {{< line_break >}} **Sun** hh:mm ~ hh:mm |

## Order
| Field name | Data type (Length) | Primary key | Format |
| --- | --- | --- | --- |
| Order_id | char(6) | v | 000001~999999 |
| Order_date | date |  | YYYY/MM/DD |
| MainCustomer_id | int(6) |  | 000001~999999 |
| MainCustomer_name | char(10) |  | xxx |
| PartnerCustomer_id | int(6) |  | 000001~999999 |
| PartnerCustomer_name | char(10) |  | xxx |
| Customer_tel | char(10) |  | 09xx-xxx-xxx |
| Teashop_id | char(6) |  | 000001~999999 |
| Teashop_title | char(10) |  | xxxxxx |
| Drink_id | int(6) |  | 000001~999999 |
| Drink_title | char(10) |  | xxxxxx |
| Total_price | int(6) |  | NTD |

---

# **Wireflow**
![image alt](https://drive.google.com/uc?export=view&id=18tNFaQnW1od08RIyvWUOqBvOtAP6KppR)

---

# **UI Dictionary**
## UI No.3 - add to cart UI
![image alt](https://drive.google.com/uc?export=view&id=1033AkJICNynlUdb_2q1SAcRwNN6-I4hd)
1. Browse the teashop information and drinks details
2. Customize their drinks
3. Add them to cart
| Name | Type | Function | Column name in DB | Data type |
| --- | --- | --- | --- | --- |
| Teashop title | Label | Show title | Teashop_Title | Char(10) |
| Address | Label | Show address | Teashop_Address | Char(30) |
| Opening hour | Label | Show opening hour | Teashop_Hour | Char(15) |
| Phone number | Label | Show phone number | Teashop_Tel | Char(10) |
| Free delivery minimum   | Label | Show Free delivery minimum  amount | Teashop_Minimum | int(5) |
|  |  |  | | |
| Drink Title | Label | Show drink title | Drink_title | Char(10) |
| Unit Price | Label | Show unit price | Unit_price | int(4) |
| Q'ty | TextBox | Input order q'ty | Quantity | int(4) |
| Sugar | TextBox | Input sugar scale | Sugar | Char(4) |
| Ice | TextBox | Input ice scale | Ice | Char(4) |
| Size | Button | Choose drink size | Size | Char(4) |
| Add | Button | Add drinks to cart |  |  |

---

# **Sequence Diagram**
![image alt](https://drive.google.com/uc?export=view&id=1S5pRbkgNsRk7x0nP_hEqqqLdllGrXT82)
