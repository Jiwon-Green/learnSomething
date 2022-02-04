
## 문제점
aws 서버 생성 후에 putty로 접속하고 자바8, 시간대 변경까지 다했다 <br>
hostname 변경하기 위해 <br>

```
$ sudo vim /etc/sysconfig/network

## hostname 적고 :wq 저장
HOSTNAME=hostname11

$ sudo reboot
``` 


했는데 remote side unexpectedly closed network connection 라면서 먹통 됨 <br>
먹통 돼도 putty 껐다키면 괜찮겠지, 했는데 껐다켜도 반영이 안되어있었다.


## 해결방법

검색해보니 호스트명 변경을, vim 편집 말고 명령어로 해보라는 글이 있었다!  

```
$ sudo hostnamectl set-hostname 호스트명
$ exit
```

다시 재접속 하니 해결!!!  😁😁


## 외않되
reboot 을 하면 OS가 재부팅 되니까 접속된 SSH 세션이 당연히 끊긴다고 하는데 ..
책에선 어떻게 했는지 궁금
