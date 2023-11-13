# IDEATE 연동 가이드

## 준비 사항
IDEATE 콘솔에서 발급 혹은 IDEATE 관리자에게 발급 받은 키가 필요합니다.

## Script 방식
배너를 노출하기 위해 아래와 같이 스크립트를 삽입해주세요.

```
<script src="https://id8.co.kr/pub.js?key={key}"></script>
```

### 파라미터

| Parameter | 설명 | 예시 | 필수 |
|-|-|-|:-:|
| canvasId | 광고를 구현할 위치의 컨테이너 | div#id | ○ |
| width | 광고 가로 사이즈 | 240px, 100% | ○ |
| height | 광고 세로 사이즈 | 50px, auto | X |
| affilationId | 하위 ID 혹은 구분자 | subpub-1234 | X |

### 예시
```html
<html>
  <head></head>
  <body>
    ... contents ...

    <script src="https://id8.co.kr/pub.js?key={key}"></script>
    <script>
      $(document).ready(function() {
        ID8.init();

        ID8.banner([
          {canvasId: 'div#id', width: '240px', height: '50px', affilationId: '하위 ID'}
        ]);
        // or

        ID8.banner({canvasId: 'div#id', width: '240px', height: '50px', affilationId: '하위 ID'});
      });
    </script>
  </body>
</html>
```

