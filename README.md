# HLS Demo page version2

## 목표 
* 자바스크립트를 이용해서 해당 데모 페이지를 5개의 브라우져로 대응 가능 하게 한다. -> 완료 
* HLS 플레이어중 IE11, Edge, Chrome, Safari 에 대응 가능하며, iOS -Webkit 에 대응하는 플레이어 찾기



## 업데이트 

### 2019 11 15 

- Pylr, Video.js, MediaElement, OpenPlayer.js, FlouidPlayer 테스트 중.

- vanlia.js 로 hls.js 를 통해 스트리밍 구현 성공 
- 하지만, 브라우저 마다 HLS 지원여부에 따라 실행 되는게 있고 없고가 존재 
- 크롬은 응답이 206 으로 성공했지만, 브라우저 내의 cors 가 걸림 
- 이 부분은 클라이언트 측에서 Proxy 로 돌리는 방식이나 서버측에서 cors 설정을 해주어야함.
- 따라서, 응답헤더에 ACAO 를 설정해 주어야 하는데. 클라이언트 측에서는 불가능 
- 결론적으로, 클라이언트 측에서 응답헤더를 조절 할 수 없다 ;; 

### 번외 
- 크롬 익스텐션 같은경우 일종의 프록시 기능으로 구현 
- manifest.json 을 통해 backgournd.js 를 구동시켜서 프록시 기능

### 2019 11 14 
1. lite-server 를 이용

```
npm i -g lite-server
```
2. 파일명은 index.html 로 해야한다. -> 그렇지 않으면 lite-server 에서 인식 하지 못함

> 대응 브라우저 
1. Chrome
2. Firefox
3. IE11 
4. Safari (HLS 지원가능)
5. Edge (HLS 지원가능)

* html5test.com 에서 해당 브라우져에 지원 여부를 파악 가능

>영상링크
* 2개의 m3u8, 1개의 mp4 
* 3개 모드 status = 206 (일부분 성공)

## 확인 된 사항
1. HLS 지원 브라우져는 모두 영상 재생 성공
2. 그렇지 않는 브라우저는 MP4 만 성공 


