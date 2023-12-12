# Database_CW1

Database Structure

Offices
  Table storing information about different offices.
Columns:
  PhoneNumber
  City
  Territory
  PostalCode
  OfficeCode (Primary Key)
  AddressLine1
  AddressLine2
  County
  Country
  
Employee
  Table storing employee details.
Columns:
  EmployeeNumber (Primary Key)
  FirstName
  LastName
  Extension
  JobTitle
  OfficeCode (Foreign Key)
  EmailAddress
  
RepresensitiveEmployee
  Table storing information about representative employees.
Columns:
  FirstName
  LastName
  RepresensitiveEmployeeNumber (Primary Key)
  Extension
  OfficeCode (Foreign Key)
  JobTitle
  EmailAddress
  
Customers
  Table storing customer details.
Columns:
  Country
  SalesAmount
  RepresensitiveEmployeeNumber (Foreign Key)
  AddressLine1
  AddressLine2
  FirstName
  LastName
  PhoneNumber
  CustomerNumber (Primary Key)
  City
  County
  PostalCode
  CreditLimitNumber
  
PaymentInformation
  Table storing payment details.
Columns:
  CustomerNumber (Foreign Key)
  ChequeNumber
  PaymentDate
  AmountPaid
  
PrescriptionOrders
  Table storing prescription order details.
Columns:
  OrderNumber (Primary Key)
  OrderDate
  RequiredDate
  ShippedDate
  OrderStatus
  Comments
  PharmaceuticalCustomerNumber (Foreign Key)
  
ProductLine
  Table storing information about product lines.
Columns:
  ProductLineID (Primary Key)
  ProductLineText
  Description
  Website
  ProductImage
  
Drugs
  Table storing information about drugs.
Columns:
  ProductCode (Primary Key)
  BuyingPrice
  ProductName
  ProductLine (Foreign Key)
  ScaleWeight
  Vendor
  Description
  Quantity
  MSRP
  
OrderInformation
  Table storing order details.
Columns:
  OrderNumber (Foreign Key)
  ProductCode (Foreign Key)
  QuantityOrdered
  Price
  LineNumber

  
Data Insertion

Sample data is inserted into each table to demonstrate the structure.
The data includes information about offices, employees, representative employees, customers, payment information, prescription orders, product lines, drugs, and order information.
Views

Customer_Order_Restricted_Info
  View combining customer, prescription order, and order information.
Columns:
  CustomerNumber
  FullName
  FullAddress
  OrderStatus
  QuantityOrdered
  CreditLimitNumber
  ShippedDate

Queries

A query is provided to select information from the "Customer_Order_Restricted_Info" view.
The query filters results based on a credit limit greater than 1000 and a shipped date before January 1, 2010.
