

select p.Name, SUM(od.Quality) as NumberOfSellingProducts from Product p 
INNER JOIN Order_Detail od ON p.Id = od.ProductId 
INNER JOIN [Order] o ON o.Id = od.OrderId 
where o.Date < DATEADD(mm,DATEDIFF(mm,0,GETDATE()),0)
GROUP BY p.Name