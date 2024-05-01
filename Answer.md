# MongoDB Task

1. Find all the information about each products
    
   ```mongodb 
       db.products.find({})
   ``` 
   ![alt text](<MongoDB Task 1,(1).png>)
   ![alt text](<MongoDB Task 1,(2).png>)
   ![alt text](<MongoDB Task 1,(3).png>)
   ![alt text](<MongoDB Task 1,(4).png>)
   ![alt text](<MongoDB Task 1,(5).png>)
   ![alt text](<MongoDB Task 1,(6).png>)
   ![alt text](<MongoDB Task 1,(7).png>)

2. Find the product price which are between 400 to 800
    
   ```mongodb 
       db.products.find({product_price: {$gte: 400, $lte: 800}})
   ``` 

   ![alt text](<MongoDB Task 2,(1).png>)
   ![alt text](<MongoDB Task 2,(2).png>)

3. Find the product price which are not between 400 to 600   
    
   ```mongodb 
       db.products.find({product_price:{$not: {$gte: 400, $lte: 800}}})
   ```  
   ![alt text](<MongoDB Task 3,(1).png>)
   ![alt text](<MongoDB Task 3,(2).png>)
   ![alt text](<MongoDB Task 3,(3).png>)
   ![alt text](<MongoDB Task 3,(4).png>)
   ![alt text](<MongoDB Task 3,(5).png>)
   ![alt text](<MongoDB Task 3,(6).png>)
   ![alt text](<MongoDB Task 3,(7).png>)
   ![alt text](<MongoDB Task 3,(8).png>)
   ![alt text](<MongoDB Task 3,(9).png>)
   ![alt text](<MongoDB Task 3,(10).png>)
   ![alt text](<MongoDB Task 3,(11).png>)

4. List the four product which are greater than 500 in price    
   
   ```mongodb 
       db.products.find({product_price: {$gte: 500}}).limit(4)
   ``` 
   ![alt text](<MongoDB Task 4,(1).png>)
   ![alt text](<MongoDB Task 4,(2).png>)

5. Find the product name and product material of each products 
   
   ```mongodb 
       db.products.find({},{product_name: 1,product_material: 1})
   ``` 
   ![alt text](<MongoDB Task 5,(1).png>)   
   ![alt text](<MongoDB Task 5,(2).png>) 
   ![alt text](<MongoDB Task 5,(3).png>) 
   ![alt text](<MongoDB Task 5,(4).png>)
   ![alt text](<MongoDB Task 5,(5).png>)  

6. Find the product with a row id of 10
   
   ```mongodb 
       db.products.find({id:"10"})
   ``` 
   ![alt text](<MongoDB Task 6,(1).png>)   

7. Find only the product name and product material   
   
   ```mongodb 
   db.products.find({},{product_name: 1, product_material: 1,_id: 0})
   ```
   ![alt text](<MongoDB Task 7,(1).png>) 
   ![alt text](<MongoDB Task 7,(2).png>) 

8. Find all products which contain the value of soft in product material 
   
   ```mongodb 
   db.products.find({ product_material: "Soft"})
   ```
    ![alt text](<MongoDB Task 8,(1).png>) 
    ![alt text](<MongoDB Task 8,(2).png>)   

9. Find products which contain product color indigo  and product price 492.00
    
     ```mongodb 
     db.products.find({ product_color:"indigo",
     product_price: 492.00
     })
   ``` 
     > There is no data matching the specified condition.
     
    ![alt text](<MongoDB Task 9,(1).png>)

10. Delete the products which product price value are 28
   
    ```mongodb 
    db.products.deleteOne({ product_price: 28 })
    ```
     
    ![alt text](<MongoDB Task 10,(1).png>)    