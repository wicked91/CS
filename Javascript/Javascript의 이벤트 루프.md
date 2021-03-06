## Javascript의 이벤트 루프

자바스크립트는 **단일쓰레드** 기반의 언어이다. 하지만 이벤트 루프를 통해 동시성을 지원하고 있다.

자바스크립트가 단일쓰레드 기반의 언어라는 것은 자바스크립트 엔진이 **단일 호출 스택**을 갖는 다는 점에서만 맞는 말이다.
실제로 브라우저, Node.JS에서는 여러개의 쓰레드가 사용되며 이러한 환경이 단일 호출 스택을 사용하는 자바스크립트와 연동하기 위해 필요한 것이 **이벤트 루프** 인 것이다. 


자바스크립트에서 함수가 실행되는 방식을 **Run to Completion**라고 한다. 이는 하나의 함수가 실행되면 이 함수의 실행이 끝날 때까지는 다른 어떤 작업도 중간에 끼어들지 못한다는 의미이다. **단일 호출 스택**을 사용하는 자바스크립트에서 스택에 쌓여있는 모든 함수들이 실행을 마치고 스택에서 제거되기 전까지는 다른 어떠한 함수도 실행될 수 없다. 

호출스택이 비워질때까지 콜백함수들을 **태스크 큐**에서 대기한다. 만약 호출스택이 비워지면 **이벤트 루프**에 의해 
**태스크 큐**에서 대기하던 콜백함수를 불러와 실행한다.

## 참고링크
- https://meetup.toast.com/posts/89