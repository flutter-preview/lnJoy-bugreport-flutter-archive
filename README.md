## 클래스
객체의 대한 속성과 기능을 모아둔 것, 인스턴스는 클래스를 기반으로 생성하게 됨
- 객체 - 클래스가 정의 된 후 메모리에 할당 되었을 때 ( 변수, 함수 등 )
- 인스턴스 - 클래스를 기반으로 생성되게 되며, 객체를 메모리에 작성하여 사용할 수 있을 때

예제코드
```dart
class Person {
	String name = ‘John’;
	int age;
}
```


## 생성자
인스턴스가 생성될 때 호출되며, 객체의 속성 또는 기능을 입력할 수 있음
- 전달인자 - 생성자를 생성할 때 초기화할 값을 입력받는 역할
- this - 전달인자와 멤버변수를 구분할 수 있도록 알려주는 역할
- new - 메모리 공간을 할당해주고 주소를 반환한 후 생성자를 실행시켜주는 역할 (생략 가능)

예제코드 (기본 생성자)
```dart
class Person {
	String name;
	int age;

	Person(String name, int age) {
		this.name = name;
		this.age = age;
	}
}

void main() {
	Person p1 = new Person(‘John’, 20);

	print(p1.name, p1.age);
}
```

예제코드 (이름 있는 생성자)
>전달인자의 데이터 입력이 필수가 아닌 선택이 되며, 전달인자의 값을 입력하기 위해 `name: value` 와 같이 입력해야 한다.
```dart
class Person {
	String name;
	int age;

	Person({String name, int age}) {
		this.name = name;
		this.age = age;
	}
}

void main() {
	Person p1 = new Person(name: ‘John’, age: 20);

	print(p1.name, p1.age);
}
```