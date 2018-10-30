## Blocking/NonBlocking/Synchronous/Asynchronous

1. Blocking/NonBlocking은 호출되는 함수가 바로 리턴하느냐 마느냐가 관심사이다.

- 호출된 함수가 바로 리턴해서 호출한 함수에게 **제어권**을 넘겨주고, 호출한 함수가 다른 일을 할 수 있는 기회를 줄 수 있으면 **NonBlocking**이다.

- 호출된 함수가 자신의 작업을 모두 마칠 때 까지 호출한 함수에게 **제어권**을 넘겨주지 않고 대기하게 만든다면 **Blocking**이다.

2. Synchronous/Asynchronous는 호출되는 함수의 작업완료 여부를 누가 신경쓰냐가 관심사이다.

- 호출되는 함수에게 callback을 전달해서, 호출되는 함수의 작업이 완료되면 호출되는 함수가 전달 받은 callback을 실행하고, 호출하는 함수는 작업 완료 여부를 신경쓰지 않는다면 **Asynchronous**다.

- 호출하는 함수가 호출되는 함수의 작업 완료 후 리턴을 기다리거나, 또는 호출되는 함수로 부터 바로 리턴 받더라도 작업 완료 여부를 호출하는 함수 스스로 계속 확인하며 신경쓰면 **Synchronous**다.

* * *
### Non-Blocking
Non-Blocking은 크게 두가지 의미로 나뉜다.
- Non-blocking algorithm
    - 어떤 쓰레드에서 오류가 발생하거나 멈추었을 때 다른 쓰레드에게 영향을 끼치지 않도록 만드는 방법들을 말한다.
    <br>
    - 공유 자원을 사용하는 멀티 쓰레드 프로그래밍을 할 때, 특정 공유 자원을 사용하는 부분에서 뮤텍스나 세마포어 등을 사용하여 여러 쓰레드에서 동시에 접근하지 못하도록 개발자가 보장하는 것이 전통적인 방법이었다. 
    <br>
    - 반면 Non-blocking algorithm(Wait-freedom, Lock-freedom 등)을 사용하면 공유 자원을 안전하게 동시에 사용할 수 있다.
 <br>

- Non-blocking I/O
    - 입출력 처리는 시작만 해둔 채 완료되지 않은 상태에서 다른 처리 작업을 계속 진행할 수 있도록 멈추지 않고 입출력 처리를 기다리는 방법을 말한다.
    <br>
    - I/O 처리를 하는 전통적인 방법은 I/O 작업을 시작하면 완료될 때까지 기다리는 방법이다. 반면, Non-blocking I/O 방식을 사용하면 외부에 I/O 작업을 하도록 요청한 후 즉시 다음 작업을 처리함으로써 시스템 자원을 더 효율적으로 사용할 수 있게된다.
    <br>
    - 그러나 I/O 작업이 완료된 이후에 처리해야하는 후속 작업이 있다면, I/O 작업이 완료될 때까지 기다려야 한다. 따라서 이 후속 작업이 프로세스를 멈추지 않도록 만들기 위해, I/O 작업이 완료된 이후 후속 작업을 이어서 진행할 수 있도록 별도의 약속(Polling, Callback function 등)을 한다.

## 참고링크
- https://homoefficio.github.io/2017/02/19/Blocking-NonBlocking-Synchronous-Asynchronous/
- https://tech.peoplefund.co.kr/2017/08/02/non-blocking-asynchronous-concurrency.html
- https://brainbackdoor.tistory.com/26


