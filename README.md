# AI는 이미지를 어떻게 구분할까?

네 가지 분류 문제로 이미지 분류를 처음부터 따라가는 인터랙티브 해설 시리즈입니다.
이름 있는 변수로 가르는 물고기에서 출발해, 사진이 숫자 행렬이 되는 과정, 필터와 CNN, 그리고 사람도 헷갈리는 치와와와 머핀까지 다룹니다.

**바로 보기:** https://adminmrobo.github.io/AI_image_classification/

글 · 안상선 ((주)M-Robo 대표)

## 구성

| 편 | 제목 | 다루는 내용 |
|---|---|---|
| [4-1](https://adminmrobo.github.io/AI_image_classification/4-1_bream_smelt.html) | 도미 vs 빙어 — 변수와 특징, 무엇이 다를까 | 변수와 특징, 샘플·특징·타겟, 결정 트리 규칙, 퍼셉트론, SVM, k-NN과 표준화 |
| [4-2](https://adminmrobo.github.io/AI_image_classification/4-2_cat_human.html) | 고양이 vs 사람 — 사진은 숫자 행렬이다 | 픽셀과 행렬, 픽셀 거리의 함정, 합성곱과 필터, 사람이 정한 특징(얼굴 검출·특징점) |
| [4-3](https://adminmrobo.github.io/AI_image_classification/4-3_cat_dog.html) | 고양이 vs 강아지 — 층을 쌓아 좌표를 바꾼다 | 분류 경계와 은닉층, CNN 구조, 소프트맥스와 학습, 데이터 증강과 Attentive CutMix |
| [4-4](https://adminmrobo.github.io/AI_image_classification/4-4_chihuahua_muffin.html) | 치와와 vs 머핀 — 저수준 특징은 속고, 고수준 특징이 가른다 | 저수준·고수준 특징, 해상도, 픽셀 규칙 대 패턴, 지름길 학습과 모델의 한계 |

순서대로 읽기를 권하지만, 각 편은 따로 읽어도 됩니다.

## 각 편에 들어 있는 것

- 직접 조작하는 실습과 움직이는 다이어그램 (픽셀 돋보기, 필터 실험실, 3차원 분류 경계, CutMix 등)
- 초보자를 위한 풀이와 섹션별 확인 문제
- **Colab 코드 2개** — 복사, `.py` 내려받기, 노트북(`.ipynb`) 내려받기를 지원합니다. Colab 기본 라이브러리와 내장 데이터만 쓰며, 페이지에 실제 실행 결과를 실었습니다.
- AI 응용 프롬프트, 용어 정리, 비유 모음, 레퍼런스
- 교육자를 위한 TIP (운영안, 흔한 오해, 확인 문제, Colab 과제)

## 파일

```
index.html                 시리즈 목록
4-1_bream_smelt.html       도미 vs 빙어
4-2_cat_human.html         고양이 vs 사람
4-3_cat_dog.html           고양이 vs 강아지
4-4_chihuahua_muffin.html  치와와 vs 머핀
```

각 HTML은 사진·데이터·스크립트를 파일 안에 담고 있어 빌드 과정이 없습니다. 파일을 브라우저로 열기만 하면 됩니다(글꼴은 Google Fonts에서 불러오므로 인터넷이 없으면 기본 글꼴로 보입니다). 편끼리 이어지는 링크는 다섯 파일이 같은 폴더에 있을 때 작동하므로 파일 이름을 바꾸지 마세요.

## 데이터와 이미지

- 고양이·사람·강아지·치와와·머핀 이미지와 마무리 장면 그림은 저자가 직접 만든 것입니다.
- 물고기 길이·무게: Kaggle Fish Market 데이터셋의 도미·빙어 값 (박해선, 『혼자 공부하는 머신러닝+딥러닝』 예제 코드, MIT 라이선스). 물고기 데이터 머신러닝은 [Fish Market Data로 쉽게 따라하는 머신러닝](https://adminmrobo.github.io/Fish_Market_Data_Machine_Learning/)에서 자세히 다룹니다.
- Colab 코드는 scikit-learn 내장 손글씨 숫자(load_digits)와 scikit-image 내장 사진을 씁니다.
- 일부 그림과 값은 설명용 모형입니다. 각 편 푸터의 "설명용 모형인 것"에 무엇이 실제 계산이고 무엇이 예시인지 적어 두었습니다.

## 라이선스

이 저작물은 [크리에이티브 커먼즈 저작자표시-비영리 4.0 국제 라이선스(CC BY-NC 4.0)](https://creativecommons.org/licenses/by-nc/4.0/deed.ko)로 공개합니다.
비상업적 목적에 한해 자유롭게 공유하고 고쳐 쓸 수 있으며, **출처는 반드시 표기**해야 합니다.

출처 표기 예: 안상선, 「AI는 이미지를 어떻게 구분할까? · 4-1 도미 vs 빙어」, AI Model Review.
