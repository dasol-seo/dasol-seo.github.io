---
layout: archive
title: "Broken-styles-when-using-styled-components-in-nextjs"
---

### 에러 내용
> #### Warning: Prop `className` did not match. Server: "sc-AzgDb hOroxl" Client: "sc-gsTCUz hyorpf"

### 발생한 이유
> #### 페이지가 새로고침되면서 서버와 클라이언트 각각의 css 클래스 이름이 동기화되지 않았다.

### 해결방법
> #### babel-plugin-styled-components 설치

#### 모든 styled component에 고유한 식별자를 추가해 서버와 클라이언트에서 각각의 다른 css 클래스 생성으로 인한 오류를 막을 수 있다.

```shell
// yarn
yarn add -D babel-plugin-styled-components 

// npm
npm install --save-dev babel-plugin-styled-components
```

```javascript
// .babelrc
{
    "presets": ["next/babel"],
    "plugins": [
        [
            "babel-plugin-styled-components",
            {
                "ssr": true,
                "minify": true,
                "transpileTemplateLiterals": true,
                // 불필요한(실행되지 않는) 코드 제거
                "pure": true,
                // css 클래스 이름을 식별하기 쉽도록 도와줌
                "displayName": true,
                // experimental
                "preprocess": false
            }
        ]
    ]
}
```

<br>

{% if page.comments != false %}
  {% include disqus_comments.html %}
{% endif %}
