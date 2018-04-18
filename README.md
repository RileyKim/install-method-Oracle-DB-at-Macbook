# 맥에서 오라클 데이터 베이스 설치해보자!



#### 결론부터 말하자면 맥 OS에 오라클 데이터 베이스를 설치하는 것은 불가능하다.

##### 그 이유는 오라클에서 맥 OS에 데이터베이스를 지원하지 않기 때문이다. 

그렇기 때문에 가상머신을 통해 오라클 데이터 베이스를 설치하고 맥 OS에 Oracle sqldeveloper를 설치하여 

쉽게 맥북에서 오라클 데이터베이스를 연동하여 사용할 수 있다. 



모든 과정은 내가 시행착오를 겪으며 진행하였으며 맥북을 사용하는 모든 사람들이 처음 오라클 데이터베이스를 접했을 때, 

나와 같은 시행착오 없이 손쉽게 설치하고 개발을 진행할 수 있도록 도와주고자 글을 쓰게 되었다.



### 글이 길어보이지만 핵심만 설명하였고 이미지를 첨부하여 쉽게 따라할 수 있으니 끝까지 읽어보길 추천한다.



먼저 과정을 간략하게 말해보겠다. 

###1. 가상 머신 설치

###2. Oracle Technology Network Developer Day를 다운받아 가상 머신을 통해 리눅스에 오라클 DB 설치

###3. 가상 머신 네트워크 HOST/GUEST 연결

###4. 맥북 OS에 Oracle SqlDeveloper 설치

###5. 오라클 DB를 실행하여 SqlDeveloper 연동 테스트



-------------



# 1단계 : 이제 가상 머신을 설치해보자

##### 나는 VirtualBox라는 가상머신을 사용하였다!

##### VirtualBox Download URL : [https://www.virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads)

참고로 나는 5.2.8 버전을 다운받아 설치하였다.



![](/Users/TaekSu/Desktop/JavaDataGit/Mac and OracleDB/images/스크린샷 2018-04-17 오후 11.33.44.png)





맥 버전일 경우, OS X hosts를 다운받아 설치하면 가상 머신 설치는 끝나게된다. 

##### Tip : 윈도우를 설치하기 위해 가상머신을 다운받는 사람은 USB 연결 등을 하게해주는 확장팩 버전을 다운받아 설치하세요!!

##### 가상 머신과 같은 확장팩 버전을 다운받을 것!!



![](/Users/TaekSu/Desktop/JavaDataGit/Mac and OracleDB/images/스크린샷 2018-04-17 오후 11.53.02.png)



##### 가상머신 VirtualBox 완료. 

#####  Window10과 Oracle DB Developer VM은 내가 따로 설치한거니 신경쓰지 않아도 된다.



-----------------





# 2단계 : 가상머신 VirtualBox에 리눅스 OracleDB를 설치하자



#### 가상머신에 리눅스 오라클DB를 설치하기 위해 Oracle Technology Network Developer Day을 다운받자.



##### Oracle Technology Network Developer Day Download URL

[http://www.oracle.com/technetwork/database/enterprise-edition/databaseappdev-vm-161299.html]()



![](/Users/TaekSu/Desktop/JavaDataGit/Mac and OracleDB/images/스크린샷 2018-04-18 오전 12.07.28.png)



파일을 다운받아 리눅스를 설치하게 되면 OracleDB 등 설치 목록을 확인할 수 있다.



![](/Users/TaekSu/Desktop/JavaDataGit/Mac and OracleDB/images/스크린샷 2018-04-18 오전 12.07.48.png)

Accept 버튼을 클릭하면 Oracle DB Developer VM을 다운받을 수 있다. 

다운을 받은 후 다음 단계로 넘어가자!!!



#### 가상 머신을 실행한 후 상단 바에서 파일 항목을 누른 후 가상 시스템 가져오기를 실행하자!

![](/Users/TaekSu/Desktop/JavaDataGit/Mac and OracleDB/images/스크린샷 2018-04-18 오전 12.04.45.png)



![](/Users/TaekSu/Desktop/JavaDataGit/Mac and OracleDB/images/스크린샷 2018-04-18 오전 12.05.11.png)







![](/Users/TaekSu/Desktop/JavaDataGit/Mac and OracleDB/images/스크린샷 2018-04-18 오전 12.36.30.png)



![](/Users/TaekSu/Desktop/JavaDataGit/Mac and OracleDB/images/스크린샷 2018-04-18 오전 12.37.07.png)



계속 진행하여 설치를 완료하자!!!



![](/Users/TaekSu/Desktop/JavaDataGit/Mac and OracleDB/images/스크린샷 2018-04-17 오후 11.53.02.png)



Oracle DB Developer VM 설치 완료된 것을 볼 수 있다!!!!!!!!!!!!!



-------------------



# 3단계 : 가상 머신 네트워크 HOST/GUEST 연결 

간단하게 리눅스 오라클DB에서 사용자를 생성하는 것도 할 것이다.

그대로 따라하면 되니 너무 겁먹지 않아도 된다!ㅎㅎ



### HOST(MacBook)와 GUEST(Linux) 네트워크/포트 포워딩



![](/Users/TaekSu/Desktop/JavaDataGit/Mac and OracleDB/images/스크린샷 2018-04-17 오후 11.53.02.png)



가상머신을 실행하여 설정 버튼을 눌러보자.



![](/Users/TaekSu/Desktop/JavaDataGit/Mac and OracleDB/images/스크린샷 2018-04-18 오전 12.53.03.png)



네트워크 항목에서 포트 포워딩 버튼 클릭.



![](/Users/TaekSu/Desktop/JavaDataGit/Mac and OracleDB/images/스크린샷 2018-04-18 오전 12.53.19.png)



사진과 같이 설정해준다.





