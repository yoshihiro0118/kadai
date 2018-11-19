# 課題3 レポート
### 閾値処理

標準画像を「」とする。
原画像の読み込み,原画像の白黒濃淡画像化、表示は
`ORG=imread('Lenna.png'); % 原画像の入力`  
`ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換`  
`imagesc(ORG); colormap(gray); colorbar; % 画像の表示`

![原画像](https://github.com/yoshihiro0118/kadai/blob/master/image03/cat3-1.jpg)

図1 原画像　グレースケール


輝度値が64以上の画素を1、その他を0に変換し表示する。  
`IMG = ORG > 64; % 輝度値が64以上の画素を1，その他を0に変換`  
`imagesc(IMG); colormap(gray); colorbar;`  

その時の画像を以下に示す。

![輝度値64](https://github.com/yoshihiro0118/kadai/blob/master/image03/cat3-2.jpg)

図3 輝度値が64の時

輝度値が96以上の画素を1、その他を0に変換表示する。  
`IMG = ORG > 96; % 輝度値が64以上の画素を1，その他を0に変換`  
`imagesc(IMG); colormap(gray); colorbar;`  

その時の画像を以下に示す。

![輝度値96](https://github.com/yoshihiro0118/kadai/blob/master/image03/cat3-3.jpg)

図4 輝度値が96の時

輝度値が128以上の画素を1、その他を0に変換表示する。  
`IMG = ORG > 128; % 輝度値が64以上の画素を1，その他を0に変換`  
`imagesc(IMG); colormap(gray); colorbar;`  

その時の画像を以下に示す。

![輝度値128](https://github.com/yoshihiro0118/kadai/blob/master/image03/cat3-4.jpg)

図5 輝度値が128の時

輝度値が192以上の画素を1、その他を0に変換表示する。  
`IMG = ORG > 192; % 輝度値が64以上の画素を1，その他を0に変換`  
`imagesc(IMG); colormap(gray); colorbar;`  

その時の画像を以下に示す。

![輝度値192](https://github.com/yoshihiro0118/kadai/blob/master/image03/cat3-5.jpg)

図6 輝度値が192の時
