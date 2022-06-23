---
title: "[개발] Framework VS Library"
date: 2019-03-29 08:42:28 -0400
categories: dev
tag:
- Framework
- Library

---

처음 개발자가 되던 당시 여러가지 개발 방법을 연구하고 공부하면서 시작한게 아니라 바로 업무에 뛰어들어 부딪히면서 익히다보니 이런 저런 개발 용어에 대해 명확한 이해가 떨어지는 일이 많다.

물론 일하면서 접하게 되니 어떤 용도인지는 알지만 Clear하지 않은 느낌이랄까.

오늘 문득 이 내용에 대해 생각하게 될 일이 있어서 정리해둔다.

Framework, Library 둘 다 다른 개발자가 미리 개발해둔 Code를 가져다 쓰는 것에서는 뭔가 비슷해보인다.
많은 블로그나 글들에서는 제어의 주도권이 어딨느냐 등의 원론적인 얘기를 하는데 난 그게 더 이해하기 어렵다;

내 식대로 정의해보면

1. Framework
 - 뼈대라는 말처럼 그냥 집이라고 생각하면 될 거 같다. 그 집을 사무용으로 쓸지 주거용으로 쓸지
  가구는 어떻게 배치할 것이며 조명은 어떤 것을 달지는 전적으로 사용자에게 달렸다.
  Framework(집)으로 환경을 제공해주고 그 안을 뭘로 채울 것인지나 용도는 개발자에게 달린 것이다.
  국내에서 Spring Framework를 엄청나게 많이 쓰지만 프로젝트마다 그 결과물은 모두 다르다.
  Framework로는 미리 구현된 틀에 내용물을 채워서 최종적인 결과물을 만들어낸다.

2. Library
 - 도구다. 집을 꾸미는데 나사를 박을 일이 있다고 하자. 그냥 드라이버를 쓸 수도 있고, 전동드릴을 쓸 수도
  있다. 하지만 나사를 박는데 밥솥을 쓰지는 않는다. 나사를 박는 프로그램을 만드는데 개발자는 드라이버 라이브러리를 쓸 수도 있고, 전동드릴 라이브러리를 쓸 수도 있지만 나사를 박는데 밥솥 라이브러리를 쓰진 않는다. 밥솥 라이브러리는 밥을 짓는 프로그램에서 쓰일 것이다. 즉 정해진 용도로
 사용함으로써 의미를 가진다. 
  - 도구라는 말의 의미처럼 라이브러리 그 자체가 결과물이 되진 않는다. 무언가의 결과물을 만들어내기 위해 사용하는 옵션일 뿐이다. 
  
  


전동드릴, 밥솥이라는 결과물이 있지 않느냐? 하면 그건 전동드릴과 밥솥 Framework의 결과물일 것이다. 전동드릴도
 브랜드와 크기, 파워에 따라서 안을 구성하고 있는 내용물은 전혀 다르니까.
 이 관점에서는 전동드릴 Framework가 있고, 그 안의 부품을 구성하기 위해 납땜시 사용한 인두 Library
 가 존재하지 않을까?
