# 04-06-API-Documentation

The Fake Store API is a free API that allows you to retrieve fictional product data. You can use it in shopping apps and websites.

You can retrieve information about products, categories, users and carts. The data is returned in JSON format.

## Products

### Get all products
```
fetch('https://fakestoreapi.com/products')
```

### Get a single product
```
fetch('https://fakestoreapi.com/products/1')
```

### Limit results
```
fetch('https://fakestoreapi.com/products?limit=5')
```

### Sort results
```
fetch('https://fakestoreapi.com/products?sort=desc')
```
Default value is in ascending mode, you can use with 'desc' or 'asc' as you want.

### Get all categories
```
fetch('https://fakestoreapi.com/products/categories')
```

### Get products in a specific category
```
fetch('https://fakestoreapi.com/products/category/jewelery')
```
You can also use limit(Number) and sort(asc|desc) as a query string to get your ideal results.

## Add new product
```
fetch('https://fakestoreapi.com/products',{
            method:"POST",
            body:JSON.stringify(
                {
                    title: 'test product',
                    price: 13.5,
                    description: 'lorem ipsum set',
                    image: 'https://i.pravatar.cc',
                    category: 'electronic'
                }
            )
        })
```          
If you send an object like the code above, it will return you an object with a new id. Remember that nothing in real will insert into the database. So if you want to access the new id you will get a 404 error.

### Update a product
```
fetch('https://fakestoreapi.com/products/7',{
            method:"PUT",
            body:JSON.stringify(
                {
                    title: 'test product',
                    price: 13.5,
                    description: 'lorem ipsum set',
                    image: 'https://i.pravatar.cc',
                    category: 'electronic'
                }
            )
        })
            
fetch('https://fakestoreapi.com/products/7',{
                method:"PATCH",
                body:JSON.stringify(
                    {
                        title: 'test product',
                        price: 13.5,
                        description: 'lorem ipsum set',
                        image: 'https://i.pravatar.cc',
                        category: 'electronic'
                    }
                )
            })
```
It will return you an object with sent id. Remember that nothing in real will update in the database.

### Delete a product
```
fetch('https://fakestoreapi.com/products/6',{
            method:"DELETE"
        })
```
           
The product will not be deleted on the database. But if you sent data successfully it will return you the fake deleted product.

## Cart

### Get all carts
```
fetch('https://fakestoreapi.com/carts')
```
 
### Get a single cart
```
fetch('https://fakestoreapi.com/carts/5')
```

### Limit results
```
fetch('https://fakestoreapi.com/carts?limit=5')
```

### Sort results
```
fetch('https://fakestoreapi.com/carts?sort=desc')
```
The default value is in ascending mode, you can use it with 'desc' or 'asc' as you want.

### Get carts in a date range
```
fetch('https://fakestoreapi.com/carts?startdate=2019-12-10&enddate;=2020-10-10')
```
If you don't add any start date it will fetch from the beginning of time and if you don't add any end date it will fetch until now. You can also use limit(Number) and sort(asc|desc) as a query string to get your ideal results.

### Get user carts
```
fetch('https://fakestoreapi.com/carts/user/2')
```
You can also use date range as query string to get your ideal results.

### Add a new product
```
fetch('https://fakestoreapi.com/carts',{
            method:"POST",
            body:JSON.stringify(
                {
                    userId:5,
                    date:2020-02-03,
                    products:[{productId:5,quantity:1},{productId:1,quantity:5}]
                }
            )
        })
```
If you send an object like the code above, it will return you an object with a new id. Remember that nothing in real will insert into the database. So if you want to access the new id you will get a 404 error.

### Update a product
```
fetch('https://fakestoreapi.com/carts/7',{
            method:"PUT",
            body:JSON.stringify(
                {
                    userId:3,
                    date:2019-12-10,
                    products:[{productId:1,quantity:3}]
                }
            )
        })

fetch('https://fakestoreapi.com/carts/7',{
                method:"PATCH",
                body:JSON.stringify(
                    {
                        userId:3,
                        date:2019-12-10,
                        products:[{productId:1,quantity:3}]
                    }
                )
            })
```
It will return you an object with sent id. Remember that nothing in real will update in the database.

### Delete a cart
```
fetch('https://fakestoreapi.com/carts/6',{
            method:"DELETE"
        })
```
The cart will not be deleted on the database. But if you sent data successfully it will return you the fake deleted cart.


## User

### Get all users
```
fetch('https://fakestoreapi.com/users')
```

### Get a single user
```
fetch('https://fakestoreapi.com/users/1')
```

### Limit results
```
fetch('https://fakestoreapi.com/users?limit=5')
```

### Sort results
```
fetch('https://fakestoreapi.com/users?sort=desc')
```
The default value is in ascending mode, you can use it with 'desc' or 'asc' as you want.

### Add a new user
```
fetch('https://fakestoreapi.com/users',{
            method:"POST",
            body:JSON.stringify(
                {
                    email:'John@gmail.com',
                    username:'johnd',
                    password:'m38rmF$',
                    name:{
                        firstname:'John',
                        lastname:'Doe'
                    },
                    address:{
                        city:'kilcoole',
                        street:'7835 new road',
                        number:3,
                        zipcode:'12926-3874',
                        geolocation:{
                            lat:'-37.3159',
                            long:'81.1496'
                        }
                    },
                    phone:'1-570-236-7033'
                }
            )
        })
```
If you send an object like the code above, it will return you an object with a new id. Remember that nothing in real will insert into the database. So if you want to access the new id you will get a 404 error.

### Update a users
```
fetch('https://fakestoreapi.com/users/7',{
            method:"PUT",
            body:JSON.stringify(
                {
                email:'John@gmail.com',
                username:'johnd',
                password:'m38rmF$',
                name:{
                    firstname:'John',
                    lastname:'Doe'
                },
                address:{
                    city:'kilcoole',
                    street:'7835 new road',
                    number:3,
                    zipcode:'12926-3874',
                    geolocation:{
                        lat:'-37.3159',
                        long:'81.1496'
                    }
                },
                phone:'1-570-236-7033'
                }
            )
        })

fetch('https://fakestoreapi.com/users/7',{
                method:"PATCH",
                body:JSON.stringify(
                    {
                        email:'John@gmail.com',
                        username:'johnd',
                        password:'m38rmF$',
                        name:{
                            firstname:'John',
                            lastname:'Doe'
                        },
                        address:{
                            city:'kilcoole',
                            street:'7835 new road',
                            number:3,
                            zipcode:'12926-3874',
                            geolocation:{
                                lat:'-37.3159',
                                long:'81.1496'
                            }
                        },
                        phone:'1-570-236-7033'
                    }
                )
            })
```
It will return you an object with sent id. Remember that nothing in real will update in the database.

### Delete a user
```
fetch('https://fakestoreapi.com/users/6',{
            method:"DELETE"
        })
```
The user will not be deleted on the database. But if you sent data successfully it will return you the fake deleted user.


## Login

### User login
```
fetch('https://fakestoreapi.com/auth/login',{
            method:'POST',
            body:JSON.stringify({
                username: "mor_2314",
                password: "83r5^_"
            })
        })
```
You can use any of the users' username and password available in users API to get token. Any other usernames return error.
