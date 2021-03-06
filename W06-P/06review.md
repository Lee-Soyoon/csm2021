## 1. 과제 

### server(b)에 LVM 설정  
하드디스크 2개 추가(2GB, 3GB)한다.   
LV 4개 설정(1GB, 1GB, 2GB, 1GB)한 후 마운트 과정을 수행한다.  

실습 과제의 결과  
총 4개의 lv가 있다.  



![화면 캡처 2021-04-12 1](https://user-images.githubusercontent.com/49148640/114318612-c3365300-9b48-11eb-92ab-73a520e27fe7.png)  



![화면 캡처 2021-04-12 2](https://user-images.githubusercontent.com/49148640/114318629-db0dd700-9b48-11eb-847e-3f8a29a4b824.png) 


## 2. 새로 배운 내용

### 여러 개의 하드디스크를 하나처럼 사용하기

#### 1. RAID 6  
2개의 패리티 정보 사용함 (RAID 5 개선)   
=>RAID 5 보다 공간효과 성능(속도)는 낮지만, 데이터 신뢰도는 높아짐    
최소 4개 이상의 하드디스크 필요로 함
공간 사용 : 하드디스크의 개수 - 2  (2개는 피리티 정보)


#### 2. RAID 1+0  
RAID 1으로 구성한 디스크를 다시 RAID 0 로 구성함   
=> 데이터의 신뢰성& 성능(속도) 동시 확보     
공간효율은 50%  
  


#### 3. RAID 1+6  
RAID 1으로 구성한 디스크를 다시 RAID 6 로 구성함
- 아주 중요한 데이터를 다루는 경우 사용  





### LVM
####  LVM, Logical Volum Manage  
• 논리적 볼륨을 효율적이고 유연하게 관리하기 위한 커널의 한 부분이자 프로그램
• 용량 조절, 크기 조절, 편의에 따른 장치 이름 지정, 디스크 스트라이핑, 미러 볼륨 제공


### LVM 구성
1. 하드디스크 준비  
2. 원하는 대로 파티션 나누기  
3. 물리적인 볼륨 생성  
4. 볼륨그룹 생성 (물리볼륨을 묶어서)  
5. 논리볼륨 생성  
6. 각 논리볼륨에 파일시스템 생성  
7. 논리볼륨 마운트  
8. 부팅 시 자동 마운트 설정  





## 3. 문제가 발생한 부분과 해결 과정
논리볼륨을 생성하는 과정에서 아래와 같은 myLV4할 때 실수를 하고도 그냥 지나갔다.    
논리볼륨에 파일시스템을 생성할 때 발견해서 다시 올바르게 고친 후 실습을 진행했다.    



![화면 캡처 2021-04-12 3](https://user-images.githubusercontent.com/49148640/114318648-eb25b680-9b48-11eb-8587-a9b356ec9694.png)


## 4. 참고할 만한 내용  
LVM 부가 설명   
https://lascrea.tistory.com/156  




## 5. 회고
\+ 중간에 다른 짓을 하지않고 집중해서 하니 실습과제 시간이 저번주보다 많이 줄었다!    
서버에서 실습하는 도중에 오류가 나면 백업해둔 서버 복사, 붙여넣기를 통해 쉽게 해결할 수 있어서 좋다.  
\- 백업을 해두니 장점도 있지만 오류발생 시 문제점을 찾다가 잘 해결되지 않으면 금방 포기하고 다시 처음부터 하게 된다. 오류 해결에 끈기를 가져보자!  
\! 파일시스템에 큰 파일들을 계속 복사하는 것을 방지하기 위해 쿼터를 이용해 파일 시스템마다 사용자나 그룹이 생성할 수 있는 파일의 용량, 개수를 제한할 수 있다.    


