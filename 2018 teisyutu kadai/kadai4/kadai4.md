標準画像「kadai4.jpg」を原画像とする．この画像は縦4000画像，横6000画素による正方形のディジタルカラー画像である。

ORG=imread('kadai4.jpg'); % 原画像の入力
ORG=rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換
imagesc(ORG); colormap(gray); colorbar;

によって，原画像を読み込み，表示した結果を図１に示す。

![原画像](https://github.com/takumikanedadendai/lecture_image_processing/blob/master/2018%20teisyutu%20kadai/kadai%20sozai/kadai4/kadai4-2.png)

図1   原画像　白黒濃淡画像

imhist(ORG);
によって読み取った画像のヒストグラムを作成、図２に示す。

![原画像](https://github.com/takumikanedadendai/lecture_image_processing/blob/master/2018%20teisyutu%20kadai/kadai%20sozai/kadai4/kadai4-1.png)

図2   ヒストグラム

写真に写るキャラクター部分が山なりになっていることがわかる。
