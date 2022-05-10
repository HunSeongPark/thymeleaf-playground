# thymeleaf-playground
사이드 프로젝트를 위한 Thymeleaf 공부방

## 정리
- thymeleaf 사용 : `<html xmlns:th="http://www.thymeleaf.org">`
- text 출력 : `<span th:text=${data}></span>`
- 컨텐츠 내 직접 출력 : `<li>[[${data}]]</li>`
- text unescape 출력 : `<span th:utext=${data}></span>`
- 컨텐츠 내 unescape 직접 출력 : `<li>[(${data})]</li>`
