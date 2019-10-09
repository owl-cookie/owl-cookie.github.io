---
layout: post
title: ngrok
tags: [ngrok, server]
image: '/images/posts/ngrok/ngrok-structure.png'
---

github project를 하나 만들면서 jenkins를 붙이고 sonarCube 까지 붙여보고 싶은 욕구가 생겨, 여러가지 글들을 디깅했었다. 
그러다가, 발견하게된 [ngrok](https://ngrok.com)! 

ngrok란 `별도의 설정 없이, 외부로부터 로컬 네트워크의 터널을 공개시킬 수 있는 프로그램` 이다.     
(+ 다른 기능들도 있다.)
 
> 여러가지 상황에서 사용할 수 있을거 같아서 간단하게 정리를 해볼까 한다.


#### TL;DR

```
0. https://ngrok.com/download 접속
1. 환경별 ngrok 설치 
2. zip 해제 후, token 입력
3. ./ngrok http ${port}  실행
4. forwarding 된 url 접근 
```

> 예시

```
Forwarding                    http://0000.ngrok.io -> http://localhost:4000
Forwarding                    https://0000.ngrok.io -> http://localhost:4000
```

위처럼 특정 도메인을 Localhost:port로 forwarding 해준다.

> (주의) free plan 인 경우, 실행 시 마다 forwarding 되는 url 이 달라진다. 

#### When should we use ngrok??


```
1. Demoing web sites without deploying
2. Building webhook consumers on your dev machine
3. Testing mobile apps connected to your locally running backend
4. Stable addresses for your connected devices that are deployed in the field
5. Running personal cloud services from your home
```

> local/Test 환경에서 사용하는것을 권장한다.

개인적으로 만든 프로젝트들을 자랑하기 위해, 구름 IDE 나 cloud 9 에서 자주 사용하고 있다. 


#### Other feature 

ngrok를 실행 후, `http://localhost:4040` 로 접근하면 아래처럼 request 에 대한 정보를 열람할 수 있는 페이지가 노출된다.

> client-end 개발자와 협업 시, 조금은 유용하지 않을까 ?? 


![ngrok inspection](/images/posts/ngrok/ngrok-inspection.png)

위처럼 인입된 request를 볼 수 있으며, `replay` 버튼을 이용하여 request를 재실행 할 수 있는 기능을 제공한다.




2019.10.06      
lusiue@gmail.com   

