# 課題9　レポート
### メディアンフィルタと先鋭化

原画像の読み込み、白黒濃淡化、白黒濃淡画像の表示は

`ORG = imread('Lenna.jpg'); % 画像の読み込み`  
`ORG = rgb2gray(ORG); % 白黒濃淡画像に変換`  
`imagesc(ORG); colormap(gray); colorbar; % 画像の表示`

![原画像](https://github.com/yoshihiro0118/kadai/blob/master/image09/cat9-1.jpg)

図1 原画像のグレースケール

また、図1の画像にノイズを付け、画像を表示するには

`ORG = imnoise(ORG,'salt & pepper',0.02); % ノイズ添付`  
`imagesc(ORG); colormap(gray); colorbar; % 画像の表示`  

![ノイズ添付](https://github.com/yoshihiro0118/kadai/blob/master/image09/cat9-2.jpg)

図2 図1にノイズを添付したもの

次に、平滑化フィルタで雑音を除去し、画像を表示するには  
`IMG = filter2(fspecial('average',3),ORG); % 平滑化フィルタで雑音除去`  
`imagesc(IMG); colormap(gray); colorbar; % 画像の表示`

![平滑化フィルタ](https://github.com/yoshihiro0118/kadai/blob/master/image09/cat9-3.jpg)

図3 平滑化フィルタによる雑音除去

メディアンフィルタで雑音を除去し、画像を表示するには  
`IMG = medfilt2(ORG,[3 3]); % メディアンフィルタで雑音除去`  
`imagesc(IMG); colormap(gray); colorbar; % 画像の表示`

![メディアんフィルタ](https://github.com/yoshihiro0118/kadai/blob/master/image09/cat9-4.jpg)

図4 メディアンフィルタによつ雑音除去

自分でフィルタを設計し、適応し、その画像の表示は  
`f=[0,-1,0;-1,5,-1;0,-1,0]; % フィルタの設計`  
`IMG = filter2(f,IMG,'same'); % フィルタの適用`  
`imagesc(IMG); colormap(gray); colorbar; % 画像の表示`

![フィルタ設計](https://github.com/yoshihiro0118/kadai/blob/master/image09/cat9-5.jpg)

図5　設計したフィルタによる雑音除去
