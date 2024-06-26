## 자동으로 소프트웨어를 빌드, 테스트, 배포하는 개념
- 소프트웨어를 사용자에게 신속하고 안정적으로 코드를 배포하기 위해 자동으로 소프트웨어를 빌드, 테스트, 배포하는 개념이다.
# CI (Continuous Integration)
**지속적인 통합 개발자를 위한 자동화 프로세스라고 볼 수 있으며, code - build - test 단계에서 이 프로세스를 실행** 
- Code : 개발자가 코드를 원격 코드 저장소에 push 하는 단계
- Build : 원격 코드 저장소로부터 코드를 가져와 컴파일, 빌드 하는 단계.
- Test: 단위(unit) 테스트를 수행했을 때 실패하는 케이스가 없는지 수행하는 단계. 보통 빌드 과정에서 함께 자동으로 테스트 코드를 실행
이 과정에서 개발자는
- 코드를 원격 코드 저장소에 자주 push하고 
- 개발자가 push한 코드를 자동으로 test, build하도록 트리거를 걸어놓음
- 테스트 및 빌드를 하며 빌드 결과를 통해 빌드가 성공했는지 실패했는지 확인
- 그 후 통합 테스트 결과를 통해 개선 방안을 찾는다
이 CI 과정을 통해 개발자는 버그를 일찍 발견하고, 테스트가 완료된 코드에 대해 빠른 전달이 가능해지며 지속적인 배포가 가능해진다.

CI는 모든 코드 별화를 하나의 repository에서 관리하는 것 부터 시작. 모든 개발팀이 코드의 변화를 확인할 수 있기 때문에, 투명하게 문제점을 파악할 수 있고 잦은 PR과 merge로 코드를 자주 통합.
이 때 기본적인 테스트도 작동 가능. 이를 통해 각자 개발한 코드를 이른 시점에 자주 합치고 자주 테스트를 가능하다
## 소프트웨어 배포?
소프트웨어를 고객이 사용할 수 있도록 제공해주는 것. 개발자가 코드 작업을 한 후 고객에게 버그 없는 소프트웨어를 제공하기 위하여 테스트를 하고, 테스트를 통한 기능 검증이 끝나면 배포를 하게 됨.
	1. 개발자 코드 작업
	2. 소프트웨어 테스트 및 기능 검증
	3. 소프트웨어 배포
 ![[Pasted image 20240419110139.png]]
# CD(Continuous Delivery)
- 지속적인 배포 = 지속적인 서비스 제공을 의미한다
- 소프트웨어 개발이 끝난 후 가능한 빠르게 고객에게 배포하는 과정을 ==자동화==하고 ==간소화== 하는것을 목표로 함
## 배포 자동화
- 커맨드 하나로 전체 배포 과정을 자동으로 진행시키는 것
- 잘 구축해놓으면 수동적이고 반복적인 배포 과정을 자동화함으로써 시간을 절약할 수 있다.
- 개발자의 human error를 방지 가능
# CI/CD와 GitHub Actions
특정 이벤트가 발생했을 때 개발자가 정의해놓은 workflow를 자동으로 실행시켜준다.
이런 흐름을 이용하여 개발자는 GitHubActions를 사용하여 CI/CD 환경을 구축 가능.
![[Pasted image 20240419110914.png]]