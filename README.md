화면구성 
0. 로그인(외부 api연결해서 행복에 대한 무작위 격언 표시,
          이메일 똑같은 구글계정 승인)
1. 홈(팔로워 많은 순으로 3명 나열, 클릭 시 포스팅 목록으로 이동)
![image](https://github.com/ljw20215223/instagram-nodejs/assets/118512075/9f0ad567-fdb1-434c-9691-0642c4ab19f8)

2.검색(프로필 사진 클릭하거나 팔로우 시 포스팅 이동, 차단 및 해제(차단 시 포스팅 못봄))
![image](https://github.com/ljw20215223/instagram-nodejs/assets/118512075/cae24b0d-0065-4fc4-abf5-6dd02f2717d3)

3.1대1 메시지(상대방의 이메일 타이핑 후 dm 가능, 지난 메시지 db저장)
![image](https://github.com/ljw20215223/instagram-nodejs/assets/118512075/c59f212f-8a44-4ae7-be87-a9f5f620c638)

4.프로필 (팔로워만 포스팅을 볼 수 있게 비공개, 프사 변경, 포스팅 추가and삭제
![image](https://github.com/ljw20215223/instagram-nodejs/assets/118512075/101a003d-e21c-4a70-bfd2-fbe195adaa1e)

5.댓글 (댓글 및 대댓글 , 본인 댓글 및 대댓글 삭제가능, 좋아요(이메일 담는 배열, 중복 좋아요 막기 위함)
![image](https://github.com/ljw20215223/instagram-nodejs/assets/118512075/fb426f95-489b-4d94-acdc-5ae336c0c703)

추가 기능
islogin 미들웨어로 매번 로그인됐는지 확인
회원가입 시 자동으로 기본프사 등록
글삭제 시 내부 댓글 및 대댓글 자동삭제


폴더 구조
![image](https://github.com/ljw20215223/instagram-nodejs/assets/118512075/44801567-f225-451e-999e-1d9b69d00492)


막힌 문제들과 해결책들 

1.대부분 왜 안되는지 모르겠을 때마다 console.log로 출력했다
2. form태그 말고 서버로 데이터 보낼 방법 없나? 쿼리파라미터로 보내자
3. 매번 로그인 해야 db에서 데이터가 갱신돼서 불편하다. 라우터에서 갱신 시켜서 결과를 ejs 변수로 보내자
4. db 컬럼 기본값을 null이 아닌 빈배열로 만들어서 !=null 같은 코드들을 전부 지울 수 있었다.
5. socket 모듈로 아주 간단한 채팅구현은 가능하지만 특정 두 유저만 있는 채팅방 생성 및 db에 대화기록 저장이라는 복잡한 상황은 엄두를 못냈으나 
gpt에게 물어봤더니 틀을 거의 짜주었고 내 프로젝트에 맞게 변수변경과 오타수정만 해줬더니 dm기능 완성
