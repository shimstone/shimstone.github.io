---
title: "[iOS] UIStackView와 AutoLayout을 함께 사용시 주의할 점"
date: 2019-02-19 08:42:28 -0400
categories: iOS
tag:
- Autolayout
- UIStackView
---

UIStackView는 intrinsic Content size를 사용하기 때문에 임의로 autolayout에서 height를 지정하면 안된다.
작동이 안되는 것은 아니지만 간헐적으로 마지막 자식뷰의 addArrangeView가 작동을 안하는 경우가 발생한다.

예를 들어

```swift
[view1.heightAnchor constraintEqualToConstant:50];
[view2.heightAnchor constraintEqualToConstant:50];
[view3.heightAnchor constraintEqualToConstant:50];
[view4.heightAnchor constraintEqualToConstant:50];
[view5.heightAnchor constraintEqualToConstant:50];
```

인 view 5개를 stackView에 addArrangeSubview 했을 때

```swift
[stackView.heightAnchor constraintEqualToConstant:250];
```
이라고 constraint를 지정하면 autolayout conflict가 발생하는 경우가 있는데 내용을 살펴보면 마지막 자식뷰가 add가 안되서 stackView의 Intrinsic Content Size 상으로는 height가 200인데 constraint로 지정된 값은 250이라서 에러가 발생한다.

정확히는 마지막 view의 height 때문에 conflict가 발생한다고 log가 찍히지만 실제 테스트해본 내용으로는 위와 같다.

문제는 무조건적으로 발생하는 것이 아니라 간헐적으로 발생하기 때문에 초기 구현시에 발견하지 못하고 넘어갈 수 있다.

UIStackView와 Auto layout을 함께 쓴다면 height 지정은 피하도록 하자.

해당 코드 삭제 후 위에 기술한 에러는 더 이상 발생하지 않는다.