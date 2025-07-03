# 04-06-API-Documentation

## Products

### Get all products
```
fetch('https://fakestoreapi.com/products')
            .then(res=>res.json())
            .then(json=>console.log(json))
```

### Get a single product
```
fetch('https://fakestoreapi.com/products/1')
            .then(res=>res.json())
            .then(json=>console.log(json))
```

### Limit results
```
fetch('https://fakestoreapi.com/products?limit=5')
            .then(res=>res.json())
            .then(json=>console.log(json))
```

### Sort results
```
fetch('https://fakestoreapi.com/products?sort=desc')
            .then(res=>res.json())
            .then(json=>console.log(json))
```
 Default value is in ascending mode, you can use with 'desc' or 'asc' as you want.

### Get all categories
```
fetch('https://fakestoreapi.com/products/categories')
            .then(res=>res.json())
            .then(json=>console.log(json))
```

### Get products in a specific category
```
fetch('https://fakestoreapi.com/products/category/jewelery')
            .then(res=>res.json())
            .then(json=>console.log(json))
```
 You can also use limit(Number) and sort(asc|desc) as a query string to get your ideal results.

