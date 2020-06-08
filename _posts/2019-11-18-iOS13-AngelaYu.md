---
title: "[iOS / Study] iOS 13 & Swift 5 - The Complete iOS App Development Bootcamp by Angela Yu"
date: 2019-11-18 08:26:28 -0400
categories: iOS study

---

## 1. Getting started with iOS 13 and Swift 5.1

- 수강생이 강좌를 수강하면서 알아야 할 것들. 마음가짐

  ### 1. Intro to the Course. What's coming up?

    - 강사의 자기 소개와 해당 강의의 장점과 동기부여 영상(어떤 이점을 얻을 수 있는지에 대한 강조)

    - 앱개발, 디자인, 배포까지 한 번에 배울 수 있다고 강조

  ### 2. Download the Course Syllabus

    - 전체 강의 커리큘럼 PDF 다운로드

  ### 3. How to Get All the Free Stuff

    - 제공하는 무료 Assets에 대한 소개

  ### 4. Download your Massive Bundle of Assets

    - 강의에서 배포하는 무료 Assets 자료 다운로드

  ### 5. Download the 12 Rules to Learn To Code eBook PDF

    - 수많은 우수 학생들에게서 뽑아낸 코드를 배울 때 12가지 규칙 PDF 다운로드

  ### 6. How does an App Work?

    - 앱이 실제로 어떻게 돌아가는지에 대한 설명
      1. 앱에서 버튼 클릭
      2. 센서가 인식
      3. OS에 해당 내용 전달
      4. OS가 버튼이 소속된 앱에 버튼 클릭이 됐다는 메시지를 보내고
         코드에서 버튼이 클릭된 것에 해당하는 코드를 실행
      5. 실행된 코드가 화면에 반영
    - 따라서 앱 개발자는 각각의 상황에 따른 모든 시나리오와 무슨 작업이 실행되야 하는지에 대한 계획을 짜야함
      1. 일반적인 앱 실행에 대한 시나리오      ex) A 버튼을 누르면 B로 이동, C를 누르면 서버에 데이터 요청 등등
      2. 시스템 이벤트에 대한 처리                ex) 전화가 왔을때, 백그라운드로 진입했을 때 등등
    - 앱은 세가지 요소로 구성됨
      1. 스크린(UI)           - View
      2. 코드                    - Controller
      3. 데이터                 - Model

  ### 7. How to Make An App

    - 앱이 어떻게 만들어지는 지에 대한 과정을 설명 및 각 과정을 어떻게 배울 것인가 설명

      0. Why
         - 자신 스스로에게 이 앱이 왜 필요한지를 묻기
      1. Idea
         - 앱이 필요하다는 확신이 들면 아이디어를 생각해 내는 것에 그치지 않고 이게 정말 좋은 아이디어인지 검증이 필요. 많은 사람들에게 얘기하고, 다양한 범위의 의견을 들어야 함. MVP(Minimum Viable Product. 최소 기능 제품)을 만들어서 사람들에게 보여주고 테스트해서 실제로 흥미를 느끼는지를 보거나 아이디어를 설명하는 문서를 만들어서 SNS에 올려 사람들이 실제로 원하는지 확인
      2. Design
         - 와이어프레임, 프로토타입을 만든다.
         - 디자인은 기능뿐만 아니라 사람들이 사랑할만한 아름다운 앱을 만들기 위한 디자인이어야 한다.
      3. Development
         - 실질적인 개발을 진행한다. 
      4. Test
         - 전 세계의 모든 유저가 어떤 기계를 가지고 있는지에 상관없이 앱을 즐겁게 사용하기 위해 모든 기계에서 UI가 깨지지 않고, 잘 작동하는지를 테스트한다. 그래서 더 많은 사용자가 다운로드할 수 있도록 유도하는데 매우 중요한 리뷰 별점 5개를 받을 수 있도록 한다.
      5. Publish
         - 앱스토어에 배포
      6. Market
         - 앱을 배포하고 사용자에게 이런 소식을 전달

      7. Update
         - 지속적인 사용자 경험 향상을 위한 업데이트

  ### 8. How to Make the Most of the Bootcamp

    - 이 강의를 들을 때의 추천 학습 방법을 설명

  - 코딩할 메인컴퓨터와 영상을 볼 다른 디바이스를 갖추는 것을 추천.

  - 노트를 사용하여 중간중간 흥미롭거나 더 보고 싶은 내용을 메모
  - 절대 튜토리얼을 건너뛰지 말 것. 이 강의는 Step By Step으로 설계되어 있음

  ### 9. How to get Help When You're Stuck

  - 강의를 듣다가 막혔을 때, 에러가 났을 때 어떻게 해야할 지 설명
  - 아직 모르고 있다면 StackOverFlow.com은 빠르게 베프가 될 것임
  - 그래도 해결이 안되면 코드를 다시 읽어봐라.
  - 그래도 해결이 안되면 Q&A 게시판에서 같은 사례를 찾아라
  - 그래도 해결이 안되면 Q&A에 직접 문의해라.
  - 누구나 막히는 순간은 오고 StackOverFlow.com은 치트가 아니다. 
    모든 개발자들이 매일 겪는 일상이다. 그러니 좌절하지 말라

  ### 10. The Giant List of Resources

  - 강의 중간중간 나오는 참고자료에 대한 링크 제공

  ### 11. Developing for iOS - Tools And Materials

  - iOS를 개발하는데 필요한 하드웨어, 소프트웨어에 대한 설명
  - Mac(iMac, Mac pro, Mac mini, Macbook Series 등등)
  - Xcode
  - 실제 기기

  ### 12. Can I Use Windows?

  - 윈도우를 써도 될까하는 질문에 대한 답변.
  - 기타 개발에 필요한 내용에 대한 Q&A (11강에 나왔던 내용을 텍스트로 설명)

  ### 13. Getting set up with Xcode

  - Xcode를 받는 법, 설치 가능 조건 설명
  - 베타는 버그가 많기 때문에 다운 받지 말것

  ### 14. Pathfinder

  - 수강생의 수준에 맞게 시작할 수 있는 코스를 지정해줌
  - 나는 그냥 쌩초보다 생각하고 아예 처음부터 진행

