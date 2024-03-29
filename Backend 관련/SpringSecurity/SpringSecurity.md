# SpringSecurity?
스프링 기반으 애플리케이션에서 보안을 담당하는 스프링의 하위 프레임워크이다.
인증, 권한 부여, 접근 제어, 암호화, 세션관리 등 다양한 보안 기능을 제공한다.

- 스프링 시큐리티는 스프링 기반 보안 옵션을 제공하고 어노테이션으로 설정도 쉽게할 수 있다.
- CSRF 공격, 세션고정공격을 방어해주고, 요청 헤더도 보안 처리를 해주므로 개발자가 보안 관련 개발을 해야 하는 부담을 줄여준다.
	- **CSRF 공격**: 사용자의 권한을 가지고 특정 동작을 수행하도록 유도하는 공격
	- **세션 고정(session fixation) 공격**: 사용자의 인증 정보를 탈취하거나 변조하는 공격


# 인증(Authentication) & 인가(Authrization)
인증: **사용자의 신원을 확인**하는 과정이다.
인가: 인증과는 또 다른 개념이다. 인가는 사이트의 **접근을 제어**하는 과정이다.

인증과 인가 관련 커드를 직접 구현하기 위해서는 너무 번거롭기에, 스프링 시큐리티를 활용해서 쉽게 처리할 수 있다.

