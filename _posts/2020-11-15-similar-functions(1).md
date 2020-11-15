---
layout: archive
title: "Similar-functions"
---

### 비슷한 함수 정리(1) map vs forEach vs reduce
### map(callback)
- 배열 내의 모든 요소에 대해 callback 함수를 호출한 결과를 모아 새로운 배열을 반환한다.

```javascript
const monthList = ['jan', 'feb', 'mar', 'apr', 'may', 'jun', 'jul', 'aug', 'sep', 'oct', 'nov', 'dec'];
const upperCaseMonthList = monthList.map(month => month.toUpperCase());
// upperCaseMonthList: ["JAN", "FEB", "MAR", "APR", "MAY", "JUN", "JUL", "AUG", "SEP", "OCT", "NOV", "DEC"]
```

### forEach(callback)
- 배열 내의 모든 요소에 대해 callback 함수를 호출한다.

``` javascript
const monthList = ['jan', 'feb', 'mar', 'apr', 'may', 'jun', 'jul', 'aug', 'sep', 'oct', 'nov', 'dec'];
const upperCaseMonthList = []

monthList.forEach(month => upperCaseMonthList.push(month.toUpperCase()));
// upperCaseMonthList: ["JAN", "FEB", "MAR", "APR", "MAY", "JUN", "JUL", "AUG", "SEP", "OCT", "NOV", "DEC"]
```

### reduce(callback, initialValue)
- 배열 내의 모든 요소에 대해 callback 함수를 호출한 후 누적된 결과값을 반환한다.

``` javascript
const monthList = ['jan', 'feb', 'mar', 'apr', 'may', 'jun', 'jul', 'aug', 'sep', 'oct', 'nov', 'dec'];
const upperCaseMonthList = monthList.reduce((acc, cur) => [...acc, cur.toUpperCase()], []);
// upperCaseMonthList: ["JAN", "FEB", "MAR", "APR", "MAY", "JUN", "JUL", "AUG", "SEP", "OCT", "NOV", "DEC"]
```