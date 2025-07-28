### ```아래의 순서대로 실행하세요 ```

### ``` 1️⃣ Naver-Intellij-formatter 적용하기 ```

1. [IntelliJ Fomatter 다운로드](https://github.com/naver/hackday-conventions-java/blob/master/rule-config/naver-intellij-formatter.xml)
2. IntelliJ - File - Settings
3. Editor - Code Style - Java
4. Scheme 항목의 오른쪽에 있는 톱니바퀴 아이콘을 선택
5. Import Scheme → InteliJ IDEA Code Style XML을 선택
6. naver-intelij-formatter.xml 선택 후 OK

---

### ``` 2️⃣ 저장 시 마다 코딩 컨벤션 자동 적용하기```

> **기존 적용 방식은**, 소스코드 또는 패키지나 프로젝트 디렉터리를 선택 한후 Ctrl + Alt + L 을 눌러 코드 포멧터를 적용해야하는 단점이 있다.  
> 이는 귀찮거나 깜빡할 가능성이 있으므로 자동 적용 기능을 추가한다.

1. File → Settings → Tools → Actions on Save 또는 Settings
2. Save 검색해서 나온 항목을 선택
3. Reformat code(저장 시 자동으로 포맷 적용)와 Optimize imports(저장 시 사용하지 않는 import 제거) 체크 후 적용

---

### ``` 3️⃣ Check Style 적용하기 ```

> **Checkstyle**:  
> Java 소스 코드가 지정된 코딩 컨벤션을 준수하는지 확인하기 위한 정적 코드 분석 도구  
> 지정된 규칙에 어긋나는 경우 컴파일 시 경고나 에러를 띄워준다.

``` Checkstyle 플러그인 설치```

1. [naver-checkstyle-rules.xml](https://github.com/naver/hackday-conventions-java/blob/master/rule-config/naver-checkstyle-rules.xml)
2. [naver-checkstyle-suppressions.xml](https://github.com/naver/hackday-conventions-java/blob/master/rule-config/naver-checkstyle-suppressions.xml)
3. File → Settings → Plugins
4. Marketplace에 CheckStyle을 검색
5. CheckStyle-IDEA 플러그인을 설치
6. InteliJ를 재시작

``` Checkstyle 설정 ```

1. File → Settings → Tools에서 Checkstyle 항목을 선택
2. Scan scope를 (All sources) including tests로 설정
3. Treat Checkstyle errors as warnings를 체크
4. Configuration File에서 + 버튼 클릭
5. Description은 ```Naver Checkstyle Rules``` 지정
6. Use a Local Checkstyle File을 선택 Browse 클릭
7. naver-checkstyle-rules.xml를 지정후 Next
8. suppressionFile 변수를 설정하라는 창이 뜨면 Value에 ```naver-checkstyle-suppressions.xml```를 입력하고 Next 버튼
9. Naver Checkstyle Rules의 Active를 체크