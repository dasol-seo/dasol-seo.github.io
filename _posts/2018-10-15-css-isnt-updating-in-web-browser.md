---
layout: archive
title: "CSS isn't updating in web browser"
---

### 에러 내용
> #### CSS 파일 수정 후 웹 브라우저를 새로고침해도 수정된 CSS코드가 반영되지 않는다.

### 발생한 이유
> #### 캐시에 이미 같은 이름의 파일이 있기 때문에 업데이트 되지 않는다.

### 해결방법
> #### 브라우저 캐시 삭제

<br>

{% if page.comments != false %}
  {% include disqus_comments.html %}
{% endif %}