## 2. Xcode Storyboards and Interface Builder

- Xcode

  ### 15. The I am Rich App

  - $999.99에 팔았던 아무 기능없는 I am Rich App의 사례를 소개
  - 이 섹션에서 배울 것들에 대한 Overview

  ### 16. Let's Create a Brand New Xcode Project

  - Single View Project를 하나 새로 생성해봄

  ### 17. A Walkthrough of the Xcode Development Environment

  - Xcode 화면에 대한 둘러보기(각 메뉴에 대한 자세한 내용은 앞으로 강의 중 설명)

  ### 18.Let's Design the User Interface!

  - Storyboard를 둘러보고, View에 Label, ImageView 올려보기 실습
  - iOS 좌표계에 대해 설명. Top-Left Corner가 기준(0)
  - 각 기기에 대한 해상도, Pt(포인트)에 대한 설명 (https://www.paintcodeapp.com/news/ultimate-guide-to-iphone-resolutions)
  - Pt는 아이폰 화면이 발전하면서 같은 크기에 더 많은 픽셀을 넣을 수 있게 되면서 만들어진 단위

  ### 19. Let's incorporate Some Image Assets

  - 18강에 이어지는 내용
  - 1x, 2x, 3x 이미지에 대한 설명
  - 1x = 1px, 2x = 4px, 3x = 9px
  - 따라서 수치가 올라갈 수록 더 선명하고 정확한 이미지 표현 가능
  - 실제 앱에서 사용되는 크기는 1x의 크기(하지만 2x, 3x이미지는 사이즈는 작아지지만 그만큼 더 선명한 이미지를 가짐)
  - appicon.co      - 이미지를 넣으면 1x, 2x, 3x를 생산해주는 사이트

  ### 20. How to Design And Add an App Icon

  - 앱 아이콘을 추가하는 방법 설명
  - 앱 아이콘을 가장 큰 이미지 한장을 쓰지 않고 일일히 세분화해놓은 이유는 일일히 Scale down할 경우 쓸데없이 리소스를 사용해 앱이 느려지기 때문
  - canva.com       - 무료로 아이콘을 디자인할 수 있는 사이트

  ### 21. Run Your App on Your iPhone or Simulator

  - 앱을 실행하는데는 실제 기기와 시뮬레이터를 통한 방법이 있다
  - 시뮬레이터는 앱을 실행할 기기를 선택하고 실행하면 끝
  - 실제 기기에 업데이트 할 시
    1. Xcode버전과 iOS 버전이 매치가 되어야 함. Xcode에서 지원하지 않는 버전이면 실행할 수 없음
    2. 애플 개발자 계정을 추가. (개발자 개정이 없을 경우 일반 Apple ID를 사용해도 무방)
    3. 앱 사이닝. 프로젝트 파일에서 Signing & Capabilities 탭으로 가서 Team을 선택하면 관련 에러들이 사라짐. 단, 실제 기기를 연결하고 선택까지 한 상태에서 진행해야 함. 기기를 연결하지 않으면 개발을 위해 등록된 기기가 없다는 에러를 계속 표시함.
    4. 실제 기기를 연결
    5. 자신을 믿어라!

  ### 22. App Signing and Provisioning Profile problems? I got you fam.

  - 앱 사이닝 관련해서 문제가 있을 경우 대처할 수 있는 다이어그램 제공

  ### 23. Join the Student Community

  - 수강생 커뮤니티 채널 링크 제공 (Discord)

## 3. Xcode Storyboard and Interface Builder Challenge

- I Am Poor 앱 만들기 실습

  ### 24. What you Will Create

  ### 25. Step 1: Create a New XCode Project 

  ### 26. Step 2: Add a Label Element from the Object Library

  ###  	27. Step 3: Add an Image View to the Storyboard 

  ###  	28. Step 4: Add an App Icon

  ### 	 29. Step 5: Run Your App

  ### 30. Step 6: Show off your work!

## 4. Swift Programming Basics - Collections, Constants & Variable
- 컬렉션 타입 및 변수, 상수
### 	31. What You'll Make by the End of this Module

  -  이번 섹션에서 배울 내용에 대한 Summary

  - Github에서 클론하는 방법을 배움
  - UI design
  - UI를 Programmatically하게 변경시키는 방법
  - 유저 액션에 대한 respond 감지
  - 변수, 배열, 주석 등등등

  ### 32. Cloning from Github and How to Download the L.A.B. Project Stubs

  - Github에서 클론 하는 방법을 배움
  - 기존에는 Download zip만 이용했는데 깃주소를 복사하고 Xcode -> Source Control -> Clone을 실행해서 주소를 입력하면 그대로 클론해서 프로젝트를 실행해줌. 앞으로 이 방법을 사용하자

  ### 33. How to Design Your App

  - Dicee앱 UI 구성 실습

  ### 34. Let's Link Our Design to Our Code

  - IBOutlet = Interface Builder Outlet
  - Who.What = Value             - Who의 What에 Value를 Set
  - IntelliSense를 사용할 때(자동완성)
    - Tab : 단어 단위의 자동완성까지 됨. diceImageView를 찾는데 diceIm까지 입력하고 Tab하면 diceImage까지 완성
    - Enter : 단어 전체가 자동완성. diceImageView를 찾는데 diceIm까지 입력하고 Enter하면 diceImageView까지 모두 완성
    - ImageView에 Image를 새로 Set할 때, UIImage(named:"")를 썼었는데 Image Literal을 입력하면 아이콘이 생성되고 그 아이콘을 더블클릭하면 Assets에 있는 Image list가 표시된다. 이 중에서 선택하면 이미지가 입력된다.

  ### 35. Responding to User Interactions with IBActions

  - IBAction 실습

  ### 36. [Swift Deep Dive] Naming Conventions, Commenting and String Interpolation

  - Naming Convention
    - camelCase         - Swift에서는 camelCase사용
    - kebab-case
    - snake_case
  - Commenting 
  - String Interpolation
    - print("Text \\(2+3) test")       \\() <- 이걸 String Interpolation이라고 한다.

  ### 37. Storing Data using Variables and Arrays

  - 변수와 배열에 대한 실습

  ### 38. [Swift Deep Dive] Variables

  - 변수에 대한 설명

  ### 39. How to sign up and submit exercises on Repl.it

  - 실습 사이트 가입 방법 설명

  ### 40. [Swift Deep Dive] Arrays

  - 배열에 대한 설명

  ### 41. How to Randomize the Dice Images

  - Int.random(in: 1...10)         1부터 10까지 랜덤한 숫자를 리턴
  - Array에서는 randomElement() 사용 가능
  - Refactoring
    - 중복되는 코드, 사용하지 않는 코드 등을 삭제하여 코드를 간결하게 만드는 과정

  ### 42. How to Solve the Error: "Maximum number of apps for free development reached"

  - 무료 계정에서 실제 기기에 추가할 수 있는 앱은 일주일에 3개까지로 제한된다. 따라서 이 메시지가 떴을 때는 기존에 설치한 앱을 삭제해주면 된다.
  - Xcode -> Window-> Devices and Simulators에 들어가서 기기에 설치된 앱을 삭제해주면 된다.

  ### 43. [Swift Deep Dive] Constants, the Range Operator and Randomisation

  - Constant를 쓰는 이유는 컴퓨터가 연산할때 Constant의 경우 앞으로 값이 변경되지 않을 것을 알 수 있기 때문에 데이터를 보다 효율적으로 저장할 수 있기 때문이다.
  - 그 외에도 변할 일이 없는 고정된 값으로 휴먼에러를 미리 예방할 수도 있다.
  - Range Operator
    - ...		- Upper bound included
    - ..<       - Upper bound not included

  ### 44. Download the Completed App Project

  - 완성된 앱 프로젝트 다운로드 방법

  ### 45. Thread 1: signal SIGABRT and "Not Key Value Coding Compliant" - How to fix it

  - Storyboard에서 연결한 IBOutlet이 이름이 바뀌거나 삭제되어 앱이 크래쉬가 날 때 해결하는 방법 설명

  ### 46. Do You Want This?

  - 이메일 뉴스레터 등록 권유 및 방법

## 5. Swift Programming Basics Challenges

- 앞서 실습해본 주사위 앱을 바탕으로 해서 매직볼 앱을 스스로 만들어보기

  ### 47. What You Will Create

  ### 48. Step 1 : Clone the Starting Project

  ### 49. Step 2 : Design the User Interface

  ### 50. Step 3 : Link Up the Design with Code

  ### 51. Step 4 : Use Code to Change the 8 Ball Image

  ### 52. Step 5 : Make the Ball Image Random

  ### 53. Step 6 : Show off your work!

  ### 54. Download the Complete Project

## 6. Auto Layout and Responsive UIs
- 오토 레이아웃

  ### 	55. Why do we need Auto Layout?

  - Autolayout의 필요성에 대해 설명

    ### 56. Size Classes Explained

    - 각 해상도를 대표하는 기기의 클래스
    - 기 각각의 클래스에 맞게 디자인을 일일히 해줄 수 없으므로 사용되는게 Auto layout

    ### 57. Setting Constraints and working with the Safe Area

    - Leading, Trailing, Top, Bottom Constraint를 Storyboard에서 설정하는 방법 설명
    - Safe Area, margin에 Constraint를 설정하면 어떤 차이가 있는지 설명

    ### 58. How to use Alignment and Pinning

    - Alignment는 기준을 가지고 위치를 설정
    - Pin은 수치를 가지고 위치를 설정

    ### 59. Working with Containers And Subviews

    - 각각의 View들을 Container역할을 할 VIew로 Embeded해서 배치하는 법 설명

    ### 60. Stack Views

    - StackView를 통해서 뷰들의 배치를 균일하게 하는 방법을 설명
    - 기존에는 StackView의 SubView들을 StackView에 constraint를 설정해서 사용했었는데 이는 잘못된 사용방법으로 보인다. distribution 설정에 따라 StackView의 배치가 달라지며 자동으로 subview에 대한 배치를 하기 때문에 StackView와 Subview간의 constraints를 별도로 설정해줄 필요가 없다.

    ### 61. Auto Layout(Optional) Boss Challenge

    - StackView를 통한 계산기 앱 UI 실습

    ### 62. Download the Completed Project

    ### 63. Calculator Challenge Solution and Walkthrough

    - 실습에 대한 설명

## 7. Using and Understanding Apple Documentation
- 애플 공식문서 보면서 개발하는 방법

  ### 		64. What You'll Make by the End of this Module

  - 이번 프로젝트에서 만들어 볼 앱에 대한 소개

  ### 		65. Setting up the Xylophone Project

  - Xylophone 앱 클론

  ### 	66. The 5 Step Approach to Solve Any Programming Problem

  - 문제를 해결해 나가는 절차를 소개

  1. Google
     - Search keyword : <What I want my app to do> + <Which programming language> + <Which Resource>
       - ex> play sound + swift + stack overflow

  2. Stack Overflow
     - 제일 연관이 있는 해답을 찾는다.
     - Accepted된 해답만 확인하지 말고 최소 상위 3개의 해답을 참고하도록 한다.
  3. Implement
     - Stack Overflow에서 찾은 해답을 자신의 프로젝트에 직접 적용해본다.
  4. Docs
     - 입력한 코드에 존재하는 클래스, 프레임워크 등에 대한 문서를 찾아서 본다.
     - developer.apple.com/documentation에서 키워드를 검색하여 문서를 읽어본다.
     - option + 클릭하면 중요한 내용만 Summarize된 내용을 Xcode내부에서 확인할 수 있다.

  5. Customize
     - 3에서 implementation한 코드를 내가 원하는 용도에 맞게 수정 or 불필요한 코드를 제거한다.

  ### 	67. [Swift Deep Dive] Functions and Scope

  - Function과 유효범위에 대한 설명

  ### 68. How to use repl.it

  - 실습 사이트 사용 방법에 대한 설명

  ### 69. Linking Multiple Buttons to the Same IBAction

  - IBAction에 여러개의 버튼을 Link하는 예제를 설명
  - 동일한 액션을 하는 여러개의 버튼에 대응하는 여러개의 func을 만들지 않고, 하나의 func에 링크시킨 후 분기 처리

  ### 70. [Swift Deep Dive] Functions with Inputs and Type Inference

  - Function과 타입추론에 대한 설명
  - Parameter : 매개변수. 함수에 전달되는 인자의 이름
  - Argument : 인자. 함수에 전달되는 실제 값

  ### 71. Playing Different Xylophone Sounds

  - 앞서 배운 function에 parameter를 추가하는 방법을 이용하여 실습 앱 수정

  ### 72. Boss Challenge

  ### 73. Download the Completed App Project

## 8. Intermediate Swift Programming - Control Flow and Optionals
- 조건문, 반복문, 옵셔널에 대한 설명

  ### 	74. What You'll Make by the End of this Module

  - 실습할 앱에 대한 설명 - Egg Timer

  ### 	75. Setting up the Egg Timer Project and Linking the Storyboard and ViewController

  ### 	76. [Swift Deep Dive] If-Else Control Flow

  - If-else 조건문 설명

  ### 	77. [Swift Deep Dive] Switch Statements

  - Switch 조건문 설명

  ### 	78. Conditional Statements Challenge Solution

  - Challenge 해설

  ### 	79. [Swift Deep Dive] Dictionaries

  - Swift의 모든 컬렉션은 [ ]로 표현
  - dictionary는 컬렉션의 일종으로 하나 이상의 Key, value 짝으로 구성된다.

  ### 	80. [Swift Deep Dive] Defining and Unwrapping Optionals

  - nil은 존재가 없음. null은 빈 주소값(데이터는 있지만 주소값이 없음)

  ### 	81. Dictionary Challenge Solution

  - Dictionary의 Value는 항상 Optional이다. 호출하는 key가 반드시 있다는 보장이 없기 때문이다.

  ### 	82. Implementing a Countdown Timer Challenge

  - 실습

  ### 	83. Egg Timer Challenge Solution

  - 실습 해설
  - Timer는 초기화되면서 바로 실행된다. 따라서 변수로 항상 tracking해서 적절한 시점에 invalidate해줘야 한다.

  ### 	84. Showing the Timer to the User with a Progress View

  - Progress Bar 실습

  ### 	85. Calculating the Progress Percentage

  - Progress Bar 실습

  ### 	86. Using the 5 Step Approach to Debug our App

  - Debugging의 5가지 단계
		1. What did you expect your code to do?
   		2. What happened instead?
  		3. What does your expectation depend upon?
  		4. How can we test the things our expectation depend on?
  		5. Fix our code to make reality match expectations

  ### 	87. Download the Completed App Project

## 9. iOS App Design Patterns and Code Structuring
