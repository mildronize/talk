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
# If Typescript compiles to Javascript doesn’t it mean that Javascript is enough?"

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

![](assets/Why-use-Typescript-prevents-us-from-passing-wrong-type-argument-to-function_.png)


TypeScript prevents you from passing the wrong type of argument to the function

---

![bg](#123)
![](#fff)

##### <!--fit--> [Marp CLI](https://github.com/marp-team/marp-cli) + [GitHub Pages](https://github.com/pages) | [Netlify](https://www.netlify.com/) | [Vercel](https://vercel.com/)

##### <!--fit--> 👉 The easiest way to host<br />your Marp deck on the web

---

![bg right 60%](https://icongr.am/octicons/mark-github.svg)

## **[GitHub Pages](https://github.com/pages)**

#### Ready to write & host your deck!

[![Use this as template h:1.5em](https://img.shields.io/badge/-Use%20this%20as%20template-brightgreen?style=for-the-badge&logo=github)](https://github.com/yhatt/marp-cli-example/generate)

---

![bg right 60%](https://icongr.am/simple/netlify.svg?colored)

## **[Netlify](https://www.netlify.com/)**

#### Ready to write & host your deck!

[![Deploy to Netlify h:1.5em](./assets/netlify-deploy-button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/yhatt/marp-cli-example)

---

![bg right 60%](https://icongr.am/simple/zeit.svg)

## **[Vercel](https://vercel.com/)**

#### Ready to write & host your deck!

[![Deploy to Vercel h:1.5em](https://vercel.com/button)](https://vercel.com/import/project?template=https://github.com/yhatt/marp-cli-example)

---

### <!--fit--> :ok_hand:

---

![bg 40% opacity blur](https://avatars1.githubusercontent.com/u/3993388?v=4)

### Created by Yuki Hattori ([@yhatt](https://github.com/yhatt))

https://github.com/yhatt/marp-cli-example

---

Ref: https://tsh.io/blog/why-use-typescript/