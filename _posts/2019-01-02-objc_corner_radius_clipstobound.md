---
title: "[iOS] cornerRadius와 clipsToBounds의 관계"
date: 2019-01-02 08:42:28 -0400
categories: iOS
tag:
- UI

---

iOS에서 UI를 꾸미다보면 굉장히 자주 접하게 되는 디자인 중 하나가

'둥근 모서리'

처음 구현해보려고 자료 찾다보면 습관처럼 나오는 코드가 바로 cornerRadius와 clipsToBounds이다.

cornerRadius는 둥근 정도를 지정하는 값이라고 생각하면 되는데, cornerRadius와 clipsToBounds를 무조건적으로 같이 쓰는 코드를 많이 보다보니 cornerRadius로 수치를 정하고 clipsToBounds로 수치만큼 뷰를 잘라내는(?) 거라고 당연하게 생각하고 있었다.

실제로 예전에 그런 내용을 읽어서 그렇게 이해하고 있었는데

아.니.었.다.

틀린 것은 아니지만 정확하게 말하자면 cornerRadius로 적용한 크기 만큼 해당 view와 관련된 영역을 잘라내는 것이다.

예를 들어 view의 모서리 부근에 텍스트가 있는데 cornerRadius 수치가 커서 이 텍스트가 뷰 영역 밖으로 나가게 될 경우 clipsToBounds가 true면 텍스트가 잘려서 보인다.

clipsToBounds가 false면 텍스트가 view에서 튀어나간 그대로 보인다.
  

```swift
view.layer.cornerRadius = 0
view.clipsToBounds = false
```

<img src = "http://127.0.0.1:4000/assets/images/clipsToBounds_1.png" width="30%"> 


```swift
view.layer.cornerRadius = 30
view.clipsToBounds = false
```

<img src = "http://127.0.0.1:4000/assets/images/clipsToBounds_2.png" width="30%"> 

```swift
view.layer.cornerRadius = 30
view.clipsToBounds = true
```

<img src = "http://127.0.0.1:4000/assets/images/clipsToBounds_3.png" width="30%"> 



마찬가지로 shadow는 view 바깥에 잡히게 되는데 clipsToBounds를 YES로 해버리면 앞서 말한대로 view 바깥영역을 다 잘라내기 때문에 shadow 효과가 먹통이 되어버린다.

따라서 clipsToBounds는 UI에 맞춰서 적절히 사용하면 되는 것이지 cornerRadius를 적용하기 위해 무조건 사용해야 하는 것은 아닌 것이다.

오늘 clipsToBounds가 NO인 뷰가 어떤 뷰는 cornerRadius가 먹히고 어떤 뷰는 안먹히면서 몇 시간을 헤매다가 깨닫게 된 사실이었다 ㅠㅠㅠ

(정작 cornerRadius가 안 먹혔던 뷰는 background 설정 문제였....)
