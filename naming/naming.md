# Section 2: Naming - Assigning Names to Variables, Functions, Classes & More

## Why Good Names Matter
Actually name of variable, function and etc. should be meaningful. It helps other who read our code code can easily understand without even dive detail into the code itself.
<br>
Example:
<br><br>
    1. `const user = new(User)`
<br><br>
    2. `database.insert(user)`
<br><br>
    3. `if (isLoggedIn) {...}`
<br><br>
Examples above can make us easily understand what each code process without ever looking at the entire code inside the function. So it helps reducing _**cognitive load**_.

<br>

## How to Name Correctly
- Variable
```mermaid
graph TB
A[Variable] --> B[Data Cointaner] -- eg. user input data, validation results, a list of products --> C[Use noun or short phrases with adjective] --> D["const userData = {...} , const isValid = bool"]
```
<br>

- Function and Method
```mermaid
graph TB
A[Function / Method] --> B[Commands or calculated value] -- eg. send data to the server, check if user is valid --> C[Use verb or short phrases with adjective] --> D["sendData() , inputIsValid()"]
```
<br>

- Class
```mermaid
graph TB
A[Class] --> B["Use classes to create 'things'"] -- eg. a user, a product, a http request body --> C[Use nouns or short phrases with nouns] --> D["class User = {...} , class RequestBody = {...}"]
```
<br>
But all the above charts just the rules, you need to choose verbs, nouns, or adjectives by your own.

<br>

## Casing Conventions and Programming Languages
Commonly there are four casing style in programming. They are:

1. `snake_case` .. eg. `is_valid` , `send_response` .. usage example in **python** as variables and functions/methods naming. 

2. `camelCase` .. eg. `isValid` , `sendResponse` .. usage example in **java or javascript** as variables and functions/methods naming.

3. `PascalCase` .. eg. `AdminRole` , `UserRepository` .. usage example in **many programming languages** as classes name.

4. `kebab-case` .. eg. `<side-drawer>` .. usage example in **html** as custom html elements.

You may see the differences between each others.

> **NOTE:** I mentioned programming language that use that casing style, but it does not mean other programming languages (that I have not mentioned) does not have those styles of casing. So explore the casing style of each by read docs and codes of the community of each programming languages. Because following the languages' conventions is also the part of writing a clean code.

<br>

## Naming Variables and Properties Theory

| Value of an Object | Value is Number or String | Value is a boolean |
|--|--|--|
| Describe the Value | Describe the Value | Answer a true/false question |
| `user` <br> `database` | `name` <br> `age` | `isActive` <br> `loggedIn` |
| Provide more details without introducing redundancy | Provide more details without introducing redundancy | Provide more details without introducing redundancy |
| `authenticatedUser` <br> `sqlDatabase` | `firstName` <br> `age` (it has been specific) | `isActiveUser` <br> `loggedIn` |

<br>

example:
| What is stored? | Bad Names | Okay Names | Good Names |
|--|--|--|--|
| A user object (name, email, age) | `u` <br> `data` <br>(not specific and "u" and "data" could contain anything) | `userData` <br> `person` <br> ("userData" is a bit redundant, and "person" is too unspecific) | `user` <br> `customer` <br> ("user" is descriptive enough, and "customer" is even more specific) |
| User input validation result (true/false) | `v` <br> `val` <br> ("v" is could be anything and "val" could stand for value instead of validation) | `correct` <br> `validatedInput` <br> (both terms do not necessarily imply a true/false value) | `isCorrect` <br> `isValid` <br> `isInputValid` <br> (those terms are descriptive and have clear value types) |

> **NOTE:** Avoid to name something not specific. 

<br>

## Naming Functions Theory
| Function performs a operation | Function computes a boolean |
|--|--|
| Describe the operation | Answer a true/false question |
| `getUser(...)` <br> `response.send()` | `isValid(...)` <br> `purchase.isPaid()` |
| Provide more detail without introducing redundancy | Provide more detail without introducing redundancy |
| `getUserByEmail(...)` <br> `response.send()` (already clear that func is for sending email) | `emailIsValid(...)` <br> `purchase.isPaid()` (already clear that func is for checking whether the purchase is already paid or not)

<br>

example:

| What does the function do? | Bad Names | Okay Names | Good Names |
|--|--|--|--|
| Save user data to database | `process(..)` <br> `handle(...)` (both are very unspecific - what is really being processed?) | `save(...)` <br> `storeData(...)` (at least we know that something is saved - but what?) | `saveUser(...)` <br> `user.store()` (The intent is very clear - especially with the method) |
| Validate the user input | `process(...)` <br> `save(...)` (unspecific "process" or even misleading "save") | `validateSave(...)` <br> `check(...)` (both names are not 100% specific) | `validate(...)` <br> `isValid(...)` (both make sense - depends on what the function does exactly) |

<br>

## Naming Classes Theory
| Describe the Object| |
|--|--|
|`User` <br> `Product` | |
|Provide more detail without introducing redundancy | |
| `Customer` <br> `Course` | |
| Avoid redundant suffixes | Classes are typically instantiate |
| `DatabaseManager` | Instantiating the 'DatabaseManager' makes no sense |

example: 
| Which object is described? | Bad Names | Okay Names | Good Names |
|--|--|--|--|
| A user | `class UEntity` <br> `class ObjA` (both are very unspecific) | `class UserObj` <br> `class AppUser` (both names have redundant information) | `class User` <br> `class Admin` <br> `class Customer` ("User" is just fine - or "Admin" and "Customer" are more specific kind of user) |
| A Database (_in code_) | `class Data` <br> `class DataStorage` (It is not clear that we are describing a database) | `class Db` <br> `class Data` (Not 100% specific) | `class Database` <br> `class SQLDatabase` ("Database" is good - while "SQLDatabase" is more specific means that it is even better)