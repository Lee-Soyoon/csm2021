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
### cron을 이용해 매주 일요일 오전 12시에 마지막 재부팅 시간을 확인 후 log파일에 기록하도록 예약작업 설정하기  


#### crontab -e를 이용해 아래와 같이 수정했다.

~~~
* 시간 설정  
매주 일요일 오전 12시 이므로 => 00 (분) 2 (시) *(일) *(월) 7(요일)로 설정  
* 명령어 뒤의 > /log  
명령어가 실행된 후 실행 결과를 log파일에 기록하도록 설정  
~~~

![8-4](https://user-images.githubusercontent.com/49148640/116040679-48704a80-a6a7-11eb-80ec-89175ddd97a7.png)


## 2. 새로 배운 내용, 복슥


###  작업예약 복습
- cron  
~~~
- 주기적으로 반복되는 일 자동화 =>  시스텝 작업 예약  
- /etc/crontab의 형식  
~~~

- crontab 사용 방법
~~~
* 예약작업 추가 및 수정   
crontab -e  
* 예약작업 리스트 확업  
crontab -l  
* 예약작업 시작  
service crond start  
~~~





## 3. 문제가 발생한 부분과 해결 과정
이번주 실습에서는 딱히 없었다.  



## 4. 참고할 만한 내용  
Linux  예약 작업 crontab  
https://m.blog.naver.com/PostView.nhn?blogId=diceworld&logNo=220253702882&proxyReferer=https:%2F%2Fwww.google.com%2F




## 5. 회고
/+ 교수님 말씀대로 나중에 따로 다시 해봐야지 해놓고 막상 실제로 복습한 적이 거의 없었다. 이번 기회에 반학기동안 배운 내용을 복습할 수 있어서 좋았다.  
/- 나름 열심히 실습했다고 생각했는데 넣쳤던 부분이 생각보다 많은 것 같다. 진작 복습하지 않은 것이 후회됐다.  
/! 확실히 직접 문제를 만들기위해 고민하고 해결하니 더 잘 이해하게 된다. 앞으로도 직접 문제를 만들어보며 공부해야겠다.
