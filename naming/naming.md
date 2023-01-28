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

