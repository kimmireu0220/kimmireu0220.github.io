---
layout: single
title: "우테코 최종 테스트"
categories: "woteco"
tag: ["Test"]
author_profile: false
sidebar:
  nav: "counts"
---

## Fork & Git Clone

## README.md 파악

## npm install & npm test

## docs/README.md 작성

## 파일 구성

📦**tests**

┣ 📜program-domain-test.js

┣ 📜specific-domain-test.js

┣ 📜ViewTest.js

┣ 📜ApplicationTest.js

┗ 📜StringTest.js

📦docs

┗ 📜README.md

📦src

┣ 📜(Program)Domain.js

┣ 📜(Specific)Domain.js

┃ 📜View.js

┃ 📜Controller.js

┣ 📜App.js

┣ 📜setting.js

┣ 📜message.js

┗ 📜index.js

## 구현

```javascript
// View.js
class View {
  async readLineAsnc(message) {
    const input = await Console.readLineAsync(message);
    this.#validateUserInput(input);
    return input;
  }

  async readIntegerAsnc(message) {
    const input = await Console.readLineAsync(message);
    this.#validateInteger(input);
    return input;
  }

  async print(message) {
    Console.print(message);
  }

  #validateUserInput(name) {
    if (name.trim() === "") throw new Error();
  }

  #validateInteger(number) {
    if (Number.isInteger(Number(number))) throw new Error();
  }
}

export default View;
```

```javascript
// Controller.js
class Controller {
  #view;
  #domain;

  constructor({ view, domain }) {
    this.#view = view;
    this.#domain = domain;
  }

  async start() {}

  async #retryOnError(callback) {
    try {
      return await callback();
    } catch ({ message }) {
      this.#view.print(message);
      return this.#retryOnError(callback);
    }
  }
}

export default App;
```

```javascript
// App.js
class App {
  #controller;

  constructor() {
    this.#controller = new Controller({
      view: new View(),
      domain: new Domain(),
    });
  }

  async play() {
    await this.#controller.start();
  }
}

export default App;
```

```javascript
// setting.js
const SETTING = Object.freeze({
  key: value,
});

export default SETTING;
```

## 과제 제출
