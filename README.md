# 캐릭터 카드 토글 사이트

QR 코드로 각 캐릭터 카드에 접속하면, 터치할 때마다 카드 앞뒤면이 번갈아 나타나는 사이트입니다.

## ✨ 기능

- **첫 화면**: 캐릭터 카드 앞면 자동 표시
- **첫 번째 터치**: 카드 뒷면으로 전환
- **두 번째 터치**: 다시 앞면으로 전환
- **반복**: 터치할 때마다 앞 ↔ 뒤 번갈아가며 표시

## 📁 파일 구조

```
your-repository/
├── index.html
├── README.md
└── images/
    ├── char1-front.png (캐릭터 1 앞면)
    ├── char1-back.png  (캐릭터 1 뒷면)
    ├── char2-front.png (캐릭터 2 앞면)
    ├── char2-back.png  (캐릭터 2 뒷면)
    ├── char3-front.png
    ├── char3-back.png
    ├── char4-front.png
    ├── char4-back.png
    ├── char5-front.png
    ├── char5-back.png
    ├── char6-front.png
    ├── char6-back.png
    ├── char7-front.png
    ├── char7-back.png
    ├── char8-front.png
    └── char8-back.png
```

## 🚀 GitHub Pages 설정 방법

### 1. 이미지 준비
- 8개 캐릭터의 앞면/뒷면 이미지를 준비합니다 (총 16개)
- 파일명을 위의 구조대로 변경합니다
- PNG 또는 JPG 형식 사용 가능

### 2. 저장소에 업로드
1. GitHub 저장소에 `images` 폴더를 만듭니다
2. 16개의 이미지 파일을 `images` 폴더에 업로드합니다
3. `index.html` 파일을 저장소 루트에 업로드합니다

### 3. GitHub Pages 활성화
1. 저장소 Settings > Pages로 이동
2. Source를 "Deploy from a branch" 선택
3. Branch를 "main" (또는 "master") 선택, 폴더는 "/ (root)" 선택
4. Save 클릭

## 🔗 QR 코드 생성

각 캐릭터별 URL:
```
https://your-username.github.io/your-repository/?char=1  (캐릭터 1)
https://your-username.github.io/your-repository/?char=2  (캐릭터 2)
https://your-username.github.io/your-repository/?char=3  (캐릭터 3)
https://your-username.github.io/your-repository/?char=4  (캐릭터 4)
https://your-username.github.io/your-repository/?char=5  (캐릭터 5)
https://your-username.github.io/your-repository/?char=6  (캐릭터 6)
https://your-username.github.io/your-repository/?char=7  (캐릭터 7)
https://your-username.github.io/your-repository/?char=8  (캐릭터 8)
```

위 URL들로 각각 QR 코드를 생성하세요.

### QR 코드 생성 사이트 추천:
- https://www.qr-code-generator.com/
- https://www.qrcode-monkey.com/

## 🎨 디자인

- 전체 화면을 사용하는 심플한 디자인
- 검은색 배경
- 이미지는 화면에 맞춰 자동으로 크기 조절
- 페이드 효과로 부드러운 전환

## 📱 반응형

- 모바일, 태블릿, 데스크톱 모두 지원
- 터치 및 클릭 모두 작동
- 이미지는 화면 크기에 맞춰 자동 조절

## 🔧 동작 방식

1. QR 코드 스캔 시 각 캐릭터의 URL로 이동
2. 처음부터 해당 캐릭터의 앞면 카드 자동 표시
3. 첫 터치: 뒷면으로 전환
4. 두 번째 터치: 앞면으로 전환
5. 이후 터치: 앞 ↔ 뒤 반복

## ⚠️ 문제 해결

### 이미지가 안 보이는 경우:
1. 이미지 파일명이 정확한지 확인 (대소문자 구분)
2. 이미지가 `images` 폴더에 있는지 확인
3. GitHub Pages가 활성화되었는지 확인
4. 브라우저 캐시를 지우고 새로고침 (Ctrl+Shift+R)

### JPG 파일을 사용하는 경우:
코드는 자동으로 PNG에서 JPG로 전환을 시도하지만, 처음부터 JPG를 사용하려면:
- 이미지 파일명을 `.jpg`로 저장
- `index.html`의 다음 부분을 수정:
```javascript
const imageFront = `images/char${charNumber}-front.jpg`;
const imageBack = `images/char${charNumber}-back.jpg`;
```

## 📊 테스트 방법

1. 로컬에서 테스트:
   - `index.html?char=1`을 브라우저로 열기
   - 각 캐릭터 번호(1-8)로 테스트

2. GitHub Pages에서 테스트:
   - 각 URL을 직접 방문하여 확인
   - 모바일에서도 테스트

## 💡 팁

- 이미지 크기는 적절하게 최적화하세요 (권장: 가로 1000px 이하)
- 파일 크기가 크면 로딩이 느려질 수 있습니다
- 이미지 형식은 PNG 또는 JPG 모두 가능합니다
