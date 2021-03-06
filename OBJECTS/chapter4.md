# 4. 설계 품질과 트레이드오프

책임은 객체의 상태에서 행동으로, 나아가 객체와 객체 사이의 상호작용으로 설계 중심을 이동시키고, 결합도가 낮고 응집도가 높으며 구현을 효과적으로 캡슐화하는 객체들을 창조할 수 있는 기반을 제공한다.

<br>

객체를 단순한 데이터의 집합으로 바라보는 시각은 객체의 내부 구현을 퍼블릭 인터페이스에 노출시키는 결과를 낳기 때문에 결과적으로 설계가 변경에 취약해진다. 이런 문제를 피할 수 있는 가장 좋은 방법은 객체의 책임에 초점을 맞추는 것이다.

<br>

**객체의 상태는 구현에 속한다.** 구현은 불안정하기 때문에 변하기 쉽다. 상태를 객체 분할의 중심축으로 삼으면 구현에 관한 세부사항이 객체의 인터페이스에 스며들게 되어 캡슐화의 원칙이 무너진다.<br>
결과적으로 상태 변경은 인터페이스의 변경을 초래하며 이 인터페이스에 의존하는 모든 객체에게 변경의 영향이 퍼지게 된다. 따라서 데이터에 초점을 맞추는 설계는 변경에 취약할 수밖에 없다.

<br>

## 캡슐화
한곳에서 일어난 변경이 전체 시스템에 영향을 끼치지 않도록 적절하게 조절할 수 있는 장치로 **캡술화**를 사용한다.<br>
변경될 가능성이 높은 부분을 **구현**이라고 부르고 상대적으로 안정적인 부분은 **인터페이스**라고 부른다.

<br>

설계가 필요한 이유는 요구사항이 변경되기 때문이고, 캡슐화가 중요한 이유는 불안정한 부분과 안정적인 부분을 분리해서 변경의 영향을 통제할 수 있기 떄문이다.

<br>

## 응집도와 결합도
**응집도**는 모듈에 포함된 내부 요소들이 연관돼 있는 정도를 나타낸다. 모듈 내의 요소들이 하나의 목적을 위해 긴밀하게 협력한다면 그 모듈은 높은 응집도를 가진다.<br>
응집도는 객체 또는 클래스에 얼마나 관련 높은 책임들을 할당했는지를 나타낸다.

<br>

**결합도**는 의존성 정도를 나타내며 다른 모듈에 대해 얼마나 많은 지식을 갖고 있는지를 나타내는 척도다.<br>
결합도는 객체 또는 클래스가 협력에 필요한 적절한 수준의 관계만을 유지하고 있는지를 나타낸다.

<br>

**좋은 설계란 오늘의 기능을 수행하면서 내일의 변경을 수용할 수 있는 설계다.**

<br>

변경의 관점에서 응집도란 **변경이 발생할 때 모듈 내부에서 발생하는 변경의 정도**로 측정할 수 있다.

<br>

변경의 관점에서 결합도란 **한 모듈이 변경되기 위해서 다른 모듈의 변경을 요구하는 정도**로 측정할 수 있다.

<br>

**단일 책임 원칙 :** 클래스는 단 한 가지의 변경 이유만 가져야 한다. 

<br>

### 데이터 중심 설계의 문제점
데이터 중심의 설계는 본질적으로 너무 이른 시기에 데이터에 관해 결정하도록 강요한다.<br>
데이터 중심의 설계에서는 협력이라는 문맥을 고려하지 않고 객체를 고립시킨 채 오퍼레이션을 결정한다.