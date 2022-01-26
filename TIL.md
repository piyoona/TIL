# 깃&깃허브 특강

## 설치

1. Git 설치
2. vscode 설치
3. Typora 설치



## 1) CLI 기초

- `GUI vs CLI`

  - GUI: 그래픽 유저 인터페이스 (ex.터미널)

  - CLI: 커멘드 라인 인터페이스 (ex.파인더)

    

- `경로`

  -  상대경로 : 내 현재 위치 기준

  -  절대경로 : 어디든 상관없는 위치

    

- `터미널 명령어`

  1. `/` (루트 디렉토리): 모든 파일과 폴더를 담고 있는 최상위 폴더

  2. `~` (홈 디렉토리)

  3. `ls` (list segments): 현재 디렉토리내의 폴더&파일을 보여줌

     - ls -a: all 옵션. 숨긴 폴더&파일을 보여줌(.파일|폴더로 표시됨)
     - ls -l: long 옵션. 정보를 자세히 보여줌
     - ls -a -l: all, long 옵션을 함께 적용
     - ls -al: 여러 옵션 축약 가능

  4. `clear` : 지우기

  5. `화살표 키 ▲` : 최근 기입한 명령어를 보여줌

  6. `touch` : 파일을 만드는 경우

     ```html
     touch a.txt -> a.txt 파일 생성
     touch a.txt b.txt c.txt -> 띄어쓰기로 구분하여 여러 파일 한꺼번에 생성 가능
     ```

  7.  `mkdir` (make directory) : 폴더를 만드는 경우

     ```
     mkdir test -> test 라는 이름의 폴더 생성
     mkdir test test -> test 라는 이름의 폴더 2개 생성 -> 중복된 이름으로 오류 발생
     mkdir "test test" -> test test 라는 이름의 폴더 생성
     ```

  8. `cd` (change directory) : 위치 이동 / 홈 위치로

     - cd + 폴더명 : 입력한 폴더로 위치 이동
     - cd + . : 현재 위치를 알려줌
     - cd + .. : 현재 위치에서 상대 경로의 상위로 위치 이동

  9. `mv` (move) : 폴더&파일을 다른 폴더 내로 이동 / 이름 바꾸기

     - mv a.txt b.txt : a.txt -> b.txt 로 이름 바꾸기
     - mv a.txt test : a.txt 를 test 폴더 안으로 이동

  10. `rm` (remove) : 삭제 (휴지통X)

      - 파일 삭제 : rm a.txt
      - 폴더 삭제 : rm -r test
      - \* (asterisk, wildcard) : all
      - rm *.txt : 현재 위치내의 txt 파일 전체 삭제
      - rm -rf : 강제 삭제
      - rm -rf* : 전체 강제 삭제 (XXXXX사용XXXXX)

  11. `open`

      ```
      # Mac
      open a.txt
      ```

      

  12. `단축키`

      - ctrl + l : 화면 정리 (스크롤 올리면 과거 내역 조회 가능)
      - ctrl +  a,e : 앞 뒤로 이동
      - tap : 폴더&파일 이름 자동 완성



## 2) Markdown

### 마크다운 문법

1. `#` : 제목 (h1~h6)

   ```html
   # h1
   ## h2
   ### h3
   #### h4
   ##### h5
   ###### h6
   ```

   

   

2. `목록(list)`

   -  순서가 없는 목록 : `- * +`

   - 순서가 있는 목록 : `1. 2. 3.`

   - 들여쓰기 : `tap 키`

     

3. `인용` : `< + 스페이스바`

   > 인용문
   >
   > >개수에 따라 중첩 가능

   

4. `코드`

- - ```inline code` `` : 백틱(`)으로 코드를 감싸준다.

  - ```
    block code : ``` + Enter
    ```



5. `링크`

   - `[표시할 글자](이동할 주소)` 형태로 작성

     ```
     [GOOGLE](http://google.com)을 눌러서 구글로 이동하세요.
     ```



6. `이미지` 

7. - `![대체 텍스트](이미지 주소)` 형태로 작성

   - 대체 텍스트란 이미지를 정상적으로 불러오지 못했을 때 표시되는 문구

   - Typora에서는 이미지 파일을 드래그해서 자동 업로드 가능

     ```
     ![Git로고](http://git-scm.com/images/logo@2x.png)
     ```



7. `표`

   ```
   # Mac 표 생성 단축키
   option + command + t
   ```

   - `파이프( | )` 와 `하이픈( - )`로 행과 열 구분

   - 표의 양쪽 끝의 파이프는 생략 가능

   - 헤더 셀을 구분할 때는 `3개 이상의 하이픈( - )`사용

   - 행을 늘릴 때는 `command + Enter` 

     ```
     | 동물 | 종류 | 다리 개수 |
     | --- | --- | ------ |
     | 사자 | 포유류 | 4개 |
     | 닭 | 조류 | 2개 |
     |도마뱀|파충류| 4개 |
     ```

     | 동물   | 종류   | 다리 개수 |
     | ------ | ------ | --------- |
     | 사자   | 포유류 | 4개       |
     | 닭     | 조류   | 2개       |
     | 도마뱀 | 파충류 | 4개       |

     

8. `강조`

   





## 3) Git

### `Git` : (분산) 버전 관리 프로그램 

#### `Git 명령어`

1. `git init`: 현재 폴더를 깃이 관리하는 폴더로 만들어 줌

   - 홈폴더에서 기입하지 X

   - ⭐최초 1번만 기입

   - ls -a로 확인 가능(.git)

     

2. `git status` : 현 상황을 보여줌



3. `git add` : 무대에 올리기

   - git add a.txt : a.txt 올리기
   - git add . : 전부 올리기

   

4. `git commit -m '메시지'` : 촬영 후 저장소로

   - git config --global user.name "Your Name"

   - git config --global user.email "You@example.com"

   - 유저명, 이메일은 최초 1회 등록하면 됨, 수정 가능

   - `git config --global --list`  : 등록된 이메일, 유저명 확인 가능

      

5. `git log` : (저장된 파일) 버전 확인

   - `git log --oneline` : 해쉬값을 알려줌 (checkout에 쓰임)

     

6. 과거물 보기

   - `git checkout + 해쉬값` : 입력한 해쉬값으로 되돌아감

   - `git checkout head~숫자` : 입력한 숫자값만큼 되돌아감

   - `git checkout master` : 원래대로 돌아옴

     ```
     8b158f5 (HEAD -> master) fifth commit - case
     23733d5 fourth commit - glass
     2a3acd8 third commit -shoe
     c85ebf8 second commit - glove
     78c98bb first commit -hat equipped
     
     git checkout 2a3acd8
     HEAD의 현재 위치는 2a3acd8 third commit -shoe
     
     git checkout master
     이전 HEAD 위치는 2a3acd8 third commit -shoe
     'master' 브랜치로 전환합니다
     
     git checkout head~3
     HEAD의 현재 위치는 c85ebf8 second commit - glove
     ```

     

7. `브릿지`

   - 브릿지 잇기 : `git remote add origin + 주소`
   - 브릿지 확인 : `git remote -v`

   

8. `올리기`

   `git push origin master`

   
