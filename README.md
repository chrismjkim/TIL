# TIL 2023.01.27

VSCode 상에서 터미널을 열어준다. 단축키 (Crtl+Shift+')

- 터미널에서 코드를 입력한다.

  git init

git이라는 소프트웨어가 작업 폴더를 감시하기 시작한다.

    git add .

git add는 파일의 현재 상태를 기록하겠다는 명령어

.을 붙이면 변경사항이 있는 모든 파일을 대상으로 하겠다는 뜻이고, 특정 파일명을 붙이면 특정 파일만 대상으로 하겠다는 뜻이 된다.

    git commit -m "커밋 메시지"

남기고 싶은 메시지를 적는 것이다. 히스토리 조회를 커밋 메시지로 확인하는 것이다.

    git push 원격저장소명 브랜치명

만약 git clone을 통해 저장소를 복제했다면 일반적으로 원격저장소명은 origin이며 git remote명령어를 통해 정확한 저장소명을 알아낼 수 있다. 브랜치를 따로 안만든상태라면 그냥 git remote origin만 하면 된다.

    git push -u 원격저장소명 브랜치명

-u옵션을 사용하면 최초 한번에만 저장소명과 브랜치명을 입력하고 그 이후에는 모든 인자를 생략하고 git push만 할 수 있다.

# TIL 2023.01.28

- html 태그(실제로는 ()대신 <>로 사용해야 함)

  - (strong)(/strong): 진한 글씨

  - (u)(/u)": 밑줄
  - (h1)~(h6): 폰트 크기 조절, h1이 가장 크다

  - (br):새로운 줄을 표현, 2개를 사용하면 단락처럼 표현된다.

  - (p)(/p) :단락을 표현, 단락이 존재한다는 사실을 의미론적으로 표현 가능하기 때문에 정보로써 좀 더 가치있게 된다. 또 정해진 여백만큼 벌어진다.

  - (img src=""): 원하는 이미지의 주소를 적으면 그것을 표시하게 됨. width="", height=""로 크기 조절

  - HTML의 의미에 맞게 정확하게 사용하는 것은 비즈니스 측면에서 매우 중요하다.

  - (li)(/li): 목차 또는 목록을 쓸 때 사용하는 태그

  - (ul)(/ul): (li) 태그의 부모 태그. (li)와 같은 태그는 어디서부터 어디까지가 연관된 항목인지를 구분하기 위해 꼭 (ul)을 달아야 한다. => Unordered List

  - (ol)(/ol): (ul) 대신에 달 수 있는 태그. 리스트 항목 앞에 자동으로 번호를 매겨준다. => Ordered List

  - (title): 웹페이지의 제목을 설정하는 태그

  - (meta charset="utf-8"): 웹 브라우저가 파일을 utf-8로 열게 만드는 지시 태그

  - (head): 본문을 설명하는 부분을 묶는 태그

  - (body): 본문 부분을 묶는 태그

    즉, HTML상의 모든 태그는 head 또는 body에 놓이게 된다.

  - (html): head와 body를 감싸는 최고위층 태그이다.

  - (!DOCTYPE HTML): 이 문서에는 HTML이 담겨있다는 뜻으로, 코드 최상단에 관용적으로 쓰는 태그

  - (a href="https://www.w3.org/TR/html5/")(/a): 감싼 부분에 링크를 거는 태그, 하이퍼링크가 https://www.w3.org/TR/html5/로 이동하게 된다.

    - target 속성, title 속성: 링크를 클릭하기 전 툴팁 표시

      target="\_blank" title="툴팁내용" 과 같이 사용

  - font: 현재는 사용하지 않는 태그, CSS를 사용

- html 속성

  태그 내에 태그의 성질을 추가하는 것

- 부모 자식 태그

  태그의 포함 관계에 따라 부모 태그, 자식 태그로 부른다.
  사이 좋은 태그의 쌍들이 있다.

- Github 내 웹 호스팅 기능 활성화

  - Settings -> Code and automation -> Pages -> Branch를 main으로 -> Save -> DNS 설정

  - Actions -> pages-build-deployment, workflow 확인

  - 도메인이 생성된 이후 링크를 클릭하면 접속 가능하다.

# TIL 2023.01.29

- CSS
  HTML이 정보 전달에만 전념할 수 있도록 하기 위해, HTML로부터 디자인에 대한 기능을 뺴앗아 온 언어이다. style 태그 안에 모든 것이 갇혀있기 때문에 html 내에서 style 내부에만 CSS가 존재하고, 디자인에 대한 부분을 제외하고 코드를 보려면 style 부분만 빼면 된다.

  - style 태그: HTML의 문법이면서, 태그 안쪽에 있는 내용은 CSS 문법에 맞게 처리함

  - a: 모든 "a" 태그에 대해서

  - color:red; -> 폰트 색상이 빨간색

  - style=""은 HTML의 속성이고, 값으로는 반드시 CSS 효과가 들어온다.

  - CSS를 삽입하는 두 가지 방법이 style 태그를 사용하는 것, 그리고 style 속성을 쓰는 것의 두 가지이다.

            a{
            color:red;
            }

    라는 코드가 있다고 한다면,

  a라는 부분은 웹 페이지의 모든 a 태그를 선택한다는 점에서 선택자(selector)

  color:red; 부분은 선언,효과(declaration), color 부분은 프로퍼티(property), red 부분은 값(value)라고 한다.

  - 프로퍼티: CSS에서 효과를 의미하는 용어

  - 위계는 태그 선택자 < 클래스 선택자 < ID 선택자 이다.

  - 클래스 선택자는 "."을 붙이고, ID 선택자는 "#"을 붙이고, 태그 선택자는 아무것도 붙이지 않는다.

  - 태그 < 클래스 < ID이다. 태그 선택자를 통해 전체적인 태그 디자인을, 예외적인 것에 ID를 부여하는 것. ID는 식별번호, 즉 유일무이한 것에 붙인다고 생각하면 이해가 편하다.

  - block level element: 화면 전체를 사용

  - inline element: 자기 자신의 크기만큼 화면 사용

  - display:block; 엘리먼트 속성을 바꿀 수 있음

  - margin px값은 음수도 가능하다!

  - 웹상에서 텍스트를 드래그해서 선택하고 '검사'를 진행하면, Styles 부분에서 어떤 CSS 스타일의 영향권에 있는지 확인 가능하다. 코드가 복잡해졌을 때 파악에 매우매우매우 중요하다.

  - margin: 황토색, border: 살구색 padding: 연두색, content: 파란색

  - Margin>Border>Padding>Content

  - div 태그와 span 태그: 디자인이라는 목적 달성을 위해 어떠한 의미도 포함하지 않는 태그. div는 블록, span은 엘리먼트

  # 2023년 1월 30일

  - 포트폴리오 웹사이트를 제작하기 위해서 html과 css로 사이트를 만들었는데, 박스 안 메인 제목과 사진만 중앙 정렬하기 위해 고민했다.

  - 그리드 디자인 시 style은 margin border padding 순으로 속성을 쓰자

  - 같은 style 태그를 공유하는 여러 문서를 위해, style 부분은 css 파일로 만들고, link 태그를 이용해서 한꺼번에 수정할 수 있다.

  # 2023년 2월 4일

  - Javascript 공부 시작

    - onclick 속성의 값으로는 반드시 자바스크립트 코드가 와야 한다

    - onchange 내용이 변했을 때를 체크하는 이벤트

    - var을 변수 앞에 붙이자. var의 장단점은

    - 숫자, 문자열, 변수, 연산에 대한 문법은 c나 파이썬과 동일하다

    - 버튼 만드는 법

      input type="button" value="" onclick=""

    - 버튼보다는 toggle이 훨씬 인터페이스상으로 보기 좋고 깔끔한 것 같다.

    - value 값 가져오기

      document.querySelector('').value

    - 리팩터링이란?

    코드의 가독성을 높이고, 유지보수를 편리하게 만드록, 중복된 코드를 줄이는 방향으로 코드를 개선하는 작업

# 2023년 2월 10일

- VSCode에서 모두 찾아 바꾸기 를 실행하려면?

  - 단어 선택 후 Crtl + Shift + L 을 하면 같은 단어가 모두 선택됨, 이 상태에서 수정 시 적용됨

  - 찾아 바꾸기: Crtl + H

  - VSCode 공식 사이트 설명: 변수 및 메서드 등의 코드 기호의 이름을 바꾸는 경우 찾기 및 바꾸기를 사용하는 것보다 리팩터링하는 것이 좋습니다. 리팩터링은 지능형이고 범위를 이해하지만 찾기 및 바꾸기는 모든 항목을 무조건 바꿉니다.

  - JavaScript 에서 배열 선언하기

    var example = ['like','this']

  - JavaScript 에서 조건문 사용하기

  https://developer.mozilla.org/ko/docs/Web/JavaScript/Guide/Loops_and_iteration

  - script 태그: 안의 내용은 자바스크립트 문법을 따른다.

  - 배열을 선언할 때, 안의 내용을 코드로 치지 않을 수가 있겠다는 의문이 생겼다.
    그러면 그걸 엑셀로 선언할 수 있을까? 그럼 부합하는 엑셀 파일이 있겠구나!
    엑셀 확장자의 종류에는 뭐가 있을까?

    xls -> 엑셀 2003 이하 버전의 파일

  - xlsx -> 엑셀 2007 이상 버전의 파일

  찾다 보니 내가 알아보려고 한 것을 긁어주지 못할 것 같다.

  배열을 파일로 선언할 수 있는 방법이 있을지 추후에 찾아봐야겠다.

  - 자바스크립트 상에서 여러 버튼끼리 연동시키는 방법을 생각해서 스스로 해결했다.
    문제 상의 예제에서는 한 쪽 버튼을 클릭하면 다른 쪽 버튼의 value가 바뀌지 않았는데,
    다른 쪽 버튼의 value도 함께 변경되도록 스스로 코드를 수정했다.

  - 그리고 코드가 길어지다 보니 들여쓰기를 통해 가독성을 높이려면 어떻게 해야할지 고민이 많이 된다.

  - var, let, const 변수의 차이

    - var

      - 중복 선언 가능
      - 값 재할당 가능
      - 함수 내 변수만 지역변수로 취급

    - let

      - 중복 선언 불가능
      - 값 재할당 가능
      - {}에서 선언된 변수만 지역변수로 취급

    - const

      - 중복 선언 불가능
      - 값 재할당 불가능
      - {}에서 선언된 변수만 지역변수로 취급

    - 호이스팅
      다음을 참고: https://curryyou.tistory.com/192

  - settings.json 파일을 맞추어서 괄호 색 설정을 했다.

  - 객체

    - 객체 리터럴: 객체를 만들 때 사용하는 기호

    - 메서드: 객체에 소속된 함수

    - 프로퍼티: 객체에 소속된 변수

    - 객체에서는 프로퍼티와 프로퍼티 사이를 ,로 구분한다.

# 2023년 2월 11일

- ChatGPT의 제안
  - 변수명 좀 더 의미있게
  - 연산자, 콜론 등 뒤에 공백 한 칸
  -

# 2023년 2월 14일

- Github Pages에 커밋 내용이 적용이 안 될 때는 한 10분 이상 기다려보자

- 소팅 알고리즘을 비교분석하는 사이트에서 기본적인 페이지 양식을 만들어냈다. 이제 자바스크립트만 더하면 될듯

- 퀵소트가 재귀함수를 이용하면 깔끔하게 만들 수 있겠다고 생각이 들었다

- CSS 만지면서 border bottom 경계가 대각선으로 만들어질 떄 의문점이 들었음

# 2023년 2월 18일

- 자바스크립트를 사용해서 소팅 애니메이션을 구현하다가, 스택 구조와 큐 구조에 대해서 알게 되었다.\

  - 자바스크립트는 스택이 하나인 single threaded language이다

  - 기본적으로 Stack에서 명령들이 실행되고, 이벤트리스너(버튼)나 setTimeout 등의 명령어는 대기실에서 기다린다.

  - Queue에 있는 명령들은 Stack이 비게 되면 Stack으로 올려보내진다.

  - 그래서 오래 걸리는 연산은 자바스크립트로 시키면 안 된다. Stack을 바쁘게 만들면 사이트가 느려진다.

# 2023년 2월 23일

- 부트스트랩(BootStrap)

  - 웹 개발할 때, 보편적으로 널리 쓰이는 구성요소들을 미리 디자인해둔 것(툴킷,toolkit)

  - 반응형 웹(mediaquery) 지향

  - CDN(Contents Delivery Network)

    - 부트스트랩 웹사이트에서 코드를 바로 가져오는 방식

    - 사람들이 자주 사용하는 JS, CSS 파일들을 모아둠

    - 부트스트랩에서 색상 설정 가져오기 -> Documentation > Utilities > Colors

# 2023년 2월 24일

- 공부하는 책이 BootStrap 4 기준이어서, BootStrap 5에 맞는 버튼 정렬 방식을 엄청나게 고민했다.

  - Grid를 사용하면 해결이 되는데, 오른쪽 버튼에 그리드를 적용하면 버튼 높이가 엄청 높아져 버려서 고민이다.

  - 결국 w-50으로 설정해서 세 버튼의 크기를 모두 똑같게 맞췄다.

- cmder에서 가상환경 실행하기

  - venv\Scripts\activate.bat로 가상환경 실행

  - pip list: 현재 설치된 패키치 확인

  - deactivate: 가상환경 종료

  - ls: 소속된 파일 확인

  - ls -A: 숨겨진 파일까지 모두 확인

- 장고 프로젝트 생성하기

  - django-admin startproject django . : 장고 프로젝트 생성

  - python manage.py runserver

    - Starting development sever at (주소) -> 주소창에 입력 후 성공여부 확인

  - pycharm 확인

    - settings.py: 프로젝트의 설정을 담고 있는 파일

    - urls.py: 웹사이트 작동 방식 정리한 파일

  - Crtl + C: 구동 중인 서버 중단

  - python manage.py migrate: db.sqlite3라는 파일을 생성하며, 마이그레이션을 반영한 DB 생성

    - SQLite3가 좋은 점: 파일 하나로 관리하는 데이터베이스이므로 지식량이 많이 필요하지 않다.

  - python manage.py createsuperuser: 관리자 계정 생성

# 2023년 2월 25일

- django 웹사이트의 작동 원리

  - urls.py 확인: URL과 URL 접속시 실행시킬 함수 확인

  - views.py 확인: urls.py에서 실행시킬 함수와 클래스 정의

  - models.py 확인: 자료의 형태를 정의한 클래스

  - DB 접근

- PyCharm

  - .gitignore: git으로 버전관리하지 않는 항목 설정 (.idea/ 등 추가)

  - manage.py:

  - admin.py: 모델 등록

  - settings.py: 국제시간 등 설정

  - models.py: 클래스 정의, 자료 형태 설정

  - urls.py: URL 접속 규칙 설정

- cmd

  - C 디렉토리 관련

    - cd: C:\로 이동

    - cd github\: C:\github로 이동

  - git 관련

    - git clone (레포지토리 주소): 폴더 생성

    - git add . : 현재 폴더 staging

    - git commit -m "커밋 내용": 커밋

    - git push: 커밋한 내용 github와 연동

    - ls: 하위 항목(폴더)의 이름들을 나열

    - ls -A: 숨긴 폴더와 파일까지 보여줌

    - cd (폴더 이름): 해당 폴더로 이동

  - venv\Scripts\actviate.bat: 가상환경 실행

  - deactivate: 가상환경 종료

  - django-admin startproject (폴더명) . :해당 폴더에 장고 프로젝트 생성

- python manage.py 관련

  - python manage.py runserver: 라이브 서버 실행

  - Crtl + C : 라이브 서버 중단

  - python manage.py maekemigrations: 장고에게 수정했음을 알림

  - python manage.py migrate: 데이터베이스에 반영

  - python manage.py migrate --run-syncdb: 추가된 앱에 대한 테이블을 처음 db에 생성(위 명령어 오류 발생 시 사용)

  - python manage.py createsuperuser: 관리자 계정 생성
