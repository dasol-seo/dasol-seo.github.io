---
layout: archive
title: "When-using-bootstrap-anchor-link-isnt-clickable"
---

### 에러 내용
> #### 브라우저 크기가 768 ~ 991px일 때 a태그 클릭이 안 된다.

### 발생한 이유
> #### 에러가 발생한 요소의 다음 요소에 col-sm-*(768 ~ 991px)클래스가 없다.

### 발생한 이유 - 자세히 보기
> #### Bootstarp version3 grid system에는 float 속성을 사용하고 있다.

####  Float의 특징
#### 부모(row) 안에 자식 요소(column1, column2)가 두 개 있고,
#### 첫 번째 요소에는 float 속성이 적용되어 있고, 두 번째 요소에는 float 속성이 적용되어 있지 않을 때

#### 1) 부모의 첫 번째 자식은 두 번째 요소가 된다.

#### 2) 자식 요소의 position값이 static인 경우 float 속성이 적용된 첫 번째 요소가 두 번째 요소보다 앞에 있다.

#### 3) 자식 요소의 position값이 static이 아닌 경우 마지막에 작성된 두 번째 요소가 첫 번째 요소보다 앞에 있다.

#### 1), 3)때문에 a태그를 클릭할 수 없다.

#### Boostrap version4부터는 flex 속성을 사용하고 있기 때문에 이와 같은 에러가 더 이상 발생하지 않는다.

### 해결방법
> #### .col-sm-* 추가

### 예시 코드
#### [Github으로 이동](https://github.com/dasol-seo/errorDiaryCode/tree/master/FRONTEND/When-using-bootstrap-anchor-link-isnt-clickable)

<br>

{% if page.comments != false %}
  {% include disqus_comments.html %}
{% endif %}
