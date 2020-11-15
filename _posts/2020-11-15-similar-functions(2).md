---
layout: archive
title: "Similar-functions"
---

### 비슷한 함수 정리(2) filter vs find vs findIndex vs indexOf

### filter(callback)
- callback 함수를 통과한 모든 요소를 모아 새로운 배열을 반환한다.

``` javascript
const scoreList = [100, 20, 82, 99, 55]
const avgScore = Math.round((scoreList.reduce((acc, cur) => acc + cur)) / scoreList.length)
const scoreListHigherThanAvg = scoreList.filter(score => score > avgScore)
// scoreListHigherThanAvg: [100, 82, 99]
```

### find(callback)
- callback 함수를 통과한 요소들 중 첫 번째 요소를 반환한다. 그런 요소가 없다면 undefined를 반환한다.

``` javascript
const scoreList = [100, 20, 82, 99, 55]
const avgScore = Math.round((scoreList.reduce((acc, cur) => acc + cur)) / scoreList.length)
const firstScoreHigherThanAvg = scoreList.find(score => score > avgScore)
// firstScoreHigherThanAvg: 100
```

### findIndex(callback)
- callback 함수를 통과한 요소들 중 첫 번째 요소의 인덱스를 반환한다. 그런 요소가 없다면 -1을 반환한다.

``` javascript
const scoreList = [100, 20, 82, 99, 55]
const avgScore = Math.round((scoreList.reduce((acc, cur) => acc + cur)) / scoreList.length)
const firstScoreIndexHigherThanAvg = scoreList.findIndex(score => score > avgScore)
// firstScoreIndexHigherThanAvg: 0
```

### indexOf(searchElement)
- searchElement가 있는 첫 번째 요소의 인덱스를 반환한다. 그런 요소가 없다면 -1을 반환한다.

``` javascript
const myPlaylist = ['through the night', 'palette', 'knees', 'glasses', 'unlucky', 'heart', 'uh oh']
const myFavoriteSongIndex = myPlaylist.indexOf('unlucky')
// myFavoriteSongIndex: 4
```