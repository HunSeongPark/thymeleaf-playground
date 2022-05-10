# thymeleaf-playground
사이드 프로젝트를 위한 Thymeleaf 공부방

## 정리
- thymeleaf 사용 : `<html xmlns:th="http://www.thymeleaf.org">`
- text 출력 : `th:text=${...}`
- 컨텐츠 내 직접 출력 : `[[${...}]]`
- text unescape 출력 : `th:utext=${...}`
- 컨텐츠 내 unescape 직접 출력 : `[(${...})]`
- 태그 내 인라인 타임리프 해석 off : `th:inline="none"`
- Object, List, Map 타입 SpringEL 표현식
- <img width="311" alt="image" src="https://user-images.githubusercontent.com/71416677/167582875-baa75f26-fe40-47ef-9d6d-b5b8523aea2d.png">
- 지역변수 사용 : `th:with="first=${user}"`
- Parameter 편의객체 : `th:text="${param.paramName}"`
- Session 편의객체 : `th:text="${session.dataName}"`
- link : `th:href="@{/hello}"`
- link (query parameter) : `th:href="@{/hello(param=${...})}"`
- link (path variable) : `th:href="@{/hello/{path}(path=${...})}"`
- link (query parameter + path variable) : `th:href="@{/hello/{path}(path=${...}, param=${...})}"`
- Literal : `th:text="'hello world!'"` `th:text="'hello ' + 'world!'"` `th:text="'hello ' + ${data}"`
  - Literal의 경우 공백 없는 문자열을 제외하고는 ' '를 붙여야 한다.
  - Literal 대체 문법(|..|)을 통해 템플릿처럼 편리하게 사용 가능 `th:text="|hello ${data}|"`
- Operation (산술 연산)
  - 10 + 2 : `th:text="10 + 2"`
  - 10 % 2 == 0 : `th:text="10 % 2 == 0"`
- Operation (비교 연산)
  - 1 > 10 : `th:text="1 &gt; 10"` `th:text="1 gt 10"`
  - 1 >= 10 : `th:text="1 >= 10"` `th:text="1 ge 10"`
  - 1 == 10 : `th:text="1 == 10"`
- Operation (조건식)
  - (10 % 2 == 0) ? '짝수' : '홀수' : `th:text="(10 % 2 == 0) ? '짝수' : '홀수'"`
- Operation (Elvis 연산자 ?:) : `th:text="${data} ?: '데이터가 없습니다.'"`
- Operation (No-Operation _ ) : `th:text="${data} ?: _"`
- class 속성 뒤에 이어붙이기 : `th:attrappend="class='add'"`
- class 속성 앞에 이어붙이기 : `th:attrprepend="class='add'"`
- class 속성 추가 : `th:classappend="add"`
- checked 처리 : `th:checked="true|false"`
- 반복 : `th:each="user : ${users}"`
