-- Question 1 🧑‍💼
-- Retrieve employee details using INNER JOIN with offices on officeCode
SELECT 
    e.firstName,
    e.lastName,
    e.email,
    e.officeCode
FROM 
    employees e
INNER JOIN 
    offices o ON e.officeCode = o.officeCode;

-- Question 2 🛍️
-- Get product details using LEFT JOIN with productlines on productLine
SELECT 
    p.productName,
    p.productVendor,
    p.productLine
FROM 
    products p
LEFT JOIN 
    productlines pl ON p.productLine = pl.productLine;

-- Question 3 📦
-- Retrieve the first 10 orders using RIGHT JOIN with customers on customerNumber
SELECT 
    o.orderDate,
    o.shippedDate,
    o.status,
    o.customerNumber
FROM 
    customers c
RIGHT JOIN 
    orders o ON c.customerNumber = o.customerNumber
ORDER BY 
    o.orderDate
LIMIT 10;
