# Basic Code Convention

## Folder name

Folder names should be in kebab case, all small case and words separated by `-`

**Don't**

```
deliveryfee

DeliveryManagement

UserImage
```

**Do**

```
delivery-fee

delivery-management

user-image
```

## File name

File names should be in kebab case, all small case and words separated by Word Separate by `-`

**Don't**

```
deliveryfee.js

DeliveryManagement.js

UserImage.js
```

**Do**

```
delivery-fee.js

delivery-management.js

user-image.js
```

## Imports Order

1. Third Party Imports (lodash, moment, rxjs).

2. Import Module.

3. Import Services.

4. Import custom lib files.

5. Import Interfaces, Constants, etc.,

Note: All above point imports need to separate by line break

**Don't**

```
import moment from 'moment';
import User from './user';
import UserModule from './user.module'
import { UserEntity } from '@lib/entity';
import { IUser } from './interface';

```

**Do**

```
import moment from 'moment';
import rxjs from 'rxjs';

import UserModule from './user.module'

import { UserEntity } from '@lib/entity';

import User from './user';
import { IUser } from './interface';
```

## Class name

Class names should be in PascalCase

**Don't**

```
userEntity

userentity

user_entity

product
```

**Do**

```
UserEntity

Product
```

## Function naming

Function names should be in camelCase

**Don't**

```
CamelCase

GetProduct
```

**Do**

```
camelCase

getProduct
```

## Function Return

Function names should use a single return statement as it can make the code more concise and easier to understand.With a single return statement, the flow of the function is clear in larger function, and the returned value is usually determined by the final execution path.

**Don't**

```
function checkExistence(type: string) {
    if(type === 'enable') return true;
    return false;
}
```

**Do**

```
function checkExistence(type: string) {
    const isEnabled = false;
    if(type === 'enable') isEnabled = true;

    return isEnabled;
}
```

## Variable naming

### Type 1

Variable names should be in camelCase

**Don't**

```
ID

FirstName

lastname

Lastname
```

**Do**

```
id

firstName

lastName
```

### Type 2

Variable names should be meaningful, even if they are lengthy or resemble a paragraph

**Don't**

```
const a = 10;
```

**Do**

```
const numberOfStudents = 10;
```

### Type 3

Variable names should generally be singular or plural based on the nature of the variable and the data it represents.

**Don't**

```
const student = ['Anya', 'Tokyo', 'Denver'];

const countries = 'India';
```

**Do**

```
const students = ['Anya', 'Tokyo', 'Denver'];
(or)
const studentList = ['Anya', 'Tokyo', 'Denver'];
```

```
const country = 'India';
```

## Comments

Comments are not always necessary if the class, interface, function and variable names already accurately represent the code

**Don't**

```
// List of User
function list() {
    return this.userTable.list();
}

//Product List
const list = ['Bike', 'Car', 'Cycle'];
```

**Do**

```
function userList() {
    return this.userTable.list();
}

(or)

function getUserList() {
    return this.userTable.list();
}
```

```
const products = ['Bike', 'Car', 'Cycle'];

(or)

const productList = ['Bike', 'Car', 'Cycle'];

```

## Todo comments

Todo comments will always have “todo” in Uppercase followed by a “:”, a space and then your comment which will start with a capital letter

**Don't**

```
// A sample todo comment (todo)

// todo - A sample todo comment

// todo: A sample todo comment
```

**Do**

```
// TODO: A sample todo comment
```

## If condition

### Type 1

If condition should always use strict equality operator `===`

**Don't**

```
if(numberOfStudents == 10) isEnabled = true;
```

**Do**

```
if(numberOfStudents === 10) isEnabled = true;
```

### Type 2

If condition should be in single line if its block line is single

**Don't**

```
if(numberOfStudents === 10) {
    isEnabled = true;
}
```

**Do**

```
if(numberOfStudents === 10) isEnabled = true;
```

## Boolean variable name

Boolean variable names should be meaningful, such as "isEnabled."

**Don't**

```
show = true

isenabled = true
```

**Do**

```
isShow = true

isEnabled = true
```
