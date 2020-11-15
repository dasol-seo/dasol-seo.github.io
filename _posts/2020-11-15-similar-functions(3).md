---
layout: archive
title: "Similar-functions"
---

### 비슷한 함수 정리(3) includes vs some vs every

### includes(value)
- 배열이 value를 포함하는지 판단해 boolean값을 반환한다.

``` javascript
const managerAuth = ['create', 'modify', 'delete']
const hasModifyAuth = managerAuth.includes('modify')
// hasModifyAuth: true
```

### some(callback)
- 배열 내의 하나의 요소라도 callback 함수를 통과하는지 판단해 boolean값을 반환한다.

``` javascript
const scoreList = [100, 20, 82, 99, 55]
const hasScoreHigherThan90 = scoreList.some(score => score > 90)
// hasScoreHigherThan90: true
```

### every(callback)
- 배열 내의 모든 요소가 callback 함수를 통과하는지 판단해 boolean값을 반환한다.

``` javascript
const scoreList = [100, 20, 82, 99, 55]
const hasAllScoreHigherThan90 = scoreList.every(score => score > 90)
// hasAllScoreHigherThan90: false
```