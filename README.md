# HLS Demo page version2

## 목표 
* 자바스크립트를 이용해서 해당 데모 페이지를 5개의 브라우져로 대응 가능 하게 한다. 



## 업데이트 
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


