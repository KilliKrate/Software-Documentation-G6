# Coding Standards

## Lezioni alla pari
January dd, 2020

## Team Members
Ovidiu Andrioaia  
David Cirdan  
Luciano Mateias  
Zhiyang Xia


## Document Control
**Change History**

| Revision | Change Date | Description of changes |
| -------- | ----------- | ---------------------- |
| V1.0     | mm/dd/2020  | Initial release        |

**Document storage**

This document is stored in the project's GIT repository at:
https://github.com/KilliKrate/Software-Documentation-G6/blob/master/docs/Coding%20Standards.md
 
**Document Owner**

Group 6 is responsible for developing and maintaining this document.

## Table of contents
> [Introduction](#introduction)
>
> [Enforcing the Standards](#enforcing-the-standards)
>> [Code Quality Tools](#code-quality-tools)
>>
>> [Code Reviews](#code-reviews)
>>
> [Whitespaces](#whitespaces)
>> [Indentation](#indentation)
>>
>> [Spacing](#spacing)
>
> [Semicolons](#semicolons)
>
> [Naming Conventions](#naming-conventions)
>
> [Comments](#comments)

## Introduction
The "Lezioni alla Pari" coding standards aim to illustrate the way forward for implementing features and changes to the Javascript codebase. Every new piece of code committed the Github repository must strictly adhere to the following rules, since all the code in this code-base should look like a single person typed it, no matter the size of the team. These rules must be followed if you also are interested in collaborating with the team, by implementing changes and features to further develop the project.

This document guarantees a basic level of quality for all the code base, which should be, in order of importance:
- Reliable
- Maintainable
- Efficient

Efficiency comes last, as the most important characteristic is for the code to be easily readable, understandable, and modifiable by all members participating to the project.

[Back to Top](#table-of-contents)

## Enforcing the standards

### Code quality tools

In order to guarantee that the coding standards are respected, we require developers to use the following tools:

- ESLint plugin for VS Code OR ESLint Node Module
- Beautify plugin for VS Code OR js-beautify Node Module

### Code reviews

After the rules have been agreed upon, issues not covered by the use of the aforementioned tools can be resolved through various tecniques of code review. We will list the two main methods used by our team in order to guarantee code standard compliance:

- Peer review  
Another team member reviews the code to ensure that the code follows the standards and meets the requirements. The code review will be conducted in pairs and in our case, always by the same pair, because of the team size: the two back-end devs will judge each other, and the front-end devs will do the same

- Architect review  
The architect of the team must review the core modules of the project to ensure they adhere to the architecture and design specifications, so that the code and algorithm therein strictly follow them.

[Back to Top](#table-of-contents)

## Whitespaces

### Indentation

All code MUST indent using two (2) space charachters, the code MUST NOT indent using tab charachters or trailing whitespaces. This can be reinforced by using an IDE with appropriate indentation settings. Alternatively, ESLint will throw an error if use of whitespaces is not consistent.

```javascript
// bad

if ( condition ) {
    doSomething();
} 

// good

if ( condition ) {
  doSomething();
} 
```

### Spacing

Lines SHOULD generally be no longer than 80 charachters, and MUST NOT not exceed 100. The only exceptions are in the case of long URLs or Regex literals.

IIf, else, for, while and try structures MUST always use braces, even in cases where they are not required, for the sake of readability. Conditions MUST be separated by the parentheses by a space.

```javascript
// bad

if(condition) doSomething();

while(condition) iterating++;

for(var i=0;i<100;i++) someIterativeFn();

// good

if ( condition ) {
  doSomething();
}

while ( condition ) {
  iterating++;
}

for ( var i = 0; i < 100; i++ ) {
  someIterativeFn();
}
```

[Back to Top](#table-of-contents)

## Semicolons

Although Javascript allows for optional semi-colons, all code in the "Lezioni alla Pari" repository must be followed by semi-colons. Therefore, all statements (except for, function, if, switch, try, while and possibly other control structures) must be followed by a semi-colon. This is in order to avoid errors in the code, where ASI fails to fill them in correctly.

```javascript

// bad - raises exception
const luke = {}
const leia = {}
[luke, leia].forEach((jedi) => jedi.father = 'vader')

// good
const luke = {};
const leia = {};
[luke, leia].forEach((jedi) => {
  jedi.father = 'vader';
});

```

[Back to Top](#table-of-contents)

## Naming Conventions

All variables and functions MUST use camelCase, with the exception of classes and constructors. The first letter of the word MUST be lowercase, while all the first letters of subsequent words MUST be uppercased. There MUST NOT be underscores between the words, as that would be snake_case.

```javascript
// bad

function q(s) {
  return document.querySelectorAll(s);
}
var i,a=[],els=q("#foo");
for(i=0;i<els.length;i++){a.push(els[i]);}

// good

function query( selector ) {
  return document.querySelectorAll( selector );
}

var idx = 0,
  elements = [],
  matches = query("#foo"),
  length = matches.length;

for ( ; idx < length; idx++ ) {
  elements.push( matches[ idx ] );
}
```

As mentioned above, there is an exception in the case of classes and constructors. The programmer, in this situation, shall use PascalCase.

```javascript
// bad
function user(options) {
  this.name = options.name;
}

const bad = new user({
  name: 'nope',
});

// good
class User {
  constructor(options) {
    this.name = options.name;
  }
}

const good = new User({
  name: 'yup',
});
```

[Back to Top](#table-of-contents)

## Comments

Single line and multiline comments are not only allowed, but recommended. The team will adopt the standards of [JSDoc 3](https://jsdoc.app/) for the proper documentation of code. Following those rules, all files, classes and functions MUST be documented. For more in-depth perspectives on code documentation, you should head over to the official [JSDoc Documentation](https://jsdoc.app/)

One should note that comments not adherent to the JSDoc standard are recommended where files, functions, classes are not concerned. In particular, when one is explaining the logic surrounding an algorithm, one should always write some comments so that who tries to comprehend a particularly complex piece of logic can understand it even without reading the  directly.

Generally speaking, all single line comments should use ```//```, placed on a newline above the subject of the comment. An empty line should be inserted before the comment unless it's on the first line of a block.

```javascript
// bad
const active = true;  // is current tab

// good
// is current tab
const active = true;

// bad
function getType() {
  console.log('fetching type...');
  // set the default type to 'no type'
  const type = this.type || 'no type';

  return type;
}

// good
function getType() {
  console.log('fetching type...');

  // set the default type to 'no type'
  const type = this.type || 'no type';

  return type;
}
```

[Back to Top](#table-of-contents)

## Variables

## Arrays

## Strings

### Quotes

### Concatenation

## Operators

## Control Structures

## Functions

## Objects

## Classes

### Constructors

## Events


