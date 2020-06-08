---
title: "[iOS] AutoLayout을 Code로 사용할 때 유의점"
date: 2018-12-13 08:42:28 -0400
categories: iOS
tags:
- UI
- Autolayout

---

AutoLayout을 Code로 직접 작성할 때 가장 기본이면서 중요한 것이 View를 선언하고 

```swift
translatesAutoresizingMaskIntoConstraints = NO
```
를 입력해주는 것이다.

translatesAutoresizingMaskIntoConstraints를 NO로 설정하지 않으면 아무리 View에 AutoLayout을 적용한들 먹히지 않는다.

그런데 Code로 View를 다루다보면 많이 사용하게 되는 method 중 하나가 viewWithTag다.

어떠한 이유에선지는 모르겠으나 viewWithTag는 translatesAutoresizingMaskIntoConstraints가 적용되질 않는다. 이미 translatesAutoresizingMaskIntoConstraints를 적용하고 addSubView한 View도 viewWithTag로 호출하면 translatesAutoresizingMaskIntoConstraints가 적용되지 않은 상태로 초기화된다. 임의의 View를 선언하고 적용시켜보아도 역시나 translatesAutoresizingMaskIntoConstraints는 초기화상태다.

물론

```swift
[self.view viewWithTag:0].translatesAutoresizingMaskIntoConstraints = NO;
```

같은 Code도 적용되지 않는다.

AutoLayout을 사용하려면 translatesAutoresizingMaskIntoConstraints를 적용하고 바로 사용해야 한다.

사용 시점에 translatesAutoresizingMaskIntoConstraints를 다시 적용해도 먹히지 않기 때문이다.

하루 종일 헤매다가 Log 찍어보고 발견해서 기록해두는 오답노트.