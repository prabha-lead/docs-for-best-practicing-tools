# Basic Code Convention

## Folder name

Folder names should be in snake case, all small case and words separated by `-`

<span style="color:red">Don't:</span>

```
deliveryfee

DeliveryManagement

UserImage
```

<span style="color:green">Do:</span>

```
delivery-fee

delivery-management

user-image
```

## File name

File names should be in snake case, all small case and words separated by Word Separate by `-`

<span style="color:red">Don't:</span>

```
deliveryfee.js

DeliveryManagement.js

UserImage.js
```

<span style="color:green">Do:</span>

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

<span style="color:red">Don't:</span>

```
import moment from 'moment';
import User from './user';
import UserModule from './user.module'
import { UserEntity } from '@lib/entity';
import { IUser } from './interface';

```

<span style="color:green">Do:</span>

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

<span style="color:red">Don't:</span>

```
userEntity

userentity

user_entity

product
```

<span style="color:green">Do:</span>

```
UserEntity

Product
```

## Function naming

Function names should be in camelCase

<span style="color:red">Don't:</span>

```
CamelCase

GetProduct
```

<span style="color:green">Do:</span>

```
camelCase

getProduct
```

## Function Return

Function names should use a single return statement as it can make the code more concise and easier to understand.With a single return statement, the flow of the function is clear in larger function, and the returned value is usually determined by the final execution path.

<span style="color:red">Don't:</span>

```
function checkExistence(type: string) {
    if(type === 'enable') return true;
    return false;
}
```

<span style="color:green">Do:</span>

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

<span style="color:red">Don't:</span>

```
ID

FirstName

lastname

Lastname
```

<span style="color:green">Do:</span>

```
id

firstName

lastName
```

### Type 2

Variable names should be meaningful, even if they are lengthy or resemble a paragraph

<span style="color:red">Don't:</span>

```
const a = 10;
```

<span style="color:green">Do:</span>

```
const numberOfStudents = 10;
```

### Type 3

Variable names should generally be singular or plural based on the nature of the variable and the data it represents.

<span style="color:red">Don't:</span>

```
const student = ['Anya', 'Tokyo', 'Denver'];

const countries = 'India';
```

<span style="color:green">Do:</span>

```
const students = ['Anya', 'Tokyo', 'Denver'];
(or)
const studentList = ['Anya', 'Tokyo', 'Denver'];

const country = 'India';
```

## Comments

Comments are not always necessary if the file name, function names, and variable names already accurately represent the code

<span style="color:red">Don't:</span>

```
// List of User
function list() {
    return this.userTable.list();
}

//Product List
const list = ['Bike', 'Car', 'Cycle'];
```

<span style="color:green">Do:</span>

```
function userList() {
    return this.userTable.list();
}

(or)

function getUserList() {
    return this.userTable.list();
}

const products = ['Bike', 'Car', 'Cycle'];

(or)

const productList = ['Bike', 'Car', 'Cycle'];

```

## Todo comments

Todo comments will always have “todo” in Uppercase followed by a “:”, a space and then your comment which will start with a capital letter

<span style="color:red">Don't:</span>

```
// A sample todo comment (todo)

// todo - A sample todo comment

// todo: A sample todo comment
```

<span style="color:green">Do:</span>

```
// TODO: A sample todo comment
```

## If condition

### Type 1

If condition should always use strict equality operator `===`

<span style="color:red">Don't:</span>

```
if(numberOfStudents == 10) isEnabled = true;
```

<span style="color:green">Do:</span>

```
if(numberOfStudents === 10) isEnabled = true;
```

### Type 2

If condition should be in single line if its block line is single

<span style="color:red">Don't:</span>

```
if(numberOfStudents === 10) {
    isEnabled = true;
}
```

<span style="color:green">Do:</span>

```
if(numberOfStudents === 10) isEnabled = true;
```

## Boolean variable name

Boolean variable names should be meaningful, such as "isEnabled."

<span style="color:red">Don't:</span>

```
show = true

isenabled = true
```

<span style="color:green">Do:</span>

```
isShow = true

isEnabled = true
```
