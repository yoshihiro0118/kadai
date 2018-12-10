# 課題8 レポート
### ラベリング

原画像の読み込み、白黒濃淡化、白黒濃淡画像の表示は

`ORG = imread('Lenna.jpg'); % 画像の読み込み`  
`ORG = rgb2gray(ORG); % 白黒濃淡画像に変換`  
`imagesc(ORG); colormap(gray); colorbar; % 画像の表示`

![原画像](https://github.com/yoshihiro0118/kadai/blob/master/image08/cat8-1.jpg)

図1 原画像のグレースケール

画像の閾値を128にして2値化し、表示するためには  
`IMG = ORG > 128; % 閾値128で二値化`  
`imagesc(IMG); colormap(gray); colorbar; % 画像の表示`  

![128](https://github.com/yoshihiro0118/kadai/blob/master/image08/cat8-2.jpg)

図2　閾値を128にした時の画像

また図2の画像をラベリング、表示するためには
`IMG = bwlabeln(IMG);`  
`imagesc(IMG); colormap(jet); colorbar; % 画像の表示`  

![ラベリング](https://github.com/yoshihiro0118/kadai/blob/master/image08/cat8-3.jpg)


図3　ラベリングした画像
