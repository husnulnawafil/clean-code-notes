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

