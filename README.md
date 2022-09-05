![이벤터스-배너](https://user-images.githubusercontent.com/112323612/187632301-327e3b0f-8202-4533-90bc-9e729499a73b.png)


# Workshop Objectives
악성코드탐지 플랫폼 SonaType Nexus Firewall (IQ Server) 을 이용하여, SDLC 내에 위협요소가 유입되는 것을 방지할 수 있도록 Nexus Repository와 Nexus Firewall을 통한 실습을 수행합니다. 가장 많이 사용하는 NPM, MAVEN, PYPI를 통해서 위협요소를 평가 실습하며, 주어진 미션을 완성함을 목적으로 합니다.

Nexus Firewall is Sonatype unique offering in the market that not only protect you against open source vulnerability (phase 1 attack) during download, it is also the only product in the market that prevents phase 2 attacks (malicious packages, typo squatting, dependency confusion”

# 환경정보
**Nexus Repository 시스템**

https://nexus-workshop.openmsa.cloud:8443/


접속 계정정보는 참가 신청시 기재한 연락처로 문자 발송됩니다. 

문자를 받지 못한 분은 marketing@osckorea.com 으로 성함과 연락처, 내용을 보내주세요. 빠르게 조치해드리겠습니다. 

# Mission #1
**9월 1일 12:00 (정오/한국시간) ~ 9월 4일 (정오/한국시간)**

가장 많이 사용하는 패키지 관리 툴을 설치하고, Public Repository를 사용하지 않고도 Nexus Repository를 통한 컴포넌트/디펜더시 다운로드할 수 있도록 환경 설정.


개인별 3개의 Repository (Individually allocated repository) 가 제공되므로, 아래 내용을 참고해서 본인의 환경에 맞게 설정합니다.
(참조용이며, 이미 각 환경에 맞게 설정이 되어 있다면 개인 환경에서 Proxy 설정만 진행하면 됩니다.)

## Quest

**총 5개 질문에 대한 답을 메일로 (marketing@osckorea.com) 보내주세요.** 


1. 문자 메세지로 안내된 계정 정보를 확인하여 시스템에 접속하세요.



2. 할당된 총 Repository 를 확인, Repository 이름을 모두 기술해 보세요



3. 각 언어에 할당된 (maven, npm, pypi) common Repository의 Health Check 항목과 View Detail을 통해서 Artifact 관련 정보를 확인하여 각 언어별로 아래 표의 빈칸을 채워보세요. 


언어 | Artifact 의 총수 | Security 취약성 갯수 | Threat Level 9 이상의 CVE 코드 | Component
---|:---:|---:|---:|---:
**pypi** | &#160;&#160;&#160; | &#160;&#160;&#160; | &#160;&#160;&#160; | &#160;&#160;&#160; | 
**maven** | &#160;&#160;&#160; | &#160;&#160;&#160; | &#160;&#160;&#160; | &#160;&#160;&#160; | 

언어 | Artifact 의 총수 | License(Critical) Copyleft 갯수 | Component
---|:---:|---:|---:
**NPM**  | &#160;&#160;&#160; | &#160;&#160;&#160; | &#160;&#160;&#160; | 



4. Python Repository 에 저장된 django 컴포넌트 버전은 얼마인가요?



5. 할당된 개인 Repository (3개)에 하나 이상의 Component/Dependencies를 적재한 뒤, 스크린 캡처하여 메일 본문에 첨부해주세요. 




- [1. NPM 환경 설정](01.NPM.md)
- [2. MAVEN 환경 설정](02.MAVEN.md)
- [3. PYTHON 환경 설정](03.PYTHON.md)

# Mission #2
**9월 5일 12:00 (정오/한국시간) ~ 9월 8일 (정오/한국시간)**

## Quest

**1번 NPM, 2번 Maven, 3번 PiPy 중 희망하는 언어를 골라 질문에 대한 답을 메일로 (marketing@osckorea.com) 보내주세요.** <br/><br/><br/>

  * **[NPM]** :  NPM Malicious 패키지 설치하고, IQ Server 를 접속해서, 아래 질의에 답변하세요.
   
        npm install @sonatype/policy-demo

    
   (NPM-1) Problem Code 는 무엇인가요?
   
   (NPM-2) Threat Level (위협도)는 얼마인가요?<br/><br/><br/>
    
    
  * **[Maven]** : Sample Maven build 후 보안관련 상황을 살펴보고 IQ Server 를 접속해서, 아래 질의에 답변하세요. 
  
        mvn install
    
   (Maven-1) 총 Component 의 수는?
   
   (Maven-2) Security-Critical 정책 위협에 Detected 된 Components 의 수는?<br/><br/><br/>
   
   
  * **[PiPy]** : PYPI Malicious 패키지 설치하고, IQ Server 를 접속해서, 아래 질의에 답변하세요. 
   
        pip install Django
   
   (PiPy-1) Threat Level (위협도)는 얼마인가요?
   
   (PiPy-2) 실제 격리를 일으키는 정책(Policy)이름은 무엇인가요?
   

# Mission #3
9월 13일 ~ 9월 16일

# 리뷰
9월 19일 ~ 20일
