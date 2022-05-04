---
layout: post
title: Dart 의 기초
subtitle: Let's study basic dart lan for flutter!
categories: Flutter
tags: [Flutter, Dart, Mac, VSCode]
---
## Overview ##
flutter는 dart기반의 크로스플랫폼 **프레임워크**이다. 고로 flutter를 사용하기에 앞서 dart에 대해 공부하고자 한다.  
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
#### 변수, 상수 ####
int, double, String, bool 을 기본적으로 제공한다.  

>**final과 const차이**  
>final은 컴파일 이후 한번만 값을 할당 가능.
>const는 컴파일 이후 항상 같은 값을 가짐.
>static은 클래스에서만 사용되며, 스코프를 글로벌로 넓혀준다. 클래스로 직접 접근해 호출이 가능하다.

<script src="https://gist.github.com/pausacoffee/8792186514b2cc332c165745e1722f4c.js"></script> 
#### enum ####
상수를 정의하는 특수한 형태의 클래스. 상수처럼 사용이 가능하다.
<script src="https://gist.github.com/pausacoffee/3d24cb2df949707d48c106a0a46aa0ea.js"></script>
#### 연산자 ####
<script src="https://gist.github.com/pausacoffee/994680d065decee91216dd2c00eca45d.js"></script>
#### 널인지 연산자 ####
어떤 객체든 null이 될수 있는 문제가 발생한다. (예를 들어 비동기 호출함수의 리턴이 null인 케이스)  
이때 if(response == null) return 과 같은 예외처리 코드를 추가해야 한다.  
dart에서는 이를 널인지 연산자를 통해 해결한다.

>**?. ?? ?? 의 차이**  
>?. null이 아니면 값을 할당하고, null이면 오류 발생없이 null을 할당하시오!  
>?? 정보가 있는지 알수 없는 상황에서 '값이 존재하지 않는 상황'에 할당할 백업값을 저장할수 있다.  
>??= 이전 연산자(??)과 비슷하지만 반대의 작업을 수행한다. 객체가 null이면 백업값을 할당하고 아니면 객체를 그대로 반환한다.  
>* [이 곳](http://blog.sethladd.com/2015/07/null-aware-operators-in-dart.html)에서 더 자세히 알아보자  
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

#### 익명함수와 람다식 ####
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

#### 생성자, getter, setter ####
<script src="https://gist.github.com/pausacoffee/35293245ca222ebb167e7d5f1c8517f8.js"></script>

#### 상속, 추상클래스, 믹스인, 팩토리 ####

> **extends, implements, mixins 의 차이**. 
> extends : 클래스의 멤버변수, 함수, 생성자 등을 구현없이 사용할때 사용  
> implements : 클래스의 멤버변수, 함수, 생성자 등의 구현이 필수적  
> mixins : 다양한 계층의 클래스에서 클래스의 코드를 재사용  
ex) 동물 클래스의 까마귀 물고기 호랑이 클래스가 있다고 하면 각각 날고 걷고 수영하는 행동(메소드)를 가지는데 이러한 동일한 메소드들을 재사용 하기 위해 사용한다.
> factory : 미리 정해진 프로퍼티를 포함하는 클래스의 특별한 메서드이다.  

<script src="https://gist.github.com/pausacoffee/7e04ec0c7bb400ff1e978557ff8f416e.js"></script>. 

  
## Collection ##
#### List, Spread, Map, Set ####
<script src="https://gist.github.com/pausacoffee/eede03526cf9adb752966297fabf0138.js"></script>
#### 기타 ####
<script src="https://gist.github.com/pausacoffee/c7a70f39d5b5ed9a210091aba17577e2.js"></script>. 
## 함수형 프로그래밍 ##
Dart는 객체지향 프로그래밍과 함수형 프로그래밍의 특징을 모두 제공한다.  
함수를 값으로 취급하여 다른 변수에 함수를 대입할 수 있다.
다른 함수의 인수로 함수 자체를 전달하거나 함수를 반환받을 수도 있다.

> 함수를 매개변수로 전달, 수정, 변수에 대입하기가 가능한 객체를 '일급 객체', first-class object라고 함.

루프에서 살펴본 forEach가 함수형 프로그래밍이다.  
이터레이션 프로토콜을 지원하는 자료구조하면 모두 forEach를 사용할 수 있다.  

forEach외의 고차함수를 살펴보자.
<script src="https://gist.github.com/pausacoffee/a60902d8c1233a08eb41a230430ebb52.js"></script>
