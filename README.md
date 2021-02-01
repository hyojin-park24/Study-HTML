# HTML학습 리포지토리

HTML5,CSS3, JS 학습용 리포지토리

## HTML5 
HTML 기본 학습

--------------------------------------------------------------------------

###### HTML기본학습
[HTML소스](https://github.com/hyojin-park24/Study-HTML/tree/main/01_HTML)

--------------------------------------------------------------------------

### 1월25~1월29일 1주차 수업 Review
> 웹은 **request**에대한 **response**이다.

```
※ 프로그래밍이란?   
 :프로그램언어를 이용해 프로그램을 구현하는 기술
 
※ IoT사물인터넷이란?   
 :사물에 센서와 통신 기능을 내장하여 인터넷에 연결하는 기술
 ```
 
 -------------------------------------------------------------------------

## 1.HTML기본태그
>태그와 속성의 이해

 -   **글자태그**    
 
  * h1~h6 : 제목 글자 생성   
  * p/br/hr : 본문 생성/줄바꿈/수평선 생성   
  * a : 하이퍼링크 생성    
  * b/i/small/sub/super/ins/del : 굴게/기울게/작게/아래첨자/위첨자/밑줄글자/취소선글자    
    
  
  ```
  <a태그> 앵커태그 = 링크태그라고 부름    
  a태그 속성 herf   
  <a href="www.naver.com">네이버</a>
  ```   
 
 - **목록태그**  
 
   * ul/ol/li : 순서없는 목록 / 순서있는 목록 / 목록 요소    
  
  ```
  <body>
   <ul>
    <li> 
     <b> 과일 </b>
      <ol> 
       <li> 사과 </li>
       <li> 바나나 </li>
       <li> 딸기 </li>
      </ol>
    </li>
   </ul>
  </body> 
```   

- **테이블태그**

  * table/tr/th/td   
    : __표__ 삽입 / 표에 **행** 삽입 / 표의 **제목 셀** 생성 / 표에 **일반 셀** 생성   
 
 > table 태그 속성 : border (표의 두께 지정)
   th 태그 속성 : colspan (셀 너비 지정)
   td 태그 속성 : rowspan (셀 높이 지정)

```
    <!DOCTYPE html>
<html>
<head>
    <title>HTML Table Basic Page</title>
</head>
<body>
    <table border="1">
        <tr>
            <th colspan="2">지역별 홍차</th>
        </tr>
        <tr>
            <th rowspan="3">중국</th>
            <td>정산소종</td>
        </tr>
        <tr><td>기문</td></tr>
        <tr><td>운남</td></tr>
        <tr>
            <th rowspan="4">인도 및 스리랑카</th>
            <td>아삼</td>
        </tr>
        <tr><td>실론</td></tr>
        <tr><td>다질링</td></tr>
        <tr><td>닐기리</td></tr>
    </table>
</body>
</html>

```   

- **IMG태그**    

  * 4가지 속성   
 
    * src / alt / width / heidth : 경로지정 / 이미지 에러시 글 표현 / 너비 / 높이    
  
- **AUDIO태그**   

  * 5가지 속성   
 
    * src / preload / autoplay / loop / cotrols   
  
- **VIDEO태그**   

  * 2가지 속성   
 
    * width / heidth   
    
 ## 2. HTML5 입력양식 태그와 구조화 태그   
 
  > **입력 양식 이란?**   
    사용자에게 정보를 입력받는 요소 : 입력 양식 태그를 사용   
    **POST방식과 GET방식**   
    - POST 방식 : 비밀스럽게 데이터를 전달   
       Ex) 물건을 택배로 부치듯 데이터를 별도로 전송 : **데이터 용량 제한 없음**   
    - GET 방식 : 주소에 데이터를 입력해서 전달   
       Ex) 물건을 직접 들고 감 : **데이터 크기 한정**   
       
       
       <body>   
        <form>   
         <input type = "text" name = "search">   
         <input type = "submit">   
        </form>   
       </body> 
       
          
       => <form> 태그로 영역 생성 , <input>으로 내부 태그를 넣어서 만듦    
       
       <!--POST 전송 방식-->   
       <body>   
        <form method = "post">   
         <input type = "text" name = "search">   
         <input type = "submit">   
        </form>   
       </body>   
       
       <!--GET 전송 방식-->   
       <body>   
        <form method = "get">   
         <input type = "text" name = "search">   
         <input type = "submit">   
        </form>   
       </body>   
       
  **입력 양식 태그**   
  
   * form : 입력 양식의 시작과 끝 표시    
   * input   
     * text : 글자 입력 양식 생성   
     * buttom : 버튼 생성   
     * checkbox : 체크 박스 생성    
     * file : 파일 입력 양식 생성   
     * hidden : 해당내용 표시 안 함   
     * image : 이미지 형태 생성   
     * password : 비밀번호 입력 양식 생성   
     * radio : 라디오 버튼 생성   
     * reset : 초기화 버튼 생성   
     * submit : 제출 버튼 생성   
  * textarea   
    * cols/rows : 여러 행의 글자 입력 양식 생성 (너비/높이)   
  * select / optgroup / option : 선택 양식 생성 / 옵션 그룹화 / 옵션  생성    
  * fieldset / legend : 입력 양식의 그룹 지정 / 입력 양식 그룹의 이름 지정   
  
 > **공간분할 이란?**   
    웹 페이지 레이아웃 구성을 위한 공간 분할 ( CSS 효율 방식 )   
    **DIV 태그** 와 **SPAN 태그**    
    - div : 블록 형식의 공간 분할    
    - span : 인라인 형식의 공간 분할   
    대세는 공간분할 태그의 div태그   
    
  **블록 형식 태그**   
  * div태그   
  * h1~h6 태그   
  * p태그   
  * 목록 태그   
  * 테이블 태그   
  
  **인라인 형식 태그**   
  * span 태그   
  * a 태그   
  * input 태그   
  * 글자 형식 태그   
  * 입력 양식 태그   
  
> **시맨틱 태그란?**   
  - 시맨틱(semantic) '의미론적인'   
  - 태그 분별이 어려워 웹 페이지에서 데이터를 효율적으로 추줄할 수 없기에 태그에 의미를 부여한 웹 = 시맨틱 웹   
  - 컴퓨터 프로그램이 코드를 읽고 의미를 인식할 수 있는 지능형 웹   
  
 * header : 머리말    
 * nav : 하이퍼링크들을 모아 둔 내비게이션   
 * aside : 본문 흐름에 벗어나는 노트나 팁   
 * section : 문서의 장이나 절에 해당하는 내용   
 * article : 본문과 독립적인 콘텐츠 영역   
 * footer : 꼬리말 (저자나 저작권 정보)   
 
  article ⊂ section 
  
  
    
    

## CSS3
CSS3 기본 학습   
[CSS소스](https://github.com/hyojin-park24/Study-HTML/tree/main/02_CSS)


## JAVASCRIPT 
JAVASCRIPT 기본 학습

## Risponsive Web
응답형 웹 기본 학습

## Project
전체통합 프로젝트
