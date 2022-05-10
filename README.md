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
- Parameter 편의객체 : `th:text=${param.paramName}`
- Session 편의객체 : `th:text=$[session.dataName}`
