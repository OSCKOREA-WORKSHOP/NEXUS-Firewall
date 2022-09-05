
* * *

Mission2 목표!
============

*   Python에서 사용되는 웹프레임워크 **Django 모듈을 다운로드** 진행
    
*   Django 모듈 **IQServer에 의해서 격리 되는지 확인**!
    
*   IQServer 접속 하여 취약성 **Report를 확인하고 미션을 확인**하자!
    

1\. Django 모듈 제거 및 Local Clean
==============================

아래 명령으로 설치되어 있는 Django 모듈 제거

```java
# pip uninstall django
```

Cache 디렉토리 확인을 진행합니다.

```java
# pip cache dir
---
c:\users\user\appdata\local\pip\cache
```

**위에서 발견한 cache 디렉토리를 삭제합니다.**

2\. Nexus repository Clean
==========================

**정책을 반영하고자 하는 Module(Django)를 Nexus Repository에서 삭제합니다.**

![](attachments/654868581/654803080.png)

3\. Pip install Django 격리 확인
============================

이제 아래와 같이 pip install 을 진행했을때 IQ-server에 의해서 격리가 되는지 확인합니다.

```java
$ pip install Django
---
Looking in indexes: https://MjAsEPkH:****@nexus-workshop.openmsa.cloud:8443/repository/thomas-pypi-proxy/simple
Collecting Django
ERROR: HTTP error 403 while getting https://nexus-workshop.openmsa.cloud:8443/repository/thomas-pypi-proxy/packages/django/4.1/Django-4.1-py3-none-any.whl#sha256=031ccb717782f6af83a0063a1957686e87cb4581ea61b47b3e9addf60687989a (from https://nexus-workshop.openmsa.cloud:8443/repository/thomas-pypi-proxy/simple/django/) (requires-python:>=3.8)
ERROR: Could not install requirement Django from https://nexus-workshop.openmsa.cloud:8443/repository/thomas-pypi-proxy/packages/django/4.1/Django-4.1-py3-none-any.whl#sha256=031ccb717782f6af83a0063a1957686e87cb4581ea61b47b3e9addf60687989a because of HTTP error 403 Client Error: -------------------->>> REQUESTED ITEM IS QUARANTINED -------------------->>> FOR DETAILS SEE ------>>> http://iq-workshop.openmsa.cloud:8070/ui/links/repositories/quarantinedComponent/ZGQ3MmJiNDMyNjhjNDU0NWE0ZmM0ZDExZmIxYzQ0MzQ <<<------ for url: https://nexus-workshop.openmsa.cloud:8443/repository/thomas-pypi-proxy/packages/django/4.1/Django-4.1-py3-none-any.whl for URL https://nexus-workshop.openmsa.cloud:8443/repository/thomas-pypi-proxy/packages/django/4.1/Django-4.1-py3-none-any.whl#sha256=031ccb717782f6af83a0063a1957686e87cb4581ea61b47b3e9addf60687989a (from https://nexus-workshop.openmsa.cloud:8443/repository/thomas-pypi-proxy/simple/django/) (requires-python:>=3.8)
```

4\. IQ-server 접속 및 Report 확인
============================

4-1. Report 확인 (1)
------------------

위 에러에서 발생한 `FOR DETAILS SEE ------>>>` 문구에서 제공한 **Iq-server URL 확인하여 Report 확인**

Ex) `ERROR: Could not install requirement Django from https://nexus-workshop.openmsa.cloud:8443/repository/thomas-pypi-proxy/packages/django/4.1/Django-4.1-py3-none-any.whl#sha256=031ccb717782f6af83a0063a1957686e87cb4581ea61b47b3e9addf60687989a because of HTTP error 403 Client Error: -------------------->>> REQUESTED ITEM IS QUARANTINED -------------------->>> FOR DETAILS SEE ------>>> http://iq-workshop.openmsa.cloud:8070/ui/links/repositories/quarantinedComponent/ZGQ3MmJiNDMyNjhjNDU0NWE0ZmM0ZDExZmIxYzQ0MzQ <<<------ for url`

4-2. Report 확인 (2)
------------------

또는 Nexus에 접속하여 연동된 IqServer 를 직접 링크를 타고 확인 할 수 있습니다.

넥서스 링크를 타고 입장하면 “금지아이콘”으로 표시되어 격리가 된것을 육안으로 확인 할 수 있습니다.

![](attachments/654868581/654868608.png?width=680)

4-3. 로그인
--------

Iqserver login ID / PW는 Mission2 시작 날짜에 업로드 예정입니다.

![](attachments/654868581/654803097.png?width=566)

5\. Report 확인
=================================

**Report를 확인하여 아래 문항에 관련한 문제를 확인하여 제출하면 성공!**  
    

* * *

접속하여 `Quarantined` 을 클릭하여 격리되어있는 컴포넌트를 확인 할 수 있고  
”녹색 박스” 에 보이는 컴포넌트가 위반한 정책의 리스트들을 확인 할 수 있습니다.

이후 해당 컴포넌트를 클릭하여 컴포넌트 와 격리정책을 살펴봅니다

![](attachments/654868581/654835869.png)

아래 사항 취약점에 대한 정보를 확인하고 Info를 클릭하여 자세한 정보를 확인합니다.
    

![](attachments/654868581/654901388.png)

Policy 탭으로 이동합니다.`module`

![](attachments/654868581/654901398.png)

* * *

여기까지 오시느라 수고하셨습니다!
------------------

