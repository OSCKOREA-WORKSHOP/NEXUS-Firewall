![이벤터스-배너](https://user-images.githubusercontent.com/112323612/187632301-327e3b0f-8202-4533-90bc-9e729499a73b.png)


# Workshop Objectives
악성코드탐지 플랫폼 SonaType Nexus Firewall (IQ Server) 을 이용하여, SDLC 내에 위협요소가 유입되는 것을 방지할 수 있도록 Nexus Repository와 Nexus Firewall을 통한 실습을 수행합니다. 가장 많이 사용하는 NPM, MAVEN, PYPI를 통해서 위협요소를 평가 실습하며, 주어진 미션을 완성함을 목적으로 합니다.

Nexus Firewall is Sonatype unique offering in the market that not only protect you against open source vulnerability (phase 1 attack) during download, it is also the only product in the market that prevents phase 2 attacks (malicious packages, typo squatting, dependency confusion”<br/><br/><br/><br/>

# 환경정보
**Nexus Repository 시스템**

https://nexus-workshop.openmsa.cloud:8443/

IQ Server 접속
http://iq-workshop.openmsa.cloud:8070

:mega: 접속 계정정보는 참가 신청시 기재한 연락처로 문자 발송됩니다. 

문자를 받지 못한 분은 marketing@osckorea.com 으로 성함과 연락처, 내용을 보내주세요. 빠르게 조치해드리겠습니다. <br/><br/><br/><br/>

# Mission #1
**9월 1일 12:00 (정오/한국시간) ~ 9월 4일 (정오/한국시간)**

가장 많이 사용하는 패키지 관리 툴을 설치하고, Public Repository를 사용하지 않고도 Nexus Repository를 통한 컴포넌트/디펜더시 다운로드할 수 있도록 환경 설정.


개인별 3개의 Repository (Individually allocated repository) 가 제공되므로, 아래 내용을 참고해서 본인의 환경에 맞게 설정합니다.
(참조용이며, 이미 각 환경에 맞게 설정이 되어 있다면 개인 환경에서 Proxy 설정만 진행하면 됩니다.)

## Quest

:mega: **총 5개 질문에 대한 답을 메일로 (marketing@osckorea.com) 보내주세요.** 


1. 문자 메세지로 안내된 계정 정보를 확인하여 시스템에 접속하세요.<br/><br/>

_성공적인 로그인_<br/><br/>

2. 할당된 총 Repository 를 확인, Repository 이름을 모두 기술해 보세요<br/><br/>

_common-maven-proxy, common-npm-proxy, common-pypi-proxy_
_{username}-maven-proxy, {username}-npm-propxy, {username}-pypi-proxy_<br/><br/>

3. 각 언어에 할당된 (maven, npm, pypi) common Repository의 Health Check 항목과 View Detail을 통해서 Artifact 관련 정보를 확인하여 각 언어별로 아래 표의 빈칸을 채워보세요.<br/><br/> 


언어 | Artifact 의 총수 | Security 취약성 갯수 | Threat Level 9 이상의 CVE 코드 | Component
---|:---:|:---:|:---:|:---:
**pypi** | _1_ | _1_ | _CVE-2022-34265_ | _Django_ | 

언어 | Artifact 의 총수 | Security 취약성 갯수 | Threat Level 9 이상의 CVE 코드 | Component
---|:---:|:---:|:---:|:---:
**maven** | _84_ | _3_ | _CVE-2021-44228, CVE-2021-45046, CVE-2016-1000027_ | _org.apache.logging.log4j, org.apache.logging.log4j, org.springframework_ | 

언어 | Artifact 의 총수 | License(Critical) Copyleft 갯수 | Component
---|:---:|:---:|:---:
**NPM**  | _238_ | _2_ | _@pm2/agent, pm2_ | 

<br/>

4. Python Repository 에 저장된 django 컴포넌트 버전은 얼마인가요? <br/><br/>
_4.1_ <br/><br/>

5. 할당된 개인 Repository (3개)에 하나 이상의 Component/Dependencies를 적재한 뒤, 스크린 캡처하여 메일 본문에 첨부해주세요. <br/><br/>

_(스크린 캡처 이미지 메일 첨부)_ <br/><br/>

- [1. NPM 환경 설정](01.NPM.md)
- [2. MAVEN 환경 설정](02.MAVEN.md)
- [3. PYTHON 환경 설정](03.PYTHON.md)<br/><br/><br/><br/>

# Mission #2
**9월 5일 12:00 (정오/한국시간) ~ 9월 8일 (정오/한국시간)**

- [1. NPM 환경 설정 가이드](Mission2.NPM.md)
- [2. PYTHON 환경 설정 가이드](Mission2.PYTHON.md)

## Quest

:mega: **1번 NPM, 2번 Maven, 3번 PiPy 중 희망하는 언어를 골라 질문에 대한 답을 메일로 (marketing@osckorea.com) 보내주세요.** <br/><br/><br/>

  * **[NPM]** :  NPM Malicious 패키지 설치하고, IQ Server 를 접속해서, 아래 질의에 답변하세요.
   
        npm install @sonatype/policy-demo

    
   (NPM-1) Problem Code 는 무엇인가요?   _SONATYPE-2022-0705_
   
   (NPM-2) Threat Level (위협도)는 얼마인가요?   _10_
   
   (NPM-3) 실제 격리를 일으키는 정책(Policy)이름은 무엇인가요?   _Security-Malicious_ <br/><br/><br/>
    
    
  * **[Maven]** : Sample Maven build 후 보안관련 상황을 살펴보고 IQ Server 를 접속해서, 아래 질의에 답변하세요. 
  
        mvn install
    
   (Maven-1) 총 Component 의 수는?   _219_
   
   (Maven-2) Security-Critical 정책 위협에 Detected 된 Components 의 수는?   _13_
   
   (Maven-3) maven-compat:3.0 컴포넌트 현재 버전과, 보안 문제를 일으키는 않는 권고되는 버전은?   _현재 버전 3.0, 권고 버전 3.8.1 _ <br/><br/><br/>
   
   
  * **[PiPy]** : PYPI Malicious 패키지 설치하고, IQ Server 를 접속해서, 아래 질의에 답변하세요. 
   
        pip install Django
   
   (PiPy-1) Threat Level (위협도)는 얼마인가요?   _10_
   
   (PiPy-2) 실제 격리를 일으키는 정책(Policy)이름은 무엇인가요?   _pypi-django-policy & Security Critial_ <br/><br/><br/><br/>
   

# Mission #3
**9월 13일 12:00 (정오/한국시간) ~ 9월 16일 12:00 (정오/한국시간)**

## Quest

:mega: 미션을 수행한 뒤 **결과 화면을 스크린 캡쳐하여** marketing@osckorea.com으로 보내주세요<br/><br/>

mission#2 에서의 Malicious 패키지들은 IQ Server 정책에 의해 다운로드가 막혀 있는 상태입니다. 하지만 필요에 의해 일정 기간 불가피하게 사용해야 하는 패키지가 있거나, 아직 보안 패치가 나오지 않은 컴포넌트들도 존재합니다. 이때 보안팀과의 검토를 통해 유예(Waive) 설정을 할 수 있습니다. <br/><br/>

**IQ Server에 접속하여 Malicious 패키지들을 유예(Waive) 설정하세요.**

:warning:IQ Server 접속해서 Waive 를 할 경우 반드시 본인의 Repository 에만 적용해야 합니다.:warning:<br/>

![3d7bc9d9-850f-40e6-9647-65fd6b7f47cc](https://user-images.githubusercontent.com/112323612/189791054-5bd4bf18-137f-4608-8225-30334fa1f85f.png) <br/><br/>

유예 설정 화면이 아닌, <U>유예 설정을 한 뒤의 결과 화면을 스크린 캡쳐</U>하여 정답 제출해주세요. <br/><br/><br/><br/>

# Review event
**9월 16일 12:00 (정오/한국시간) ~ 9월 20일 12:00 (정오/한국시간)**

:mega: Nexus Firewall 사용 후기를 SNS에 작성하고 포스트 URL을 marketing@osckorea.com으로 보내주세요<br/><br/>

Sonatype Nexus Firewall을 사용하면서 어떤 점이 좋으셨나요? 

몰랐던 것을 알게 된 것은 무엇이 있나요?

오픈소스 소프트웨어 보안에 대한 생각은 어떻게 변화하였나요? 

Nexus Firewall의 장점, Trial을 사용하면서 느낀점 등 어떤 내용이든 좋아요!

이번 **행사에 참여한 후기를 개인 SNS (페이스북, 블로그, 링크드인 등)에 작성하고 게시물 URL을 보내주세요!**


