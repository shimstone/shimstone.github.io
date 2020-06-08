---
title: "[iOS / Common] xcodeproj와 xcworkspace중 어떤 걸 실행시켜야 할까?"
date: 2018-12-06 08:42:28 -0400
categories: iOS cocoapods xcworkspace xcodeproj openSource
---

아주 기초중에 기초이고 당연하다면 너무 당연한 얘기지만

의외로 처음 iOS 개발을 하면 헷갈리는 것 중에 하나가 이 xcodeproj와 xcworkspace의 차이점이다.

특히 오픈소스나 튜토리얼 등 다른 사람이 개발한 코드를 받아서 실행시켜 볼 경우

둘 중에 뭘 실행시켜야 하지 헷갈릴 수 있다. (제가 그랬거든요...)

왜냐하면 얼핏보면 둘 다 실행시켰을 때 똑같이 Xcode가 실행되고 특별한 차이점이 보이지 않기 때문.

본인이 직접 생성한 프로젝트에는 처음에 xcodeproj 밖에 존재하지 않는다.

xcworkspace는 프로젝트의 집합소같은 역할로 외부 라이브러리를 사용할 경우에

즉 Cocoapods 등을 사용하여 외부 라이브러리 등을 내 프로젝트에 추가한 경우에 필요한 파일이며

내 프로젝트와 라이브러리를 연결해주는 역할을 한다.

따라서 이런 경우에는 xcodeproj가 아닌 xcworkspace를 실행시켜줘야한다.

외부 라이브러리가 추가되어있는 프로젝트를 xcodeproj로 실행시킬 경우 라이브러리 연결이 되지

않아 문제가 생길 수 있다.

따라서 외부 라이브러리 연결이 되어 있다면 xcworkspace를 사용하고,

내 프로젝트는 외부라이브러리 연결 없이 사용한다하면 처음 생성된 대로 xcodeproj를 사용하면

되겠다.

