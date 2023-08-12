# 🚌 BUSTAGO
한남대학교 셔틀버스 앱

## 🕶️ 프로젝트 개요
- 개발 목적: 현재 학생들에게는 셔틀버스 관련 어플이 없어 이용하는데 불편을 겪는 것을 파악하고, 버스 정원을 45명으로 제한함으로써, 실제 탑승 인원보다 초과 인원으로 인한 사고를 예방하고자 어플리케이션 제작
- 최종 배포: 2023.06.18

## 💻 개발 환경
### Language & Tools
<img src="https://img.shields.io/badge/java-007396?style=for-the-badge&logo=java&logoColor=white"> <img src="https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white"> <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white"/> <img src="https://img.shields.io/badge/Android Studio-3DDC84?style=for-the-badge&logo=androidstudio&logoColor=white"/> <img src="https://img.shields.io/badge/Visual Studio Code-007ACC?style=for-the-badge&logo=visualstudiocode&logoColor=white"/>

### Collaboration
<img src="https://img.shields.io/badge/Notion-000000?style=for-the-badge&logo=notion&logoColor=white"/> <img src="https://img.shields.io/badge/Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white"/> <img src="https://img.shields.io/badge/Slack-4A154B?style=for-the-badge&logo=slack&logoColor=white"/> <img src="https://img.shields.io/badge/Github-181717?style=for-the-badge&logo=github&logoColor=white"/>


## 🖼️ 화면 구성
<table>
        <tr>
              <th>로그인 화면</th>
              <th>학생용 화면</th>
                <th>버스 위치 화면</th>
                <th>분실물 게시판</th>
              <th>기사용 화면</th>
        </tr>
        <tr>
              <td valign="top"><img src="https://github.com/KIMJOONSIG/BUSTAGO/assets/129662947/10e91366-ab34-455a-8835-393b46f390f3"></td>
                <td valign="top"><img src="https://github.com/KIMJOONSIG/BUSTAGO/assets/129662947/6467f8a5-0ddc-4d04-851f-00132db959b8"></td>
                <td valign="top"><img src="https://github.com/KIMJOONSIG/BUSTAGO/assets/129662947/f8308bcd-3939-4f01-a01b-12e9c506e78f"></td>
                <td valign="top"><img src="https://github.com/KIMJOONSIG/BUSTAGO/assets/129662947/76efaba1-70a3-403a-81d4-15fc8b089cc2"></td>
                <td valign="top"><img src="https://github.com/KIMJOONSIG/BUSTAGO/assets/129662947/2bef0891-a8bd-4515-b390-a146d6872250"></td>
        </tr>
</table>

## 🌟 주요 기능
- 로그인 기능 : 입력받은 아이디 정보를 Internet를 통해 다음 Activity로 사용자의 정보가 이동할 수 있도록 함. 위 결과물에서 볼 수 있듯이 모든 사용자의 예약목록을 가져오지 않고 로그인 된 사용자만의 에약 목록을 출력함.
- 버스 위치 전송 및 확인 기능 : LocationListener를 통해 1초마다 위도, 경도 를 업데이트 함. 업데이트 된 위치정보는 httpURLConnection을 통해 서버로 전송하며, GoogleMap API를 통해 안드로이드 기기에 버스 위치 정보를 표시함
- 분신물 이미지 업로드 및 확인 기능 : 선택한 이미지를 Bitmap 객체로 생성하여 Byte Array로 변환

## 🆙 Security Update(2023.08.12)
- 이미지 전송 시 base64_decode를 통해 파일형식 저장
- 로그인 과정에서 발생할 수 있는 보안 사고를 예방하고자 POST 전송 방식과 안전한 SQL처리를 위한 Prepared Statement 사용
- 중복된 아이디 생성 예방을 위한 중복 처리 기능 Update
