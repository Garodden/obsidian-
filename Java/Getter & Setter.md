객체지향 프로그래밍에서 일반적으로 객체의 데이터는 객체 외부에서 직접적으로 접근하는 것을 막는다.
객체의 외부에서 데이터를 마음대로 읽어들이고 수정하면 객체의 무결성이 깨질 수 있기 때문.

# 그래서 getter와 setter를 통해서만 필드값을 열람, 수정 가능하도록 한다.

## Setter
```java
public class Car {
		private int speed;
		
		public void setSpeed(int speed) {
				if (speed < 0) {
						this.speed = 0;
						return;
				} else {
						this.speed = speed;
				}
		}
}
```
이런식으로 규격을 벗어나는 필드의 데이터 수정을 막아주기 위해 setter 클래스를 사용해서 필드 값을 수정하도록 한다.

## 근데 setter 메소드 사용은 특정 상황에서 지양해야함.
- 값을 변경한 의도를 파악하기 힘들다.
- 객체의 일관성을 유지하기 어렵다.
라는 이유 때문에
- setter를 사용하면 어디서든지 객체의 필드값을 변경할 수 있게 된다. 이건 좋지 못함. 객체의 일관성을 유지하기가 매우 어려워짐.
1. 불변 객체일때
2. 캡슐화 위반일 때
3. 여러 속성 값이 상호의존적일 대 개별 속성을 설정하는 setter 메소드를 사용하면 일관성이 깨질 수 있다.
4. 객체의 상태 변경이 복잡한 비즈니스 로직에 의존하는 경우에는 옳지 않음(3번과 비슷한 이유에서)

## 그래서 뭘 써야 하는데?
### 생성자를 오버로딩
- 생성자를 오버로딩해 처음부터 필드값을 전부 로직에 맞게 정해준다
### 빌더 패턴 사용
- 생성자가 너무 많은 경우에는 빌더패턴을 사용해서 생성한다
### 정적 팩토리 메소드
- 인스턴스의 생성만을 목적으로 하는 정적 팩토리 메소드를 만든다
### 도메인 이벤트
- 객체 상태(필드) 변경이 비즈니스 로직에 따라 이루어져야 하는 경우, 도메인 이벤트를 사용하여 상태 변경을 관리한다.
	- 상태를 바꿀때 연관 있는 상태들도 다 바꿔주는 도메인 이벤트 메소드를 만들어 주는 것이다.
