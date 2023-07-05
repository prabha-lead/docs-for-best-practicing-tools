# API Convention

## Route naming

### Type 1

The API route path should be in the plural form and should follow the REST pattern for route naming wherever possible. It should be in snake case

**Don't**

```
GET /super-market

POST /superMarket

POST /super-market
```

**Do:**

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

   **Don't**

   ```
   GET /super-markets/products?id=1

   GET /products/super-markets/1

   GET /super-markets/1/products (/super-markets/:super_market_id/products)
   ```

   **Do:**

   ```
   GET /super-markets/1/products (/super-markets/:id/products)
   // Set param as "id" because it is after supermarket that means it is Supermarket ID
   ```

2. Avoid verbosity in API route naming. For example, when using the POST method to save data, there is no need to explicitly include "save" in the route.

   **Don't**

   ```
   POST /save/products

   POST /products/save
   ```

   **Do:**

   ```
   POST /products
   ```

## Methods

### List

The List API should always use the GET method.

**Don't**

```
POST /super-markets

PUT /super-markets
```

**Do:**

```
GET /super-markets

GET /super-markets/1 (/super-markets/:id)
```

### Add

The Add API should always use the POST method.

**Don't**

```
PUT /super-markets

GET /super-markets
```

**Do:**

```
POST /super-markets
```

### Edit

The Edit API should always use the PUT method.

**Don't**

```
POST /super-markets

GET /super-markets
```

**Do:**

```
PUT /super-markets/1 (/super-markets/:id)
```

### Delete

The Delete API should always use the DELETE method.

**Don't**

```
POST /super-markets

PUT /super-markets/1 (/super-markets/:id)
```

**Do:**

```
DELETE /super-markets/1 (/super-markets/:id)
```

## Controller naming

Controller functions should not contain any logic, instead, write all the logic inside services and load those into controller

**Don't**

```
async signUp(@Body() signupDto: SignupDto) {
    const userData = await this.userData.get();
    if(!userData || userData.is_deleted) {
        throw new Error('User not available');
    }

    return userData;
}
```

**Do:**

```
async signUp(@Body() signupDto: SignupDto) {
    return this.userService.singup(signupDto);
}
```
