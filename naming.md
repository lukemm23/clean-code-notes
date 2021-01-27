# Naming Conventions

### why names matter

1. names should be meaningful to its context

### example 1

    // bad code
    const us = new MainEntity();
    us.process();
    if(login){

    }

    // good code
    const user = new User();
    user.save();
    if(isLoggedIn){

    }

### how to name things correctly

- variables & constants - use nouns and short phrases with adjectives, how best describes what is inside. ie. userData
- functions & methods - use verbs and short phrases with adjectives, how best describes what it does. ie. sendUserData
- classes - use nouns or short phrases with nouns, how best describes what is encapsulated inside. ie. User

### casing conventions: ( snake_case, camelCase, PascalCase, kebab-case )

javascript, java

- variables & constants - camelCase
- functions & methods - camelCase
- classes - PascalCase
- event emitter/fetch keys - SNAKE_CASE

python

- variables & constants - snake_case
- functions & methods - snake_case
- classes - PascalCase

html

- custom elements - kebab-case

### naming variables, contants, properties

- value is an object - describe the value, or provide more details without redundancy ie. user database, authenticatedUser, sqlDatabase
- value is a number or string - describe the value, or provide more details without redundancy ie. name or age, firstName
- value is a boolean - answer a true/false question, or provide more details without redundancy ie. isActive, loggedIn, isActiveUser

### naming functions and methods

- function performs an operation - describe the operation, or provide more details without redundancy ie. getUser(), response.send(), getUserByEmail()
- function computes a boolean - answer a true/false question, or provide more details without redundancy ie. isValid(), purchase.isPaid(), emailIsValid()

### naming classes

- describe the object, or provide more details without redundancy ie. User Product, Customer Course

### exceptions

    class Database {

      private client: any;

      get connectedClient(){
        if(!this.client){
          throw new Error('Database not connected!');
        }
        return this.client;
      }

      connect(){
        // estabilishing connection...
        this.client = {};
      }

    }

- get connectedClient() is a getter method, yet it sounds more like a property name, this is an exception yet an acceptable naming method.

### common error and pitfalls

    // bad name (redundancy)
    userWithNameAndAge = User('luke', 34)
    // name is too long with redundant information.

    // good name
    user = User('luke', 34), newUser = User('luke', 34), loggedInUser = User('luke', 34)
    // avoids redundancy and gives more context of what the data.

    // bad name (slang)
    product.diePlease()
    user.facepalm()
    message(n)
    ymdt = '20210121cet'
    userList = {u1:..., u2:...}
    allAccounts = accounts.filter()

    // good name
    product.remove()
    user.sendErrorMessage()
    message(newUser)
    dateWithTimezone = '20210121cet'
    userMap = {u1:..., u2:...}
    filteredAccounts = accounts.filter()
