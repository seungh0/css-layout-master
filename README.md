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

- children 에게 줄 수 있는 property
- cross axis (like align items)

#### order

- default -> order: 0
- children 에게 줄 수 있는 property
- 세개중 만약 가운데를 order:1 로 지정하면 order -> (0, 0, 1)로 마지막으로 가짐.

### align-content vs align-items

- align-content 는 줄 사이의 간격을 결정하는 반면, align-items 는 전체 항목이 컨테이너 내에서 정렬되는 방식을 결정합니다. 한 줄만 있으면 align-content 가 효과가 없습니다.

### flex-grow, flex-shrink

- child 에게 줄 수 있는 property.

#### flex-shrink

- 기본적으로 element의 행동을 정의함.
- 화면에 꽉 찰 경우 (공간이 부족할 경우), 얼마나 찌그러질지
- default: 1
- flex-shrink: 2 => 1/2의 길이로 쭐어듬

#### flex-grow

- 남아있는 공간을 가져가는 비율.
- default: 0

### flex-basis

- flex-grow 되지 않았을 경우, 기본 main axis
