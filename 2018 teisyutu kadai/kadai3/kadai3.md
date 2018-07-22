標準画像「kadai3.jpg」を原画像とする．この画像は縦4000画像，横6000画素による正方形のディジタルカラー画像である。
ORG=imread('kadai3.jpg'); % 原画像の入力
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換
imagesc(ORG); colormap(gray); colorbar; % 画像の表示

によって，原画像を読み込み，表示した結果を図１に示す。

![原画像](https://github.com/takumikanedadendai/lecture_image_processing/blob/master/2018%20teisyutu%20kadai/kadai%20sozai/kadai3/kadai3-1.png)

￼図1  原画像 白黒濃淡画像


IMG = ORG > 64; % 
によって輝度値が64以上の画素を1，その他を0に変換した画像を作成、図２に示す。

![原画像](https://github.com/takumikanedadendai/lecture_image_processing/blob/master/2018%20teisyutu%20kadai/kadai%20sozai/kadai3/kadai3-2.png)

図２　輝度値が64以上の画素を1，その他を0に変換した画像


次に
IMG = ORG > 96;
によって輝度値が96以上の画素を1，その他を0に変換した画像を作成、図3に示す。

![原画像](https://github.com/takumikanedadendai/lecture_image_processing/blob/master/2018%20teisyutu%20kadai/kadai%20sozai/kadai3/kadai3-3.png)

図3　輝度値が96以上の画素を1，その他を0に変換した画像


次に
IMG = ORG > 128;
によって輝度値が128以上の画素を1，その他を0に変換した画像を作成、図4に示す。

![原画像](https://github.com/takumikanedadendai/lecture_image_processing/blob/master/2018%20teisyutu%20kadai/kadai%20sozai/kadai3/kadai3-4.png)

図4　輝度値が128以上の画素を1，その他を0に変換した画像


次に
IMG = ORG > 192;
によって輝度値が192以上の画素を1，その他を0に変換した画像を作成、図5に示す。

![原画像](https://github.com/takumikanedadendai/lecture_image_processing/blob/master/2018%20teisyutu%20kadai/kadai%20sozai/kadai3/kadai3-5.png)

図5　輝度値が192以上の画素を1，その他を0に変換した画像


対象の輝度値が増えるとそれだけ変化する場所が増えるので
より画像が暗くなることがわかった。
