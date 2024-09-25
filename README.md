# MongoDB_Queries01-Guvi

### 1.Find all the information about each products:
```py
db.products.find()
```
### 2.Find the product price which are between 400 to 800:
```py
db.products.find({$and:[{product_price:{$lt:800}},{product_price:{$gt:400}}]})
```
or
```py
db.products.find(
  { 
    product_price: { $gt: 400, $lt: 800 } 
  }, 
  { product_price: 1, _id: 0 }
)
```
### 3.Find the product price which are not between 400 to 600:
```py
db.products.find({product_price:{$not:{$gt:400,$lt:600}}})
```
### 4.List the four product which are greater than 500 in price:
```py
db.products.find({product_price:{$gt:500}})
```
### 5.Find the product name and product material of each products:
```py
db.products.find({},{product_name:1,product_material:1,_id:0})
```
### 6.Find the product with a row id of 10:
```py
db.products.find(
  { id: "10" }
)
```
### 7.Find only the product name and product material:
```py
db.products.find({},{product_name:1,product_material:1,_id:0})
```
### 8.Find all products which contain the value of soft in product material:
```py
db.products.find(
  { product_material: "Soft" }
)
```
### 9.Find products which contain product color indigo  and product price 492.00:
```py
db.products.find(
  { 
    product_color: "indigo", 
    product_price: 492.00 
  }
)
```
### Delete the products which product price value are 28:
```
db.products.deleteMany({product_price:28})
```
# Task time extension proof:
### ![image](https://github.com/ShakthiSundar-K/Guvi_D5_Task/assets/128116143/5318043f-5150-4178-bb8d-39bf235a2149)

