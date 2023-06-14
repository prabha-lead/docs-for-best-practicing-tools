# API Convention

## Route naming

### Type 1

The API route path should be in the plural form and should follow the REST pattern for route naming wherever possible. It should be in snake case

<span style="color:red">Don't</span>

```
GET /super-market

POST /superMarket

POST /super-market
```

<span style="color:green">Do:</span>

```
GET /super-markets

GET /super-markets/1 (/super-markets/:id)

POST /super-markets

PUT /super-markets/1 (/super-markets/:id)

DELETE /super-markets/1 (/super-markets/:id)
```

### Type 2

The API route path should be in the plural form and be descriptive of the functionality.

1. List products based on supermarket

   <span style="color:red">Don't</span>

   ```
   GET /super-markets/products?id=1

   GET /products/super-markets/1

   GET /super-markets/1/products (/super-markets/:super_market_id/products)
   ```

   <span style="color:green">Do:</span>

   ```
   GET /super-markets/1/products (/super-markets/:id/products)
   // Set param as "id" because it is after supermarket that means it is Supermarket ID
   ```

2. Avoid verbosity in API route naming. For example, when using the POST method to save data, there is no need to explicitly include "save" in the route.

   <span style="color:red">Don't</span>

   ```
   POST /save/products

   POST /products/save
   ```

   <span style="color:green">Do:</span>

   ```
   POST /products
   ```

## Methods

### List

The List API should always use the GET method.

<span style="color:red">Don't</span>

```
POST /super-markets

PUT /super-markets
```

<span style="color:green">Do:</span>

```
GET /super-markets

GET /super-markets/1 (/super-markets/:id)
```

### Add

The Add API should always use the POST method.

<span style="color:red">Don't</span>

```
PUT /super-markets

GET /super-markets
```

<span style="color:green">Do:</span>

```
POST /super-markets
```

### Edit

The Edit API should always use the PUT method.

<span style="color:red">Don't</span>

```
POST /super-markets

GET /super-markets
```

<span style="color:green">Do:</span>

```
PUT /super-markets/1 (/super-markets/:id)
```

### Delete

The Delete API should always use the DELETE method.

<span style="color:red">Don't</span>

```
POST /super-markets

PUT /super-markets/1 (/super-markets/:id)
```

<span style="color:green">Do:</span>

```
DELETE /super-markets/1 (/super-markets/:id)
```

## Controller naming

Controller functions should not contain any logic, instead, write all the logic inside services and load those into controller

<span style="color:red">Don't</span>

```
async signUp(@Body() signupDto: SignupDto) {
    const userData = await this.userData.get();
    if(!userData || userData.is_deleted) {
        throw new Error('User not available');
    }

    return userData;
}
```

<span style="color:green">Do:</span>

```
async signUp(@Body() signupDto: SignupDto) {
    return this.userService.singup(signupDto);
}
```
