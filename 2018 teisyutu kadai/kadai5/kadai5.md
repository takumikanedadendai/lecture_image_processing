標準画像「kadai5.jpg」を原画像とする．この画像は縦4000画像，横6000画素による正方形のディジタルカラー画像である。

ORG=imread('Lenna.png'); % 原画像の入力
ORG = rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換
imagesc(ORG); colormap(gray); colorbar;

によって，原画像を読み込み，表示した結果を図１に示す。

![原画像](https://github.com/takumikanedadendai/lecture_image_processing/blob/master/2018%20teisyutu%20kadai/kadai%20sozai/kadai5/kadai5-1.png)

図1   原画像 白黒濃淡画像

H = imhist(ORG); 
によってヒストグラムのデータを列ベクトルEに格納。

myu_T = mean(H);
max_val = 0;
max_thres = 1;
for i=1:255
C1 = H(1:i); 
によってヒストグラムを2つのクラスに分ける。

n1 = sum(C1); 
n2 = sum(C2);
によって画素数の算出。

myu1 = mean(C1); 
myu2 = mean(C2);
によって平均値の算出。

sigma1 = var(C1); 
sigma2 = var(C2);
によって分散の算出。

sigma_w = (n1 *sigma1+n2*sigma2)/(n1+n2); 
によってクラス内分散の算出。

sigma_B = (n1 *(myu1-myu_T)^2+n2*(myu2-myu_T)^2)/(n1+n2); 
によってクラス間分散の算出。

各計算結果を図２に示す。

![原画像](https://github.com/takumikanedadendai/lecture_image_processing/blob/master/2018%20teisyutu%20kadai/kadai%20sozai/kadai5/kadai5-4.png)

図２　　各計算結果
