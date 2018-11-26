# 課題6 レポート
### 画像の二値化

原画像の読み込み、白黒濃淡化、白黒濃淡画像の表示は

`ORG=imread('Lenna.png'); % 原画像の入力`  
`ORG=rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換`  
`imagesc(ORG); colormap(gray); colorbar;`  

![原画像](https://github.com/yoshihiro0118/kadai/blob/master/image06/cat6-1.jpg)

図1 原画像のグレースケール

128による二値化は
`IMG = ORG>128; % 128による二値化`
`imagesc(IMG); colormap(gray); colorbar; % 画像の表示`

![128](https://github.com/yoshihiro0118/kadai/blob/master/image06/cat6-2.jpg)

図2 128による二値化

ディザ法による二値化は
`IMG = dither(ORG); % ディザ法による二値化`
`imagesc(IMG); colormap(gray); colorbar; % 画像の表示`

![ディザ法](https://github.com/yoshihiro0118/kadai/blob/master/image06/cat6-3.jpg)

図3 ディザ法による二値化
