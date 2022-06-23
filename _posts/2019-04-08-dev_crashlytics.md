---
title: "[개발] Crashlytics 사용시 주의점"
date: 2019-04-08 08:42:28 -0400
categories: dev
tags:
- Crashlytics



---

앱 개발을 하다보면 버그나 오류로 인한 앱 크래쉬를 피할 수가 없는데 문제는 사용자에게 배포되면 친절하고 감사하게도 직접 크래쉬 리포트를 해주시는 거의 일어나지 않을 경우를 제외하면 정확한 크래쉬 상황을 파악하기가 쉽지 않다.(물론 플레이스토어 대시보드나 Xcode organizer에서 확인할 수는 있지만)

이때 Firebase Crashlytics를 사용하면 좋다.

실시간으로 오류 리포트가 들어오고, 해당 오류가 발생한 라인과 히스토리까지 제공해주기 때문에 비교적 원인 파악하기가 쉽다.

단, 변수에 nil이나 잘못된 값이 들어와서 Crash가 발생했을 경우 그 잘못된 값에 대한 정보까진 제공하지 않는다.

이건 사용자가 맞춤로그나 맞춤 키를 미리 설정해둬야 확인할 수 있다.

이 방식의 문제는 주어진 데이터만으로 버그 원인 해결이 안될 경우 원인 파악을 위해 로그나 키를 추가하고 버그가 존재하는 버전을 배포해야하는 점이다.

(다른 방법을 알고 계시면 알려주세요 ㅠㅠ)

그리고 가장 치명적인 문제는 키를 사용할 경우인데 변수가 nil이어서 앱이 크래쉬가 발생할 경우 이 값을 추적하려고 nil이 될 가능성이

있는 변수를 키로 설정하면 안된다. 맞춤로그로 이 데이터를 찍어볼 경우에는 문제가 되지 않는다. Crashlytics에서 nil이라고 로그가 찍힐 뿐이다.

하지만 키로 설정할 경우 변수가 nil이면 이 키를 설정하다가 앱이 죽어버린다. 혹 떼려다가 혹 붙이는 격이다. 이 걸 안 후로 맞춤 키 기능은 거의 사용하지 않고 있다.

따라서 맞춤 키는 확실하게 데이터가 존재하는 경우에만 사용할 것을 권하는 바이다.