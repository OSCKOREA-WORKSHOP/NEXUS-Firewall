## Workshop Objectives
악성코드탐지 플랫폼 SonaType Nexus Firewall (IQ Server) 를 이용하여, SDLC 내에 위협요소가 유입되는 것을 방지할 수 있도록 Nexus Repository와 Nexus Firewall을 통한 실습을 수행합니다. 가장 많이 사용하는 NPM, MAVEN, PYPI를 통해서 위협요소를 평가 실습하며, 주어진 미션을 완성함을 목적으로 합니다.

Nexus Firewall is Sonatype unique offering in the market that not only protect you against open source vulnerability (phase 1 attack) during download, it is also the only product in the market that prevents phase 2 attacks (malicious packages, typo squatting, dependency confusion”

## 환경정보
Nexus Repository 시스템

https://nexus-workshop.openmsa.cloud:8443/

IQ Server(Nexus Firewall) 시스템

http://iq-workshop.openmsa.cloud:8070


접속 계정정보는 개인 이메일을 통해서 별도로 전달될 예정입니다.

## Mission 1
9월 1일 ~ 9월 4일

가장 많이 사용하는 패키지 관리 툴을 설치하고, Public Repository를 사용하지 않고도 Nexus Repository를 통한 컴포넌트/디펜더시 다운로드할 수 있도록 환경 설정.
개인별 3개의 Repository (Individually allocated repository) 가 제공되므로, 아래 내용을 참고해서 본인의 환경에 맞게 설정합니다.
(참조용이며, 이미 각 환경에 맞게 설정이 되어 있다면 개인 환경에서 Proxy 설정만 진행하면 됩니다.)

### Question

1. NPM Repository Manager 를 주어진 계정을 가지고 접속

2. 할당된 총 Repository 를 확인, Repository 이름을 모두 기술해 보세요

3. 각 언어에 할당된 (maven, npm, pypi) common Repository 에 Health Check 항목하고, View Detail 를 통해서 Artifact 관련 정보를 확인해 보세요.

4. Python Repository 에 저장된 django 컴포넌트 버전은 얼마인가요?

5. 할당된 개인 Repository (3개) 적어도 하나의 Component/Dependencies를 적재해 보세요



- [1. NPM 환경 설정](01.NPM.md)
- [2. MAVEN 환경 설정](02.MAVEN.md)
- [3. PYTHON 환경 설정](03.PYTHON.md)

## Mission 2
9월 5일 ~ 9월 8일

## Mission 3
9월 13일 ~ 9월 16일

## 리뷰
9월 19일 ~ 20일
