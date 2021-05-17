
## 1. 과제 

### 사용한 ip 3개  
~~~

www.sungshin.ac.kr -> 203.250.150.73  
www.sookmyung.ac.kr -> 203.252.201.8  
www.ewha.ac.kr -> 203.255.161.161  
~~~  

### 실습 과제 결과 확인

https://user-images.githubusercontent.com/49148640/118504307-59702100-b766-11eb-84b3-e8e239ee86fa.mp4



## 2. 새로 배운 내용, 복습
### Domain Name System

~~~
- namesever에 문제가 생겨도 ip를 알면 접속이 가능함    
- 도메인 네임 시스템, 네임 서버  
- 호스트의 도메인 이름을 호스트의 네트워크 주소로 바꾸거나, 그 반대의 변환  
~~~


### Round Robin DNS

~~~
- 하나의 사이트의 ip를 나눠놓고 부하를 줄이는 방법    
- 여러 대의 웹 서버를 운영하여 웹 클라이언트가 서비스를 요청할 경우 교대로 서비스를 실행하여, 웹 서버의 부하를 공평하게 나누는 방식  
~~~ 






## 3. 문제가 발생한 부분과 해결 과정
ufw status에서 자꾸 서버가 inactive라고 뜨는데 아직 원인을 발견하지 못했지만 실습은 가능했다...  



## 4. 참고할 만한 내용  
원격 서버에 접속하는 방법: SSH  
https://llighter.github.io/access-remote-server-with-ssh/  


## 5. 회고
\+ iPutty에 이어서 가상 호스트로 git bash를 이용해 원격 접속 신기했다.  내가 만든 네임서버 주소로 여러 사이트에 바로 접속이 가능하다는 것도 신기했다.   
\- ufw status에서 자꾸 서버가 inactive라고 뜨는데 아직 원인을 발견하지 못했다..  
\! namesever에 문제가 생겨도 ip를 알면 접속이 가능하다!  
