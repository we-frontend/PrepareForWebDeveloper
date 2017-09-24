# * Explain event delegation

## 개념
  - Javascript Event
    - Event Delegation
      - Event Bubbling, Event Capture
    - addEventListener
    - Event Object
      - Event Target

---

SPA 이전 웹사이트들에서 자바스크립트의 중요한 역할은 웹사이트의 동작을 구현하는 것입니다. 여기서 말하는 동작은 애니메이션이 아닌, 동적인 상호작용을 뜻합니다. (애니메이션은 CSS3의 역할이라고 생각합니다.)



위와 같은 동적인 상호작용을 `Event`라고 지칭합니다. 사용자의 이벤트 요청을 받아들이기 위해서는 사용자의 이벤트 요청을 받아들이기 위한 장치를 마련해두어야 합니다.



이를 위한 가장 일반적인 방법이 `addEventListener`입니다. `addEventListener`의 대상이 될 수 있는 `EventTarget`은 `Element`, `Document`, `Window`와 같은 이벤트를 지원하는 객체입니다. 일반적으로는 `document.querySelector()`를 통해 특정 `Element`를 지칭하여 `addEventListener`를 추가합니다.



IE9부터 사용 가능한 `addEventListener`는 다음과 같은 인자를 갖고 있습니다. [addEventListener MDN](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/addEventListener)

`type`, `listener`, `useCapture`, `wantsUntrusted`



- `type`

`EventTarget`에 어떤 `Event`가 일어났을 때, `listener parameter`를 호출할지 결정하는 문자열입니다. 어떤 종류가 있는지는 다음 페이지에서 확인할 수 있습니다. [Event reference MDN](https://developer.mozilla.org/en-US/docs/Web/Events) 일반적으로 많이 사용하는 것은 `click`, `load` 등입니다.




- `listener`

`type`에서 정의한 `event`가 발생했을 때 호출될 객체입니다. 일반적으로 자바스크립트 함수로 합니다. 이 함수를 웹 브라우저가 호출하면서 인수로 `Event` 객체를 넘겨줍니다. 이 인자를 일반적으로 `e` 또는 `event`로 정의합니다.




- `options` `||`  `useCapture`

인수가 `object`이면 options를, `boolean`을 넘겨주면 useCapture로 인식합니다. [WICG Link](https://github.com/WICG/EventListenerOptions/blob/gh-pages/explainer.md#eventlisteneroptions)




- `useCaputre`일 때 (default `false`)


이 인자는 `Event`의 전파방식을 결정합니다. false일 경우 이벤트가 발생한 node로부터 









##### * Reference

- Event Delegation
  - [자바스크립트 이벤트, 이벤트 버블링, 이벤트 캡춰링](http://frontend.diffthink.kr/2016/08/blog-post_16.html)
  - http://poiemaweb.com/js-event#8-event-delegation-이벤트-위임
  - https://github.com/nhnent/fe.javascript/wiki/August-22-August-26,-2016
  - https://opentutorials.org/module/904/6768
  - http://poiemaweb.com/js-event#6-event-flow-이벤트의-흐름

- Javascript Event
  - [EventTarget.addEventListener()](https://developer.mozilla.org/ko/docs/Web/API/Event)
    - Event Object
        - [13.2 이벤트 - 이벤트 객체](http://sonim1.tistory.com/152)
        - [Event MDN](https://developer.mozilla.org/ko/docs/Web/API/Event)
        - [Event.target MDN](https://developer.mozilla.org/ko/docs/Web/API/Event/target)