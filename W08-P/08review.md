## 1. 과제 

### 과제 1번
### 5주차에서 RAID5와 고민했던 RAID1을 Server(b)에 구축하라.

#### RAID1 설치

~~~
5주차 과제에서 RAID1과 RAID5 중에 고민하다 RAID5를 설치했다. 그래서 이번주에 복습하는 겸 RAID1을 설치해보려한다.  
RIAD1은 신뢰성과 가용성이 높고 복원이 간단하다. 따라서 중요한 데이터를 안전하게 관리 가능하다.  
가상머신을 사용하면서 아직까지 실수도 잦고 백업을 위해서 복원이 중요하다고 생각한다.  
물론 용량을 많이 차지한다는 단점이 있다.  
~~~ 

#### 하드디스크 파티션 후 
![8-1](https://user-images.githubusercontent.com/49148640/116040584-2aa2e580-a6a7-11eb-9a10-d97d2f2c043d.png)




![8-2](https://user-images.githubusercontent.com/49148640/116040638-3d1d1f00-a6a7-11eb-95d7-3eb1b0abcb2a.png)

#### RAID1을 구성  
![8-3](https://user-images.githubusercontent.com/49148640/116040919-92f1c700-a6a7-11eb-93ce-8f13c1487491.png)

### 과제 2

![8-4](https://user-images.githubusercontent.com/49148640/116040679-48704a80-a6a7-11eb-80ec-89175ddd97a7.png)


## 2. 새로 배운 내용


###  작업예약 
- cron  
~~~
- 주기적으로 반복되는 일 자동화 =>  시스텝 작업 예약  
- /etc/crontab의 형식  
~~~



- at 
~~~
- 일회성 작업 예약  

* 시간 자동 동기화
- timedatectl set-ntp 0 (동기화 off)
- timedatectl set-ntp 1 (동기화 on)
~~~




## 3. 문제가 발생한 부분과 해결 과정
이번주 실습에서는 딱히 없었다.  



## 4. 참고할 만한 내용  
bash scripting cheatsheet (배시 스크립트 유용한 명령어 사이트)  
https://johyungen.tistory.com/302  



## 5. 회고

