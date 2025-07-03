# 04-06-API-Documentation

The Fake Store API is a free API that allows you to retrieve fictional product data. You can use it in shopping apps and websites.

You can retrieve information about products and categories. The data is returned in JSON format.

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

