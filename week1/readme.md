# 📌 유의 사항

> 과제 풀이 전 아래 유의사항을 꼭 숙지해 주시길 바랍니다. 이를 어길 시 평가에 불이익이 있을 수 있습니다.

- `HTML`, `CSS`, `JavaScript` 기반의 베이스 코드가 주어집니다.
- **라이브러리나 프레임워크는 쓸 수 없으며, `Vanilla JavaScript`로만 과제를 수행해야** 합니다.
- `npm`, `yarn` 및 `cdn` 등을 활용한 외부 패키지를 활용할 수 없습니다.
- 프로그래머스 사이트에서 실행되는 `VSCode` 상에서 시험을 보셔야 합니다.
- 미응시 또는 `0`점은 자동 실격됩니다.
- 본 과제는 자동 채점 시스템에 의해 채점됩니다.
  - 반드시 `크롬(chrome)` 브라우저에서 진행해야 하며 개발자 도구 사용이 가능합니다.
  - 지문에 제시된 제약 사항을 따르지 않을 경우 정상적으로 채점이 되지 않을 수 있습니다.
- **`pages` 폴더 내부의 `problem_2.html` 파일과 `styles` 폴더 내부의 `problem_1.css`, `problem_2.css` 파일은 절대로 수정하지 않습니다.**

  - 반드시 지문에 제시된 `html` 및 `css` 파일에 있는 선택자 요소를 활용합니다.
  - 응시자가 임의로 작성하여 적용하는 경우 정상적으로 채점이 되지 않습니다.

- **정답 코드는 각 문제에 해당하는 번호에 맞게 `scripts` 폴더 내부의 `problem_1.js`, `problem_2.js`에 작성합니다.**

  - **채점 가능**

    - 각 `problem_1.js`, `problem_2.js` 파일에 모든 솔루션 코드를 작성하는 경우

      ```javascript
      // problem_1.js

      console.log("Hello World");
      ```

    - 추가적인 파일을 생성하여 해당 코드를 `problem_1.js`, `problem_2.js`에 연결하는 경우

      ```javascript
      // solution.js

      import { add, subtract } from "./problem_1.js";

      console.log(add(5, 3));
      console.log(subtract(5, 3));
      ```

      ```javascript
      // scripts/problem_1.js

      export function add(a, b) {
        return a + b;
      }

      export function subtract(a, b) {
        return a - b;
      }
      ```

  - **채점 불가능**

    - HTML 문서 내에 미리 작성한 `<script>` 안에 정답 코드를 작성하는 경우
      ```html
      <body>
        ...
        <script>
          console.log("Hello World");
        </script>
      </body>
      ```
    - `problem_1.js`, `problem_2.js` 파일이 아닌 다른 이름의 `.js` 파일을 만들어 코드를 작성하는 경우

      ```javascript
      // app.js
      console.log("Hello World");
      ```

- 아래와 같이 VSCode 우측 상단의 `미리 보기 열기` 버튼을 통해 보다 편리하게 문제를 확인할 수 있습니다.
  ![howtousevscode](https://user-images.githubusercontent.com/91870252/233291623-3eb89d4c-11ca-47a1-8218-cb5496781c2b.gif)

- 문제에 제시된 예시 GIF는 예시사항이므로 실제 데이터와는 다를 수 있습니다.

# 📌 1번 문제. 항공편 검색하기

> - 특정 조건에 맞는 항공편을 검색하는 기능을 구현하는 문제입니다.
>
> - 1번 문제에 대한 자세한 요구사항은 `문제` 폴더의 `문제 1번.md` 파일을 참조해 주세요.

# 📌 2번 문제. 항공편 예약하기

> - 항공편 예약을 위한 탑승객 정보 및 항공료 계산하는 기능을 구현하는 문제입니다.
>
> - 2번 문제에 대한 자세한 요구사항은 `문제` 폴더의 `문제 2번.md` 파일을 참조해 주세요.
