## Blocking/NonBlocking/Synchronous/Asynchronous

1. Blocking/NonBlocking은 호출되는 함수가 바로 리턴하느냐 마느냐가 관심사이다.

- 호출된 함수가 바로 리턴해서 호출한 함수에게 **제어권**을 넘겨주고, 호출한 함수가 다른 일을 할 수 있는 기회를 줄 수 있으면 **NonBlocking**이다.

- 호출된 함수가 자신의 작업을 모두 마칠 때 까지 호출한 함수에게 **제어권**을 넘겨주지 않고 대기하게 만든다면 **Blocking**이다.

2. Synchronous/Asynchronous는 호출되는 함수의 작업완료 여부를 누가 신경쓰냐가 관심사이다.

- 호출되는 함수에게 callback을 전달해서, 호출되는 함수의 작업이 완료되면 호출되는 함수가 전달 받은 callback을 실행하고, 호출하는 함수는 작업 완료 여부를 신경쓰지 않는다면 **Asynchronous**다.

- 호출하는 함수가 호출되는 함수의 작업 완료 후 리턴을 기다리거나, 또는 호출되는 함수로 부터 바로 리턴 받더라도 작업 완료 여부를 호출하는 함수 스스로 계속 확인하며 신경쓰면 **Synchronous**다.

## 참고링크
- https://homoefficio.github.io/2017/02/19/Blocking-NonBlocking-Synchronous-Asynchronous/



