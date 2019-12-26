# 환경설정

[https://www.youtube.com/watch?v=hYr8ZHv40Nk](https://www.youtube.com/watch?v=hYr8ZHv40Nk)



이 강의를 보면서 따라함.

{% embed url="https://dololak.tistory.com/355" %}



docker for windows와 docker toolbox를 같이 깔았더니 충돌이 남.

hyper-v\(가상화\) 기능을 키면 docker는 실행되는데 docker toolbox에서 oracle vm 실행이 안됨.vice versa

{% embed url="https://woonizzooni.tistory.com/entry/Windows10%EC%97%90%EC%84%9C-Docker%EC%99%80-VMware-%EB%8F%99%EC%8B%9C-%EC%82%AC%EC%9A%A9-%EB%B6%88%EA%B0%80" %}

이걸 보면서 해결.



{% embed url="https://github.com/QingdaoU/OnlineJudgeDeploy" %}

어쨌든 여기서 땡겨받아서 

docker-compose up -d 명령어를 실행



sudo apt install git

sudo apt install nodejs-legacy

sudo apt install npm

sudo npm clean cache -f 

sudo npm install -g n



`An attemp was made to access a socket in a way forbidden by its access permissions.`

갑자기 이런 에러가 떠서 도커가 실행이 안됐는데

netsh int ip reset resetlog.txt

이 명령어를 치니까 된다. tcp/ip 원상복구라는데 흠...

 

