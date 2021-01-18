# CSS Layout 마스터 클래스

## inline vs block vs inline-block

- inline

  - element (width, height를 가질 수 없음.)
  - 옆에 올 수 있음.

- box

  - box (width, height를 가짐)
  - 옆에 올 수 없음.

- inline-block
  - box (width, height를 가짐)
  - 옆에 올 수 있음.

### inline-block의 문제점

- 관리하기 힘듬..
- 뭐만하면 다음 줄로 넘어가고
- 기본 여백 있고..

### flexbox

- inline-block의 문제를 해결.

- children와 얘기하지 않음.
- box들이 flex container 안에 있어야한다 => 부모를 display: flex로 설정.
- 바로 위의 부모가 자식의 위치를 움직일 수 있음.

#### flex-direction

- flex-direction: row
  <img src="https://camo.githubusercontent.com/4ad163b9f1701b75df04eafc0c6d5db24a5c69fa6776ac7f9ccefddc6974b1a3/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a5f527579366a464737675570536637364955634a54512e706e67">

- flex-direction: column
  <img src="https://mdn.mozillademos.org/files/15615/Basics2.png">

#### justify-content

- main-axis

#### align-items

- cross axis

#### align-self

- children 에게 줄 수 있는 property 1.
- cross axis (like align items)

#### order

- default -> order: 0
- children 에게 줄 수 있는 property 2.
- 세개중 만약 가운데를 order:1 로 지정하면 order -> (0, 0, 1)로 마지막으로 가짐.
