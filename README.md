<a id="top"></a>

**🌐 [한국어](#ko) · [English](#en) · [中文](#zh) · [日本語](#ja) · [Oʻzbekcha](#uz) · [Русский](#ru)**

---

<a id="ko"></a>

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

## 언어

모든 페이지는 **한국어(기본)**, 영어, 중국어, 일본어, 우즈베크어, 러시아어로 읽을 수 있습니다.

- 페이지 맨 위 메뉴의 🌐 언어 선택 상자와, 그 아래 언어 배너에서 언제든 바꿀 수 있습니다. 보던 편과 위치를 유지한 채 같은 편의 다른 언어판으로 이동합니다.
- 처음 방문할 때는 브라우저 언어를 보고 자동으로 맞는 언어판을 엽니다(브라우저가 한국어이거나 지원하지 않는 언어면 한국어판). 한 번 고른 언어는 이 기기에 기억됩니다.
- 한국어판 주소 뒤에 `?lang=ko`를 붙이면 자동 전환 없이 한국어판을 엽니다.

## 각 편에 들어 있는 것

- 직접 조작하는 실습과 움직이는 다이어그램 (픽셀 돋보기, 필터 실험실, 3차원 분류 경계, CutMix 등)
- 초보자를 위한 풀이와 섹션별 확인 문제
- **Colab 코드 2개** — 복사, `.py` 내려받기, 노트북(`.ipynb`) 내려받기를 지원합니다. Colab 기본 라이브러리와 내장 데이터만 쓰며, 페이지에 실제 실행 결과를 실었습니다.
- AI 응용 프롬프트, 용어 정리, 비유 모음, 레퍼런스
- 교육자를 위한 TIP (운영안, 흔한 오해, 확인 문제, Colab 과제)

## 파일

```
index.html                 시리즈 첫 화면 (긴급 미션 브리핑과 미션 네 개) — 한국어
4-1_bream_smelt.html       도미 vs 빙어
4-2_cat_human.html         고양이 vs 사람
4-3_cat_dog.html           고양이 vs 강아지
4-4_chihuahua_muffin.html  치와와 vs 머핀
en/  zh/  ja/  uz/  ru/    같은 다섯 파일의 영어·중국어·일본어·우즈베크어·러시아어판
```

각 HTML은 사진·데이터·스크립트를 파일 안에 담고 있어 빌드 과정이 없습니다. 파일을 브라우저로 열기만 하면 됩니다(글꼴은 Google Fonts에서 불러오므로 인터넷이 없으면 기본 글꼴로 보입니다). 편끼리, 언어끼리 이어지는 링크는 폴더 구조가 위와 같을 때 작동하므로 파일과 폴더 이름을 바꾸지 마세요.

## 데이터와 이미지

- 고양이·사람·강아지·치와와·머핀 이미지와 마무리 장면 그림은 저자가 직접 만든 것입니다.
- 물고기 길이·무게: Kaggle Fish Market 데이터셋의 도미·빙어 값 (박해선, 『혼자 공부하는 머신러닝+딥러닝』 예제 코드, MIT 라이선스). 물고기 데이터 머신러닝은 [Fish Market Data로 쉽게 따라하는 머신러닝](https://adminmrobo.github.io/Fish_Market_Data_Machine_Learning/)에서 자세히 다룹니다.
- Colab 코드는 scikit-learn 내장 손글씨 숫자(load_digits)와 scikit-image 내장 사진을 씁니다.
- 일부 그림과 값은 설명용 모형입니다. 각 편 푸터의 "설명용 모형인 것"에 무엇이 실제 계산이고 무엇이 예시인지 적어 두었습니다.

## 라이선스

이 저작물은 [크리에이티브 커먼즈 저작자표시-비영리 4.0 국제 라이선스(CC BY-NC 4.0)](https://creativecommons.org/licenses/by-nc/4.0/deed.ko)로 공개합니다.
비상업적 목적에 한해 자유롭게 공유하고 고쳐 쓸 수 있으며, **출처는 반드시 표기**해야 합니다.

출처 표기 예: 안상선, 「AI는 이미지를 어떻게 구분할까? · 4-1 도미 vs 빙어」, AI Model Review.

[↑ 맨 위로](#top)

---

<a id="en"></a>

# How Does AI Tell Images Apart?

An interactive explainer series that walks through image classification from scratch using four classification problems.
It starts with fish that can be separated by named variables, then covers how a photo becomes a matrix of numbers, filters and CNNs, and finally chihuahuas and muffins — a pair that even confuses people.

**Read online:** https://adminmrobo.github.io/AI_image_classification/en/

By Sangsun Ahn (CEO, M-Robo Inc.)

## Contents

| Part | Title | Topics |
|---|---|---|
| [4-1](https://adminmrobo.github.io/AI_image_classification/en/4-1_bream_smelt.html) | Bream vs Smelt — Variables and Features: What’s the Difference? | Variables and features; samples, features and targets; decision-tree rules; perceptron; SVM; k-NN and standardization |
| [4-2](https://adminmrobo.github.io/AI_image_classification/en/4-2_cat_human.html) | Cat vs Human — A Photo Is a Matrix of Numbers | Pixels and matrices, the pixel-distance trap, convolution and filters, hand-crafted features (face detection, landmarks) |
| [4-3](https://adminmrobo.github.io/AI_image_classification/en/4-3_cat_dog.html) | Cat vs Dog — Stack Layers, Change the Coordinates | Decision boundaries and hidden layers, CNN architecture, softmax and training, data augmentation and Attentive CutMix |
| [4-4](https://adminmrobo.github.io/AI_image_classification/en/4-4_chihuahua_muffin.html) | Chihuahua vs Muffin — Low-Level Features Get Fooled, High-Level Features Decide | Low- and high-level features, resolution, pixel rules vs patterns, shortcut learning and the limits of models |

Reading in order is recommended, but each part also stands on its own.

## Languages

Every page is available in **Korean (default)**, English, Chinese, Japanese, Uzbek and Russian.

- Switch at any time with the 🌐 language selector in the top menu or the language banner just below it. You stay on the same part and position, in the other language.
- On your first visit, the page follows your browser language automatically (Korean if your browser is set to Korean or to an unsupported language). The language you pick is remembered on your device.
- Add `?lang=ko` to a Korean page URL to open it without automatic switching.

## What each part includes

- Hands-on exercises and animated diagrams (pixel magnifier, filter lab, 3D decision boundaries, CutMix and more)
- Beginner-friendly explanations and a quiz for each section
- **Two Colab notebooks** — copy, download as `.py`, or download as a notebook (`.ipynb`). They use only Colab's built-in libraries and datasets, and the page shows their real output.
- AI prompts for applying the ideas, a glossary, a collection of analogies, and references
- Tips for educators (lesson plans, common misconceptions, quiz questions, Colab assignments)

## Files

```
index.html                 Series home (urgent mission briefing and the four missions) — Korean
4-1_bream_smelt.html       Bream vs Smelt
4-2_cat_human.html         Cat vs Human
4-3_cat_dog.html           Cat vs Dog
4-4_chihuahua_muffin.html  Chihuahua vs Muffin
en/  zh/  ja/  uz/  ru/    The same five files in English, Chinese, Japanese, Uzbek and Russian
```

Each HTML file contains its images, data and scripts, so there is no build step — just open the file in a browser (fonts load from Google Fonts, so without internet you will see default fonts). Links between parts and between languages work when the folder structure is as above, so please don't rename the files or folders.

## Data and images

- The cat, human, dog, chihuahua and muffin images and the closing-scene illustration were created by the author.
- Fish length and weight: bream and smelt values from the Kaggle Fish Market dataset (example code from Haesun Park's *Hands-On Machine Learning & Deep Learning (혼자 공부하는 머신러닝+딥러닝)*, MIT License). Machine learning with the fish data is covered in detail in [Easy Machine Learning with Fish Market Data](https://adminmrobo.github.io/Fish_Market_Data_Machine_Learning/) (Korean).
- The Colab code uses scikit-learn's built-in handwritten digits (load_digits) and scikit-image's built-in photos.
- Some figures and values are illustrative models. The "What is an illustrative model" note in each part's footer says what is a real computation and what is an example.

## License

This work is published under the [Creative Commons Attribution-NonCommercial 4.0 International License (CC BY-NC 4.0)](https://creativecommons.org/licenses/by-nc/4.0/deed.en).
You may share and adapt it freely for non-commercial purposes, but **attribution is required**.

Attribution example: Sangsun Ahn, "How Does AI Tell Images Apart? · 4-1 Bream vs Smelt", AI Model Review.

[↑ Back to top](#top)

---

<a id="zh"></a>

# AI 如何区分图像？

一套交互式讲解系列，通过四个分类问题，从零开始带你了解图像分类。
从可以用有名称的变量区分的鱼出发，依次讲解照片如何变成数字矩阵、滤波器与 CNN，最后是连人都会看错的吉娃娃和松饼。

**在线阅读：** https://adminmrobo.github.io/AI_image_classification/zh/

作者 · Sangsun Ahn（M-Robo 株式会社 代表）

## 目录

| 篇 | 标题 | 内容 |
|---|---|---|
| [4-1](https://adminmrobo.github.io/AI_image_classification/zh/4-1_bream_smelt.html) | 鲷鱼 vs 胡瓜鱼——变量和特征有什么不同？ | 变量与特征，样本·特征·目标，决策树规则，感知机，SVM，k-NN 与标准化 |
| [4-2](https://adminmrobo.github.io/AI_image_classification/zh/4-2_cat_human.html) | 猫 vs 人——照片就是数字矩阵 | 像素与矩阵，像素距离的陷阱，卷积与滤波器，人工设计的特征（人脸检测·特征点） |
| [4-3](https://adminmrobo.github.io/AI_image_classification/zh/4-3_cat_dog.html) | 猫 vs 狗——叠加层来改变坐标 | 分类边界与隐藏层，CNN 结构，Softmax 与训练，数据增强与 Attentive CutMix |
| [4-4](https://adminmrobo.github.io/AI_image_classification/zh/4-4_chihuahua_muffin.html) | 吉娃娃 vs 松饼——低层特征会被骗，高层特征来区分 | 低层·高层特征，分辨率，像素规则与模式，捷径学习与模型的局限 |

建议按顺序阅读，但每一篇也可以单独阅读。

## 语言

所有页面均提供 **韩语（默认）**、英语、中文、日语、乌兹别克语和俄语版本。

- 可随时通过页面顶部菜单中的 🌐 语言选择框或其下方的语言横幅切换，并停留在同一篇的同一位置。
- 首次访问时会根据浏览器语言自动打开对应版本（浏览器为韩语或不支持的语言时显示韩语版）。选择过的语言会记住在本设备上。
- 在韩语版网址后加上 `?lang=ko`，即可不自动切换、直接打开韩语版。

## 每篇包含的内容

- 可亲手操作的练习和动态图示（像素放大镜、滤波器实验室、三维分类边界、CutMix 等）
- 面向初学者的讲解和每节的检验题
- **2 段 Colab 代码** —— 支持复制、下载 `.py`、下载笔记本（`.ipynb`）。只使用 Colab 自带的库和内置数据，页面中附有实际运行结果。
- AI 应用提示词、术语表、比喻合集、参考文献
- 给教师的 TIP（授课方案、常见误解、检验题、Colab 作业）

## 文件

```
index.html                 系列首页（紧急任务简报和四个任务）—— 韩语
4-1_bream_smelt.html       鲷鱼 vs 胡瓜鱼
4-2_cat_human.html         猫 vs 人
4-3_cat_dog.html           猫 vs 狗
4-4_chihuahua_muffin.html  吉娃娃 vs 松饼
en/  zh/  ja/  uz/  ru/    以上五个文件的英语·中文·日语·乌兹别克语·俄语版
```

每个 HTML 文件都内含图片、数据和脚本，无需构建，用浏览器直接打开即可（字体从 Google Fonts 加载，没有网络时会显示默认字体）。篇与篇、语言与语言之间的链接在上述文件夹结构下才能正常工作，请不要更改文件名和文件夹名。

## 数据与图片

- 猫、人、狗、吉娃娃、松饼的图片和结尾场景插图均由作者本人制作。
- 鱼的长度·重量：Kaggle Fish Market 数据集中鲷鱼和胡瓜鱼的数值（朴海善《独自学习机器学习+深度学习（혼자 공부하는 머신러닝+딥러닝）》示例代码，MIT 许可证）。用鱼类数据做机器学习的详细内容见 [用 Fish Market Data 轻松学机器学习](https://adminmrobo.github.io/Fish_Market_Data_Machine_Learning/)（韩语）。
- Colab 代码使用 scikit-learn 内置的手写数字（load_digits）和 scikit-image 内置的照片。
- 部分图示和数值是说明用的模型。每篇页脚的“哪些是说明用模型”中写明了哪些是实际计算、哪些是示例。

## 许可证

本作品采用 [知识共享 署名-非商业性使用 4.0 国际许可协议（CC BY-NC 4.0）](https://creativecommons.org/licenses/by-nc/4.0/deed.zh-hans) 发布。
仅限非商业目的，可自由分享和改编，但**必须注明出处**。

出处标注示例：Sangsun Ahn，《AI 如何区分图像？· 4-1 鲷鱼 vs 胡瓜鱼》，AI Model Review。

[↑ 返回顶部](#top)

---

<a id="ja"></a>

# AIはどうやって画像を見分けるのか？

4つの分類問題を通して、画像分類を基礎からたどるインタラクティブな解説シリーズです。
名前のある変数で分けられる魚から始まり、写真が数値の行列になる過程、フィルターとCNN、そして人でも見間違えるチワワとマフィンまでを扱います。

**オンラインで読む：** https://adminmrobo.github.io/AI_image_classification/ja/

文 · アン・サンソン（Sangsun Ahn、M-Robo株式会社 代表）

## 構成

| 編 | タイトル | 扱う内容 |
|---|---|---|
| [4-1](https://adminmrobo.github.io/AI_image_classification/ja/4-1_bream_smelt.html) | タイ vs ワカサギ — 変数と特徴、何が違うのか | 変数と特徴、サンプル・特徴・ターゲット、決定木のルール、パーセプトロン、SVM、k-NNと標準化 |
| [4-2](https://adminmrobo.github.io/AI_image_classification/ja/4-2_cat_human.html) | ネコ vs ヒト — 写真は数の行列である | ピクセルと行列、ピクセル距離の落とし穴、畳み込みとフィルター、人が決めた特徴（顔検出・特徴点） |
| [4-3](https://adminmrobo.github.io/AI_image_classification/ja/4-3_cat_dog.html) | ネコ vs イヌ — 層を重ねて座標を変える | 分類境界と隠れ層、CNNの構造、ソフトマックスと学習、データ拡張とAttentive CutMix |
| [4-4](https://adminmrobo.github.io/AI_image_classification/ja/4-4_chihuahua_muffin.html) | チワワ vs マフィン — 低レベル特徴はだまされ、高レベル特徴が見分ける | 低レベル・高レベル特徴、解像度、ピクセルルール対パターン、ショートカット学習とモデルの限界 |

順番に読むことをおすすめしますが、各編は単独でも読めます。

## 言語

すべてのページを **韓国語（標準）**、英語、中国語、日本語、ウズベク語、ロシア語で読めます。

- ページ最上部メニューの 🌐 言語選択ボックスや、その下の言語バナーからいつでも切り替えられます。同じ編の同じ位置のまま、別の言語版に移動します。
- 初めて訪れたときは、ブラウザの言語に合わせて自動で対応する言語版を開きます（ブラウザが韓国語か未対応の言語なら韓国語版）。一度選んだ言語はこの端末に記憶されます。
- 韓国語版のURLの末尾に `?lang=ko` を付けると、自動切り替えなしで韓国語版を開きます。

## 各編に含まれるもの

- 実際に操作できる実習と動く図解（ピクセル拡大鏡、フィルター実験室、3次元の分類境界、CutMixなど）
- 初心者向けの解説とセクションごとの確認問題
- **Colabコード2つ** ― コピー、`.py` のダウンロード、ノートブック（`.ipynb`）のダウンロードに対応。Colab標準のライブラリと内蔵データだけを使い、実際の実行結果をページに載せています。
- AI応用プロンプト、用語集、たとえ集、参考文献
- 教育者向けTIP（運営案、よくある誤解、確認問題、Colab課題）

## ファイル

```
index.html                 シリーズのトップ（緊急ミッションのブリーフィングと4つのミッション）― 韓国語
4-1_bream_smelt.html       タイ vs ワカサギ
4-2_cat_human.html         ネコ vs ヒト
4-3_cat_dog.html           ネコ vs イヌ
4-4_chihuahua_muffin.html  チワワ vs マフィン
en/  zh/  ja/  uz/  ru/    同じ5ファイルの英語・中国語・日本語・ウズベク語・ロシア語版
```

各HTMLは写真・データ・スクリプトをファイル内に含んでいるため、ビルド作業は不要です。ブラウザでファイルを開くだけで読めます（フォントはGoogle Fontsから読み込むため、インターネットがないと標準フォントで表示されます）。編どうし・言語どうしをつなぐリンクは上記のフォルダー構成で動作するので、ファイル名とフォルダー名は変えないでください。

## データと画像

- ネコ・人・イヌ・チワワ・マフィンの画像と締めくくりの場面のイラストは、著者が自ら制作したものです。
- 魚の体長・体重：Kaggle Fish Marketデータセットのタイ・ワカサギの値（パク・ヘソン『独学 機械学習＋ディープラーニング（혼자 공부하는 머신러닝+딥러닝）』のサンプルコード、MITライセンス）。魚のデータを使った機械学習は[Fish Market Dataでやさしく学ぶ機械学習](https://adminmrobo.github.io/Fish_Market_Data_Machine_Learning/)（韓国語）で詳しく扱っています。
- Colabコードはscikit-learn内蔵の手書き数字（load_digits）とscikit-image内蔵の写真を使います。
- 一部の図と値は説明用のモデルです。各編フッターの「説明用モデルであるもの」に、何が実際の計算で何が例なのかを記しています。

## ライセンス

この著作物は[クリエイティブ・コモンズ 表示-非営利 4.0 国際ライセンス（CC BY-NC 4.0）](https://creativecommons.org/licenses/by-nc/4.0/deed.ja)で公開しています。
非営利目的に限り自由に共有・改変できますが、**出典の表示が必須**です。

出典表示の例：アン・サンソン「AIはどうやって画像を見分けるのか？ · 4-1 タイ vs ワカサギ」、AI Model Review。

[↑ トップへ](#top)

---

<a id="uz"></a>

# AI tasvirlarni qanday farqlaydi?

Toʻrtta tasniflash masalasi orqali tasvirlarni tasniflashni boshidan oʻrgatadigan interaktiv tushuntirish turkumi.
Nomlangan oʻzgaruvchilar bilan ajratiladigan baliqlardan boshlab, rasm qanday qilib sonlar matritsasiga aylanishi, filtrlar va CNN, va nihoyat odamlar ham adashtiradigan chixuaxua va maffingacha boʻlgan mavzular yoritiladi.

**Onlayn oʻqish:** https://adminmrobo.github.io/AI_image_classification/uz/

Muallif · Sangsun Ahn (M-Robo Inc. rahbari)

## Tarkibi

| Qism | Sarlavha | Mavzular |
|---|---|---|
| [4-1](https://adminmrobo.github.io/AI_image_classification/uz/4-1_bream_smelt.html) | Leshch vs koryushka — oʻzgaruvchi va belgi: farqi nimada? | Oʻzgaruvchi va belgi; namuna, belgi va nishon; qaror daraxti qoidalari; perseptron; SVM; k-NN va standartlashtirish |
| [4-2](https://adminmrobo.github.io/AI_image_classification/uz/4-2_cat_human.html) | Mushuk vs odam — rasm bu sonlar matritsasi | Piksellar va matritsalar, piksel masofasi tuzogʻi, svertka va filtrlar, inson belgilagan belgilar (yuzni aniqlash, tayanch nuqtalar) |
| [4-3](https://adminmrobo.github.io/AI_image_classification/uz/4-3_cat_dog.html) | Mushuk vs kuchukcha — qatlamlarni qoʻyib, koordinatalarni oʻzgartiramiz | Tasniflash chegarasi va yashirin qatlamlar, CNN tuzilishi, softmax va oʻqitish, maʼlumotlarni koʻpaytirish va Attentive CutMix |
| [4-4](https://adminmrobo.github.io/AI_image_classification/uz/4-4_chihuahua_muffin.html) | Chixuaxua vs maffin — quyi darajali belgilar aldanadi, yuqori darajali belgilar ajratadi | Quyi va yuqori darajali belgilar, ruxsat, piksel qoidasi va naqsh, “qisqa yoʻl” bilan oʻrganish va modelning cheklovlari |

Tartib bilan oʻqish tavsiya etiladi, lekin har bir qismni alohida ham oʻqish mumkin.

## Tillar

Barcha sahifalar **koreys (asosiy)**, ingliz, xitoy, yapon, oʻzbek va rus tillarida mavjud.

- Sahifaning eng yuqorisidagi menyudagi 🌐 til tanlash oynasi yoki uning ostidagi til banneri orqali istalgan vaqtda almashtirish mumkin. Oʻsha qism va oʻsha joyda qolgan holda boshqa til versiyasiga oʻtasiz.
- Birinchi tashrifda sahifa brauzer tiliga qarab mos versiyani avtomatik ochadi (brauzer koreyscha yoki qoʻllab-quvvatlanmaydigan tilda boʻlsa — koreyscha versiya). Bir marta tanlangan til shu qurilmada eslab qolinadi.
- Koreyscha versiya manziliga `?lang=ko` qoʻshilsa, avtomatik almashtirishsiz koreyscha versiya ochiladi.

## Har bir qismda nimalar bor

- Qoʻlda boshqariladigan mashqlar va harakatlanuvchi diagrammalar (piksel lupasi, filtr laboratoriyasi, uch oʻlchamli tasniflash chegarasi, CutMix va boshqalar)
- Yangi boshlovchilar uchun tushuntirishlar va har bir boʻlim uchun tekshiruv savollari
- **Ikkita Colab kodi** — nusxalash, `.py` yuklab olish va daftar (`.ipynb`) yuklab olish mumkin. Faqat Colab’ning standart kutubxonalari va ichki maʼlumotlaridan foydalanadi, sahifada haqiqiy natijalar keltirilgan.
- SI’ni qoʻllash uchun promptlar, atamalar lugʻati, oʻxshatishlar toʻplami, manbalar
- Oʻqituvchilar uchun TIP (dars rejasi, keng tarqalgan xato tushunchalar, tekshiruv savollari, Colab topshiriqlari)

## Fayllar

```
index.html                 Turkumning bosh sahifasi (shoshilinch topshiriq brifingi va toʻrtta topshiriq) — koreyscha
4-1_bream_smelt.html       Leshch vs koryushka
4-2_cat_human.html         Mushuk vs odam
4-3_cat_dog.html           Mushuk vs kuchukcha
4-4_chihuahua_muffin.html  Chixuaxua vs maffin
en/  zh/  ja/  uz/  ru/    Shu besh faylning ingliz, xitoy, yapon, oʻzbek va rus tilidagi versiyalari
```

Har bir HTML fayl rasmlar, maʼlumotlar va skriptlarni oʻz ichiga oladi, shuning uchun yigʻish (build) jarayoni kerak emas — faylni brauzerda ochish kifoya (shriftlar Google Fonts’dan yuklanadi, internet boʻlmasa standart shrift koʻrinadi). Qismlar va tillar orasidagi havolalar yuqoridagi papka tuzilishida ishlaydi, shuning uchun fayl va papka nomlarini oʻzgartirmang.

## Maʼlumotlar va tasvirlar

- Mushuk, odam, it, chixuaxua va maffin tasvirlari hamda yakuniy sahna rasmini muallifning oʻzi yaratgan.
- Baliqlarning uzunligi va ogʻirligi: Kaggle Fish Market maʼlumotlar toʻplamidagi lesh va koryushka qiymatlari (Pak Xesonning “Mustaqil oʻrganiladigan mashinali oʻqitish + chuqur oʻqitish (혼자 공부하는 머신러닝+딥러닝)” kitobidagi misol kodi, MIT litsenziyasi). Baliq maʼlumotlari bilan mashinali oʻqitish [Fish Market Data bilan oson mashinali oʻqitish](https://adminmrobo.github.io/Fish_Market_Data_Machine_Learning/) (koreyscha) sahifasida batafsil yoritilgan.
- Colab kodi scikit-learn’ning ichki qoʻlyozma raqamlari (load_digits) va scikit-image’ning ichki rasmlaridan foydalanadi.
- Baʼzi rasmlar va qiymatlar tushuntirish uchun model hisoblanadi. Har bir qism pastki qismidagi “Tushuntirish uchun model boʻlganlar” boʻlimida nima haqiqiy hisob va nima misol ekani yozilgan.

## Litsenziya

Ushbu asar [Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)](https://creativecommons.org/licenses/by-nc/4.0/deed.uz) litsenziyasi ostida eʼlon qilingan.
Faqat notijorat maqsadlarda erkin tarqatish va oʻzgartirish mumkin, lekin **manbani koʻrsatish shart**.

Manba koʻrsatish namunasi: Sangsun Ahn, “AI tasvirlarni qanday farqlaydi? · 4-1 Leshch vs koryushka”, AI Model Review.

[↑ Yuqoriga](#top)

---

<a id="ru"></a>

# Как ИИ различает изображения?

Интерактивная серия объяснений, которая на четырёх задачах классификации шаг за шагом знакомит с классификацией изображений.
Она начинается с рыб, которых можно разделить по именованным переменным, затем показывает, как фотография превращается в матрицу чисел, рассказывает о фильтрах и CNN и заканчивается чихуахуа и маффинами — парой, которую путают даже люди.

**Читать онлайн:** https://adminmrobo.github.io/AI_image_classification/ru/

Автор · Сансун Ан (Sangsun Ahn), генеральный директор M-Robo Inc.

## Содержание

| Часть | Название | Темы |
|---|---|---|
| [4-1](https://adminmrobo.github.io/AI_image_classification/ru/4-1_bream_smelt.html) | Лещ vs корюшка — переменные и признаки: в чём разница? | Переменные и признаки; объекты, признаки и целевая переменная; правила дерева решений; перцептрон; SVM; k-NN и стандартизация |
| [4-2](https://adminmrobo.github.io/AI_image_classification/ru/4-2_cat_human.html) | Кошка vs человек — фотография как матрица чисел | Пиксели и матрицы, ловушка пиксельного расстояния, свёртка и фильтры, признаки, заданные человеком (детекция лиц, ключевые точки) |
| [4-3](https://adminmrobo.github.io/AI_image_classification/ru/4-3_cat_dog.html) | Кошка vs собака — складываем слои и меняем координаты | Граница классов и скрытые слои, архитектура CNN, softmax и обучение, аугментация данных и Attentive CutMix |
| [4-4](https://adminmrobo.github.io/AI_image_classification/ru/4-4_chihuahua_muffin.html) | Чихуахуа vs маффин — низкоуровневые признаки обманываются, высокоуровневые различают | Низко- и высокоуровневые признаки, разрешение, пиксельные правила против паттернов, обучение по «короткому пути» и ограничения моделей |

Рекомендуем читать по порядку, но каждую часть можно читать и отдельно.

## Языки

Все страницы доступны на **корейском (по умолчанию)**, английском, китайском, японском, узбекском и русском языках.

- Переключить язык можно в любой момент — через 🌐 список выбора языка в верхнем меню или языковой баннер под ним. Вы останетесь в той же части и на том же месте, но в другой языковой версии.
- При первом посещении страница автоматически открывает версию на языке браузера (корейскую — если браузер на корейском или на неподдерживаемом языке). Выбранный язык запоминается на этом устройстве.
- Добавьте `?lang=ko` к адресу корейской страницы, чтобы открыть её без автоматического переключения.

## Что есть в каждой части

- Интерактивные упражнения и анимированные схемы (пиксельная лупа, лаборатория фильтров, трёхмерная граница классов, CutMix и др.)
- Пояснения для начинающих и проверочные вопросы к каждому разделу
- **Два блокнота Colab** — можно скопировать, скачать `.py` или блокнот (`.ipynb`). Используются только стандартные библиотеки и встроенные данные Colab, на странице приведены реальные результаты запуска.
- Промпты для применения ИИ, глоссарий, сборник аналогий, список литературы
- Советы для преподавателей (планы занятий, частые заблуждения, проверочные вопросы, задания в Colab)

## Файлы

```
index.html                 Главная страница серии (срочный брифинг и четыре миссии) — на корейском
4-1_bream_smelt.html       Лещ vs корюшка
4-2_cat_human.html         Кошка vs человек
4-3_cat_dog.html           Кошка vs собака
4-4_chihuahua_muffin.html  Чихуахуа vs маффин
en/  zh/  ja/  uz/  ru/    Те же пять файлов на английском, китайском, японском, узбекском и русском
```

Каждый HTML-файл содержит изображения, данные и скрипты внутри себя, поэтому сборка не нужна — достаточно открыть файл в браузере (шрифты загружаются из Google Fonts, без интернета будут показаны стандартные шрифты). Ссылки между частями и языками работают при указанной структуре папок, поэтому не переименовывайте файлы и папки.

## Данные и изображения

- Изображения кошки, человека, собаки, чихуахуа и маффина, а также иллюстрацию финальной сцены создал автор.
- Длина и масса рыб: значения для леща и корюшки из набора данных Kaggle Fish Market (пример кода из книги Пак Хэсона «Машинное обучение и глубокое обучение самостоятельно (혼자 공부하는 머신러닝+딥러닝)», лицензия MIT). Машинное обучение на данных о рыбах подробно разобрано в [Простое машинное обучение на Fish Market Data](https://adminmrobo.github.io/Fish_Market_Data_Machine_Learning/) (на корейском).
- Код Colab использует встроенный в scikit-learn набор рукописных цифр (load_digits) и встроенные фотографии scikit-image.
- Некоторые рисунки и значения — иллюстративные модели. В подвале каждой части, в пункте «Что здесь иллюстративная модель», указано, что является реальным расчётом, а что — примером.

## Лицензия

Работа опубликована по [лицензии Creative Commons «Атрибуция — Некоммерческое использование» 4.0 Международная (CC BY-NC 4.0)](https://creativecommons.org/licenses/by-nc/4.0/deed.ru).
Её можно свободно распространять и изменять только в некоммерческих целях, **указание источника обязательно**.

Пример указания источника: Сансун Ан, «Как ИИ различает изображения? · 4-1 Лещ vs корюшка», AI Model Review.

[↑ Наверх](#top)
