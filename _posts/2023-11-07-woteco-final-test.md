---
layout: single
title: "우테코 최종 테스트"
categories: "woteco"
tag: ["Test"]
author_profile: false
sidebar:
  nav: "counts"
---

## 미션 시작

1. Fork
2. git clone
3. git checkout -b kimmireu0220
4. README.md 파악
5. npm install
6. npm test

## docs/README.md 작성

1. 🚀 기능 요구 사항
2. 🛠️ 구조 설계
3. ⚙️ 기능 구현 목록
4. ✅ 최종 체크포인트

## 파일 구성

📦src

┣ 📂constants

┃ ┣ 📜error.js

┃ ┣ 📜messages.js

┃ ┗ 📜system.js

┣ 📂controller

┃ ┗ 📜Controller.js

┣ 📂domain

┃ ┗ 📜index.js

┣ 📂exceptions

┃ ┗ 📜ApplicationError.js

┣ 📂service

┃ ┗ 📜index.js

┣ 📂utils

┃ ┗ 📜validator.js

┣ 📂view

┃ ┣ 📜InputView.js

┃ ┣ 📜OutputView.js

┃ ┗ 📜index.js

┣ 📜App.js

┗ 📜index.js

## 구현

```javascript
import { InputView, OutputView } from "../view/index.js";

class Controller {
  /**
   * 입출력을 담당하는 View입니다.
   */
  #view = {
    input: InputView,
    output: OutputView,
  };

  /**
   * 비즈니스 로직을 담당하는 Service입니다.
   */
  #service = {};

  async start() {
    await this.#handleError(async () => {});
  }

  /**
   * 해당 콜백 함수 실행 중 에러가 발생할 시 함수를 다시 시작합니다.
   * @param {Function} action 에러 핸들링 대상이 될 함수입니다.
   */
  async #handleError(action) {
    try {
      await action();
    } catch ({ message }) {
      this.#view.output.error(message);
      await this.#handleError(action);
    }
  }
}

export default Controller;
```

## 과제 제출
