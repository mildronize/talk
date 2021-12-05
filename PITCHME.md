---
marp: true
title: Marp CLI example
description: Hosting Marp slide deck on the web
theme: uncover
paginate: true
_paginate: false
---

![bg](./assets/gradient.jpg)

# <!--fit--> No Type No Life (TypeScript)

Thada Wangthammang



---
# Who Am I?
```
I am
 __  __ _ _     _                 _
|  \/  (_) | __| |_ __ ___  _ __ (_)_______
| |\/| | | |/ _` | '__/ _ \| '_ \| |_  / _ \
| |  | | | | (_| | | | (_) | | | | |/ /  __/
|_|  |_|_|_|\__,_|_|  \___/|_| |_|_/___\___|

Thada Wangthammang
My Blog site | https://thadaw.com             |
GitHub       | https://github.com/mildronize  |
Facebook     | http://fb.me/mildronize        |
Twitter      | https://twitter.com/mildronize |
E-Mail       | thada.wth@gmail.com            |
```

<style scoped>a { color: #eee; }</style>

<!-- This is presenter note. You can write down notes through HTML comment. -->

---

![Marp bg 60%](https://raw.githubusercontent.com/marp-team/marp/master/marp.png)

---

# What is TypeScript?

- Typescript is an open-source programming language created by Microsoft. 
- a superset of Javascript which adds static typing to the language. 
- It is worth mentioning that in the end Typescript compiles to Javascript, so the final code can run on any environment which supports JS. 
- It can be both client-side (web browser) or server-side (Node.js).

---


# "Why do I need static typing? 
#### If Typescript compiles to Javascript doesn’t it mean that Javascript is enough?"

---

![](assets/why-use-typescript-pirate-meme_.png)

---

## TypeScript may save your project from failure 

---

```js
function getSalaryWithBonus(salary, bonus){
    return salary + bonus;
}
```

Really complicated financial system function

---

```js
const salary = getSalaryWithBonus(8000, '0');
// Result is 80000 
```

The result is ‘80000’ as a string instead of 8000 as number

---
## Look at Type

```ts
function getSalaryWithBonus(salary: number, bonus: number){
    return salary + bonus;
}
```

In Typescript, you can explicitly define function parameters types

---

![width:1100px](assets/Why-use-Typescript-prevents-us-from-passing-wrong-type-argument-to-function_.png)

<!-- TypeScript prevents you from passing the wrong type of argument to the function -->

---

![](assets/why-use-typescript-typescript-meme_.png)

---

## Typescript documents itself

```js
function renderItems(items){
    // here function does something with items
}
```

---

### If you want to know what “items” actually are in JavaScript, you have a few options:

- read the documentation (if one exist),
- add `console.log(items)` in the definition of this function, run the application and check the “items” argument in the console,
- try to find out where the function is used and from there track down what data is put into it,
- ask your colleagues if someone has been recently working on it,

---

```ts
type Item = {
    id: number;
    title: string;
    description: string;
}

function renderItems(items: Item[]){
    // here function does something with items
}
```

Better?

---

# Great for Code Editor Support

- Mouse hover support 
- Code auto-completion
- Real-time type checking 
- Easier code refactor
---

# JavaScript Object Complexitiy
---

```js
const result = await fetch('https://domain.com');
for(const member of result.response.data.members){
  console.log(`My customer: `);
  for(const customer of member.business.customers){
    console.log(customer.name);
  }
}
```

How do you know that is exactly `result` structure?

---

```ts
interface ICustomer{
  name: string;
}

interface IMember {
  business: {
    customers: ICustomer[]
  }
}

interface IResult {
  response: {
    data: {
      members: IMember[]
    }
  }
}

const result = await fetch('https://domain.com') as IResult;
```

---

# TypeScript Fact

---

# 1. Can we use TypeScript without any type?

---

# Yes!

---

Ref: https://tsh.io/blog/why-use-typescript/