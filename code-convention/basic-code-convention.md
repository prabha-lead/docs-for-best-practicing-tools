# Basic Code Convention

## File name

File names should be in snake case. Word Separate by `-`

<span style="color:red">Don't</span>

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

<span style="color:red">Don't</span>

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

<span style="color:red">Don't</span>

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

<span style="color:red">Don't</span>

```
CamelCase

GetProduct
```

<span style="color:green">Do:</span>

```
camelCase

getProduct
```

## Variable naming

### Type 1

Variable names should be in camelCase

<span style="color:red">Don't</span>

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

<span style="color:red">Don't</span>

```
const a = 10;
```

<span style="color:green">Do:</span>

```
const numberOfStudents = 10;
```

## Todo comments

Todo comments will always have “todo” in Uppercase followed by a “:”, a space and then your comment which will start with a capital letter

<span style="color:red">Don't</span>

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

If condition should be in single line if its block line is single

<span style="color:red">Don't</span>

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

<span style="color:red">Don't</span>

```
show = true

isenabled = true
```

<span style="color:green">Do:</span>

```
isShow = true

isEnabled = true
```
