---
layout: post
title:  "Utilizando Chamadas SSIS Assincronas"
date:   2019-01-22
desc: "Como utilizar chamadas assincronas"
keywords: "SSIS,Pacotes,Sincrono,Assincrono,blog,easy"
categories: [SSIS]
tags: [SSIS,SQL]
icon: icon-html
---
Algumas vezes queremos utilizar chamadas de pacotes SSIS porem queremos que estas chamadas variem em seus parametros e somente se determinada condições atendidas e que sejam executadas em paralelo.
Neste post demonstro a arquiterura da solução encontrada para este tipo de comportamento.
This is a raw snippet:

```
hello world
123
This is a text snippet
```


This is a JavaScript snippet:

```
const add = (a, b) => a + b
const minus = (a, b) => a - b

console.log(add(100,200))  // 300
console.log(minus(100,200))  // -100
```

This is a Python snippet:

```
def say_hello():
    print("hello world!")

say_hello()   // "hello world!"
```

---

Side note comment: applied a bug fix similar to [this commit](https://github.com/Atlas7/atlas7.github.io/commit/6659f4a47f6ec66987adb0f683a9c6f3842252ae#diff-818954a41dbfb01af70050a459c603b9) to ensure code snippet does not collapse unexpectly upon clicking on it. This issue is tracked [here](https://github.com/jarrekk/Jalpc/issues/97).