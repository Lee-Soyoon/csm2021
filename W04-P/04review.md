# 컴퓨터 시스템 관리 4주차 회고

## 1. 과제 

### 유용한 프로그램 설치하기

#### 1. Skype
- 스카이프 가장 인기있는 화상 채팅 응용 프로그램으로 인터뷰와 회의를 위해 많은 회사와 기업에서 사용됩니다. 
Skype는 우분투에서 꼭 필요한 애플리케이션 중 하나라고 생각해서 설치했다.   
특히, 코로나19로 인해 비대면 회의가 많아진 지금 유용하다.  

- 설치 방법
~~~  
- wget 명령을 사용해 최신 sktpe.deb 패키지를 다운로드한다.  
wget https://go.skype.com/skypeforlinux-64.deb  
- sudo apt install ./skypeforlinux-64.deb
~~~  

- 실행 화면

![image](https://user-images.githubusercontent.com/49148640/112719976-2fa53580-8f3f-11eb-9302-8faa13fc88e4.png)  


#### 2. VLC 미디어 재생기
MS Windows용으로 만들어진 곰플레이어와 비슷하고 중요한 요소인 자막도 잘 지원한다.

- 설치 방법  
~~~
- sudo add-apt-repository ppa:videolan/stable-daily  
- sudo apt update  
- sudo apt install vlc  

*영상 파일 바로 열기

- vlc file.mp4  
~~~

- 실행 화면
 
![image](https://user-images.githubusercontent.com/49148640/112720044-801c9300-8f3f-11eb-86cd-a65f807ca674.png)  


#### 3. visual studiocode
- vd코드는 microsoft의 오픈 소스 코드 편집기로 가볍고 시작 속도가 빠른 장점이 있다.  
또한, 내부의 많은 개발자들을 이용해 직접 제작한 확장팩을 제공하고 있더 신뢰 가능한 확장성이 있기때문에 설치했다.  

- 설치 방법
~~~
- visual studio code 사이트에서 우분투에 설치하기 위해 리눅스 64bit용 deb파일을 다운로드한다.
- sudo dpkg -i code*.deb
~~~

- 실행 화면
 
![image](https://user-images.githubusercontent.com/49148640/112719753-cc66d380-8f3d-11eb-8b26-393aa667806c.png)  





## 2. 새로 배운 내용

tldr 패키지 = 너무 길면 읽지 않는 패키지

apt search <패키지명>
이 패키지와 관련된 패키지를 볼 수 있다.

### gftp
~~~
내가 생성한 파일을 다른 컴퓨터들과 공유하는 것이다.  
gftp를 gui,cli 환경 모두 사용 가능해서 원하는 대로 골라 쓸 수 있다.  
~~~

### 패키지 삭제
~~~  
패키지를 삭제하는 옵션은 purge와 remove 두가지가 있다.
remove는 사용자가 설정한 설정 파일들은 남겨두고 삭제하지만 purge는 모두 삭제한다.

* autoremove는 연관된 패키지까지 함께 삭제한다.
~~~ 

### X 윈도우
~~~  
유닉스 계열 운영체제에서 사용되는 윈도우 시스템이다.  
디스플레이 장치에 창(윈도우)을 표시하며, 마우스와 키보드 등 입력장치의 상호작용을 관리해 GUI 환경 구현을 위한
기본적인 프레임워크 제공한다.  
~~~  




## 3. 문제가 발생한 부분과 해결 과정
server(b)에 GNOME 데스크톱 환경을 추가하기 위해 tasksel install ubuntu-deaktop을 했는데 이런 오류가 발생했다.  

![fail](https://user-images.githubusercontent.com/49148640/112719435-5ada5580-8f3c-11eb-83ee-e7c9960e2279.png)

원인은 찾지 못했지만 강의 자료에서 apt로 패키지 설치하는 방법으로 하니 해결됐다.




## 4. 참고할 만한 내용 
Ubuntu용 유용한 애플리케이션들  
https://with-ubuntu.tistory.com/8  




## 5. 회고
\+ 과제 제출을 저번주보다 여유롭게 했다.  
\- 과제를 더 빠르게 집중해서 끝낼 수 있는데 중간에 자꾸 늘어지게 된다. 다음주에는 정확히 시간을 정해두고 해봐야겠다.  
\! 패키지 설치가 편리하긴 하지만 패키지명을 다 알아야 사용가능한 단점도 있다.  
=> 그럴 때 우분투 소프트웨어 설치 지원 프로그램을 통해서 더 편하게 사용가능하다.  확실히 명령어를 통한 패키지 설치보다는 이 방법이 더 편리한 것 같다.  
가상의 환경에 평소에 사용하던 파이참, 인텔리 제이 등을 바로 설치해서 사용할 수 있다는 게 신기하다.  


