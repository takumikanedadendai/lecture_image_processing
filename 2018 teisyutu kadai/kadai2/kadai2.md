標準画像「kadai2.jpg」を元画像とする。この画像は縦4000画素、横6000画素のディジタルカラー画像である。

ORG=imread('kadai2.jpg'); % 原画像の入力
ORG = rgb2gray(ORG); colormap(gray); colorbar;モノクロ画像の表示

によって原画像を読み込み、表示した結果を図１に示す。

![原画像](https://github.com/takumikanedadendai/lecture_image_processing/blob/master/2018%20teisyutu%20kadai/kadai%20sozai/kadai2/kadai2-1.png)


図１　原画像

次に
IMG = ORG>128;
imagesc(IMG); colormap(gray); colorbar;  axis image;

を入力し２階調画像を作成し図２に示す。

![原画像](https://github.com/takumikanedadendai/lecture_image_processing/blob/master/2018%20teisyutu%20kadai/kadai%20sozai/kadai2/kadai2-2.png)

図２　２階調画像

次に

IMG0 = ORG>64;
IMG1 = ORG>128;
IMG2 = ORG>192;
IMG = IMG0 + IMG1 + IMG2;
imagesc(IMG); colormap(gray); colorbar;  axis image;

を入力し４階調画像を作成し図３に示す。

![原画像](https://github.com/takumikanedadendai/lecture_image_processing/blob/master/2018%20teisyutu%20kadai/kadai%20sozai/kadai2/kadai2-3.png)


図３　４階調画像


図２、図３から分かる様に階調が上がると画像がなめらかになる
