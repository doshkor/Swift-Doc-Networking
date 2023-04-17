<!-- Swift-Doc-Networking -->
# Swift-Doc-Networking
###### Documentation / Foundation / URL Loading 

<br/>

<!-- 학습 목표 -->
# 학습 목표
##### 공식문서 학습을 진행합니다.

<br/>
    
<!-- 학습 내용 목차 -->
# 학습 내용
###### Networking
##### [URL Loading System](#URL-Loading-System)

<!-- ###### &nbsp;&nbsp;&nbsp;&nbsp; Essentials -->
<!-- ##### &nbsp;&nbsp;&nbsp;&nbsp; [Fetching Website Data into Memory](#Fetching-Website-Data-into-Memory) -->
<!-- ##### &nbsp;&nbsp;&nbsp;&nbsp; [Analyzing HTTP Traffic with Instruments](#Analyzing-HTTP-Traffic-with-Instruments) -->

<br/><br/>

<!-- 학습 내용 -->
#
## URL Loading System
###### API Collection
###### URL, 표준 인터넷 프로토콜을 이용하여 서버와 통신합니다.

**개요**

즉, 표준 혹은 커스텀 프로토콜(https or custom)을 통해 URL을 통해 식별된 리소스에 접근 가능하게 합니다. 이 작업은 비동기로 실행되며, 응답이 도착했을 때 처리할 수 있습니다.

URLSession 인스턴스를 가지고 앱의 데이터 또는 파일을 원격 저장소에 주고 받을 수 있는 URLSessionTask 인스턴스를 생성합니다. 캐시나 쿠키를 사용할지, 셀룰러 연결을 허용할지 말지 등의 세션 설정을 위해 URLSessionConfiguration 객체를 사용합니다.

한 개의 세션으로 여러 Task를 반복적으로 생성할 수 있습니다. 예를 들어 웹 브라우저는 일반 브라우징과 개인정보 보호 브라우징 두 개의 분리된 session 을 가질 수 있습니다. 이때 개인정보 보호 브라우징은 데이터를 캐싱하지 않습니다. 아래 그림은 이러한 구성을 사용하는 두 세션이 어떻게 여러 작업을 생성할 수 있는지 보여줍니다.

![](https://i.imgur.com/0KUvobT.png)

일반 모드와 시크릿 모드, 두 모드는 각각 별도의 URLsession을 사용합니다.

각 세션은 대리자와 연결되어 주기적으로 업데이트(또는 에러)를 받습니다. 각 delegate는 작성한 completion handler를 호출합니다. 커스텀한 delegate 를 작성하면 이 블록은 호출되지 않습니다.

백그라운드에서 세션이 실행되도록 설정 할 수 있습니다. 그렇게 되면 앱이 중단된 동안 시스템이 대신 다운로드하고 다시 돌아왔을 때 결과를 받을 수 있습니다.

#### [목차로 돌아가기](#학습-내용)

<!-- ## Fetching Website Data into Memory
#### [목차로 돌아가기](#학습-내용) -->

<!-- 
## 제목
#### [목차로 돌아가기](#학습-내용)
 -->
