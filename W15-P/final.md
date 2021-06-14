## 20180990 이소윤 기말과제

### 미션 1번 : 각자 서버에 접속할 수 있는 계정 3개 생성  

  
#### 3명의 이름은 a,b,c로 지정했으며 root계정에서 adduser [사용자명]을 사용했다.  
 <br/> 
  <br/> 
  
#### 서버를 재부팅하면 3명의 사용자가 추가된 것을 볼 수 있다.  

![컴시관 기말 1](https://user-images.githubusercontent.com/49148640/121887303-89a0e480-cd51-11eb-8eb8-eecdc268fdac.png)    
 

#### cat /etc/passwd 를 이용해서도 확인할 수 있다.  
    
https://user-images.githubusercontent.com/49148640/121887306-8b6aa800-cd51-11eb-9186-cfa7d9efd52c.mp4    

  
### 미션 2번 : 재택근무가 가능하도록 서버에 원격 접속    

#### ssh를 설치해 윈도우 터미널 창으로 원격 접속을 확인했다.   
 <br/> 
  <br/> 
#### a,b,c 모두 터미널에서 서버에 원격 접속이 가능한 것을 볼 수 있다.  
  
~~~
apt install openssh-server  

systemctl restart ssh  

systemctl enable ssh  

systemctl status ssh  
  
ufw allow 22/tcp
~~~
https://user-images.githubusercontent.com/49148640/121888471-ff598000-cd52-11eb-8246-a73523e8c84f.mp4    

  
## 미션 3번 : 스타트업 이름의 메일 서비스 별도 생성  
<br/> 
  <br/> 
  #### 메일 서비스는 lee.ac.kr로 했으며  DNS 서버 (Server)에 bind9 패키지를 사용했다.  
  #### 메일 서버에는 sendmail과 dovecot-pop3d 를 이용했다.   
  <br/> 
  <br/> <br/> 
  <br/> 
  #### 미션 3-1  
  #### 서버의 기존에 있던 유저 ubuntu 계정으로 로그인한 후 유저 a,b,c에게 각각 메일을 보냈다.  
    
      
https://user-images.githubusercontent.com/49148640/121890011-d76b1c00-cd54-11eb-8e4b-657e80ea6e02.mp4  
  
  #### 미션 3-2  
  <br/> 
  <br/> 
  #### 서버의 유저 a계정에서 유저 c에게 메일을 보냈다.  
https://user-images.githubusercontent.com/49148640/121888892-7e4eb880-cd53-11eb-9f0d-208b00906c92.mp4

https://user-images.githubusercontent.com/49148640/121888899-80b11280-cd53-11eb-9ed9-cfa04c39577d.mp4
