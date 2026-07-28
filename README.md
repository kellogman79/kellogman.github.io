<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Hello Everyone!</title>

  <style>
    /* 브라우저의 기본 여백 제거 */
    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      width: 100vw;
      min-height: 100vh;

      /* 글자를 화면 중앙에 배치 */
      display: flex;
      justify-content: center;
      align-items: center;

      /* 흑백 그라데이션 */
      background: linear-gradient(
        135deg,
        #ffffff,
        #888888,
        #000000
      );

      /* 배경이 움직일 공간 확보 */
      background-size: 400% 400%;

      /* 흰색 → 회색 → 검은색 변화 반복 */
      animation: grayscaleFlash 3s ease-in-out infinite;

      font-family: Arial, sans-serif;
    }

    h1 {
      margin: 0;
      padding: 20px 30px;

      color: white;
      font-size: clamp(36px, 8vw, 90px);
      text-align: center;

      /* 배경색이 밝을 때도 글자가 보이도록 그림자 추가 */
      text-shadow:
        0 0 5px black,
        0 0 15px black,
        0 0 30px black;
    }

    @keyframes grayscaleFlash {
      0% {
        background-position: 0% 50%;
        filter: brightness(1.5);
      }

      50% {
        background-position: 100% 50%;
        filter: brightness(0.35);
      }

      100% {
        background-position: 0% 50%;
        filter: brightness(1.5);
      }
    }

    /* 움직임 감소 설정을 사용하는 방문자 보호 */
    @media (prefers-reduced-motion: reduce) {
      body {
        animation: none;
        background: linear-gradient(
          135deg,
          #ffffff,
          #888888,
          #000000
        );
      }
    }
  </style>
</head>

<body>
  <h1>Hello Everyone!</h1>
</body>
