---
title: "[iOS/Swift] Autolayout 구현시 알아둘 점"
date: 2019-11-05 08:42:28 -0400
categories: iOS swift autolayout

---

- Autolayout에서 이미 active된 constraint의 경우 constant값을 변경할 경우 따로 active를 하지 않아도 그대로 적용된다.

- Autolayout을 변수에 할당해서 관리할 경우 이미 할당된 constraint에 새로운 constraint를 할당하는 방법은 쓰지 않도록 하고 상황에 따라 active, inactive만 제어하도록 한다. 그 이유는 변수에 새로운 constraint를 할당하더라도 기존의 constraint는 view에서 해제되는게 아니라 유지된 채 새로운 constraint만 할당되기 때문에 제어가 꼬이게 된다. (해당 변수의 constraint를 바꿔야 할 경우 반드시 inactive시킨 후에 할당 후 다시 active해야 한다.)

- ```swift
  sampleTopConstraint = sampleView.topAnchor.constraint(equalTo:view.topAnchor)
  
  sampleTopConstraint.isActive = false
  sampleTopConstraint = sampleView.topAnchor.constraint(equalTo:anotherView.topAnchor)
  sampleTopConstraint.isActive = true
  ```

  

- isActive =  false를 안할 경우 동시에 따라야 할 제약이 생기게 되어 UI가 깨지게 된다.(Unable to simultaneously satisfy constraints.)

- isActive를 아예 안할 경우에는 변수에 할당된 constraint만 바뀌고 아무 액션도 일어나지 않는다. 더불어 기존에 변수로 제어하던 constraint는 직접 제어하던지 다시 변수로 할당해야 한다.

- 따라서 혼선을 막기 위해 변수로 constraint를 제어할 경우 하나의 변수에는 하나의 constraint만 사용하는 게 좋다.

- 변수로 활용할 때에는 constant와 active/inactive만 활용하도록 한다.