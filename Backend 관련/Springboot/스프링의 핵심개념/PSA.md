# Portable Service Abstraction : 이식 가능한 서비스 추상화
환경의 변화나 관계없이 일관된 방식의 기술로의 접근 환경을 제공하는 추상화 구조. 스프링의 중요 컨셉중 하나이다.
스프링에서 제공하는 다양한 기술들을 잘 추상화 해뒀기 때분에 개발자가 인터ㅔ이스를 쉽게 이용하고 구현 가능

## 예시
- 데이터베이스에 접근하기 위한 기술로는 JPA, MyBatis, JDBC 등이 있는데, 이 중 어떤 기술을 사용하든 일관된 방식으로 데이터베이스에 접근하도록 인터페이스를 지원한다.
- WAS도 PSA의 예시 중 하나라고 볼 수 있는데, 코드는 그대로 두고 WAS를 톰캣이 아닌 다른 곳에서 실행해도 기존 코드를 그대로 사용 가능. 원래 스프링은 톰캣 기반이지만, dependencies에서 web을 webflux로 바꾸고 다시 실행해보면 NETTY 기반으로 돌아간다.
- 스프링의 PSA덕분에 코드를 거의 바꾸지 않고도 톰캣이 아닌 완전히 다른 기술로 실행이 가능하다는 의미이다.
