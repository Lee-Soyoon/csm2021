## 1. 과제 


실습 과제 결과 확인

### 모든 ip주소와 실습이 순조롭게 되었지만  
![Server(b) - VMware Workstation 16 Player (Non-commercial use only) 2021-06-08 오전 7_27_21](https://user-images.githubusercontent.com/49148640/121095353-2849b480-c82b-11eb-8eae-3f46f3347c9c.png)  

  
    
    
![Client - VMware Workstation 16 Player (Non-commercial use only) 2021-06-08 오전 7_27_49](https://user-images.githubusercontent.com/49148640/121095356-2aac0e80-c82b-11eb-8b32-e9a9b68d0c96.png)  
  
    
    
![Server - VMware Workstation 16 Player (Non-commercial use only) 2021-06-08 오전 7_27_54](https://user-images.githubusercontent.com/49148640/121095358-2c75d200-c82b-11eb-81d5-62c86670a372.png)  
  
    
    
### 마지막에 접속이 되지 않았다...      
![192 168 159 128 - Chrome 2021-06-08 오전 7_28_03](https://user-images.githubusercontent.com/49148640/121095364-2e3f9580-c82b-11eb-8f70-7ab9c737e02a.png)  
  
    

  
    
      
    
      

## 2. 새로 배운 내용, 복습

### 서버의 방화벽 정책 설정 단계    
#### 1. 외부 컴퓨터는 내부에 접속할 수 없도록 한다.  
~~~
• iptables --policy FORWARD DROP
• iptables --policy INPUT DROP
• iptables --pplicy OUTPUT DROP
~~~  
  
    
#### 2. 내부 컴퓨터는 외부 인터넷을 사용할 수 있도록 한다.
~~~
• 패킷 포워딩 설정  
• 방화벽 규칙 추가 : ens35 장치로 모든 패킷 통과하도록 설정  
• 방화벽 규칙 추가 : ens32 장치로 모든 패킷 통과하도록 설정  
• ens32 에 마스커레이드 허가  
• 설정한 내용 저장
~~~
  
    
#### 3. 외부 컴퓨터가 방화벽 서버의 공인 IP로 웹 서비스를 요청하면, 내부 웹 서버가 서비스한다.
~~~
• Server(b)에 nginx 웹 서버 설치  
• Server에 규칙 추가  
~~~

    
      
## 3. 문제가 발생한 부분과 해결 과정
아직 해결하지 못했다.,,  
처음에 교수님이 서버b의 apt update가 안될거라고 하셨는데 잘 되길래 그냥 실습을 했는데 그 부분이 문제일까?    


  
    
      
## 4. 참고할 만한 내용  
apt update 오류  
https://ksy3241blog.wordpress.com/2016/06/17/sudo-apt-get-update-%EC%97%90%EB%9F%AC/  

    
      
## 5. 회고
\+ 방화벽 실습을 통해 가상 서버를 나의 호스트 컴퓨터로 접속할 수 있게되었다.       
\- 실습을 완성하고 싶었지만 그러지 못해서 굉장히 아쉽다.  
\! 실습이 완료되지 않아 아쉽다..문제점도 찾지 못했다.마지막에 서버b의 apt update가 안되길래 초기화하고 아예 처음에 설치하고 시작했는데도 실패했다..  
 
