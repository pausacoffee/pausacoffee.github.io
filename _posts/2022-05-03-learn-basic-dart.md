---
layout: post
title: Dart 의 기초
subtitle: Let's study basic dart lan for flutter!
categories: Flutter
tags: [Flutter, Dart, Mac, VSCode]
---
## OverView ##
flutter는 크로스플랫폼 **프레임워크**이다. 고로 flutter를 사용하기에 앞서 dart에 대해 공부하고자 한다.  
이 정도 길이면 포스트를 나누는데... 솔직히 귀찮다...  
dart에 관련된 지식은 여기에 우겨넣거나 나중에 정리하도록 하자!  
(본 포스팅에서 소개하는 글보다 자세한 설명이 필요하다면 아래의 사이트를 이용하자! dart 공문서 사이트이다.)
> <https://dart.dev/samples>

간단한 dart 예제를 별도의 환경세팅 없이 학습해보고 싶다면 아래의 사이트를 이용하자!   
이 포스트에서 제공하는 코드도 dartpad에서 동작함.
> <https://dartpad.dev/?>

## 개발환경 ##
> MacBook pro(M1, 2020)  
> Monterey v.12.3.1  
> Visual Studio Code 버전: 1.66.2  
> Flutter 2.10.4  
> Dart 2.16.2  
> DevTools 2.9.2  
  
## 기본문법 ##
기본적으로 ;(세미콜론)으로 문장이 끝난다.  
#### print ####
<script src="https://gist.github.com/pausacoffee/6e8971504048ae2fb7225931911b508a.js"></script> 
#### 주석 ####
<script src="https://gist.github.com/pausacoffee/34ad2f0100c9105d3d7e88104b79dc83.js"></script>
#### 변수, var, 상수 ####
int, double, String, bool 을 기본적으로 제공한다.  
<script src="https://gist.github.com/pausacoffee/8792186514b2cc332c165745e1722f4c.js"></script> 
#### 연산자 ####
<script src="https://gist.github.com/pausacoffee/994680d065decee91216dd2c00eca45d.js"></script>
#### 형변환 ####
<script src="https://gist.github.com/pausacoffee/bb5684ec616477be3caa846b298f767c.js"></script>
#### 조건문 ####
<script src="https://gist.github.com/pausacoffee/8e72a9fb206b2f7d5bb2e6745b4798d9.js"></script>
#### 반복문 ####
<script src="https://gist.github.com/pausacoffee/c6a18ca39ab9a343a96c0c6003fa264a.js"></script>
  
## Function ##
**반환형식 함수명(인수형식 arg)** 의 패턴으로 구성된다. 다트는 함수도 객체이며 fuction이라는 형식을 갖는다.  
함수를 인수로 전달하거나 함수에서 함수를 반환하는 언어의 기능을 가진다.(고차 함수) 

> **함수와 메소드 차이**  
> 함수(function) : class 밖에서 작성하는 함수. 어디에서나 호출 가능.  
> 메소드(method) : class 내부에 작성하는 함수. 정의된 class에 관계된 기능을 수행. Static이 붙은 method는 정적 메서드가 되어 최상위 함수처럼 사용 가능.  

#### 익명함수와 화살표함수(람다식) ####
**(인수형식){동작}** 의 패턴으로 구성된다. 변수에 할당하여 사용할 수 있다.
<script src="https://gist.github.com/pausacoffee/b2ffd58a945a9465660eb1837fa37843.js"></script>
#### 매개변수 ####
다트 함수는 위치 지정, 이름 지정, 선택형 위치 지정, 선택형 이름 지정 파라미터와 이 모두를 조합한 파라미터 등 다양한 파라미터를 지원한다.
<script src="https://gist.github.com/pausacoffee/63939b9749f9ad4a9f007e63d49c198a.js"></script>

## Class ##
객체 object : 저장 공간에 할당되어 값을 가지거나 식별자에 의해 참조되는 공간. (변수, 함수, 메서드)  
인스턴스 instance : 객체를 메모리에 작성하는 것.  
클래스 class : 인스턴스의 설계도.   
속성 property : 클래스 안에 표현되는 속성.  
  
클래스는 일종의 사용자 정의 타입이라 볼 수 있다.

> **new 키워드를 사용하지 않음!**  
> 다른 객체지향 언어에서는 new라는 키워드로 클래스의 인스턴스를 만든다. 다트에서도 new 키워드를 사용할 수 있지만, 선택사항이다.  
> 컴파일러가 자동으로 알맞은 키워드를 추론하기 때문이다. 다만, dart에서는 new사용을 권장하지 않는다.

#### 생성자 with getter, setter ####
<script src="https://gist.github.com/pausacoffee/35293245ca222ebb167e7d5f1c8517f8.js"></script>

#### 상속과 추상클래스####
#### 널인지 연산자 ####
#### 믹스인 ####
#### enum ####
#### method ####
  
## Collection ##
#### List ####
#### Spread ####
#### Map ####
#### Set ####
