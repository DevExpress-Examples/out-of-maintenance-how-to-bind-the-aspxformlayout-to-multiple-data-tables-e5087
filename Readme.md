<!-- default file list -->
*Files to look at*:

* [Default.aspx](./CS/WebSite/Default.aspx) (VB: [Default.aspx](./VB/WebSite/Default.aspx))
<!-- default file list end -->
# How to bind the ASPxFormLayout to multiple data tables
<!-- run online -->
**[[Run Online]](https://codecentral.devexpress.com/e5087)**
<!-- run online end -->


<p><br />
This example demonstrates how to bind the ASPxFormLayout control to multiple tables by joining these tables in an SQL request.<br />


```sql
SELECT
    p.Discontinued, p.ProductID, p.ProductName, p.ReorderLevel, p.UnitsOnOrder, p.UnitsInStock, p.UnitPrice, p.QuantityPerUnit,
    c.CategoryID, c.CategoryName, c.Description,
    s.SupplierID, s.CompanyName, s.ContactName, s.ContactTitle, s.Country, s.Region, s.City, s.Address, s.Phone, s.Fax,  s.PostalCode, s.HomePage,
    od.OrderID, od.UnitPrice, od.Quantity, od.Discount
FROM
    Products AS p
    INNER JOIN Suppliers AS s ON p.SupplierID = s.SupplierID
    INNER JOIN Categories AS c ON p.CategoryID = c.CategoryID
    INNER JOIN [Order Details] AS od ON p.ProductID = od.ProductID
```

 </p>


<h3>Description</h3>

<p><br />
</p>

<br/>


