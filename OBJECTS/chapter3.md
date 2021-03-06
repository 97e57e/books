# 3. 역할, 책임, 협력

## 객체지향 패러다임의 관점에서 핵심은 **역할(role)**, **책임(responsibility)**, **협력(collaboration)** 이다.
애플리케이션의 기능을 구현하기 위해 어떤 협력이 필요하고 협력을 위해 어떤 역할과 책임이 필요한지를 고민하지 않은 채 너무 이른 시기에 구현에 초점을 맞추는 것은 변경하기 어렵고 유연하지 못한 코드를 낳는 원인이 된다.

<br>

## 협력
**애플리케이션의 기능을 구현하기 위해 수행하는 상호작용을 협력이라고 한다.**

<br>

메시지 전송은 객체 사이의 협력을 위해 사용할 수 있는 유일한 커뮤니케이션 수단이다.<br>
메세지를 수신한 객체는 메서드를 실행해 요청에 응답한다.

<br>

객체를 자율적으로 만드는 가장 기본적인 방법은 내부 구현을 **캡슐화**하는 것이다.<br>
캡슐화를 통해 변경에 대한 파급효과를 제한할 수 있기 때문에 자율적인 객체는 변경하기도 쉬워진다.

<br>

## 책임
**책임이란 객체에 의해 정의되는 응집도 있는 행위의 집합으로, 객체가 유지해야 하는 정보와 수행 할 수 있는 행동에 대해 서술한 문장이다.**

<br>

객체지향 개발에서 가장 중요한 능력은 책임을 능숙하게 소프트웨어 객체에 할당하는것

<br>

객체에게 책임을 할당하기 위해서는 먼저 협력이라는 문맥을 정의해야 한다.<br>
협력을 설계하면서 객체의 책임을 식별해 나가는 과정에서 최종적으로 시스템을 구성하는 객체들의 인터페이스와 오퍼레이션 목록을 얻는다.

<br>

책임을 수행할 적절한 객체를 찾아 책임을 할당하는 방식으로 협력을 설계하는 방법을 **책임 주도 설계** 라고 한다.

<br>

## 역할
**객체가 어떤 특정한 협력 안에서 수행하는 책임의 집합을 역할이라고 부른다.**

<br>

역할은 여러 종류의 구체적인 객체를 포괄하는 추상화라고 할 수 있다.<br>
역할을 이용하면 불필요한 중복 코드를 제거할 수 있다.

<br>

협력을 구체적인 객체가 아니라 추상적인 역할의 관점에서 설계하면 협력이 유연하고 재사용 가능해진다. **(역할 모델링)**