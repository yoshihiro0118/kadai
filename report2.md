# 課題2 レポート
## 階調数と擬似輪郭

2階調、4階調、8階調のグラフを生成する。

標準画像を「」とする。
原画像の読み込み、表示は  
`ORG=imread('Lenna.png'); % 原画像の入力`  
`ORG = rgb2gray(ORG); colormap(gray); colorbar;`  
`imagesc(ORG); axis image; % 画像の表示`

図1 原画像

2階調画像の生成、表示は  
`IMG = ORG>128;`  
`imagesc(IMG); colormap(gray); colorbar;  axis image;`  

図2 2階調画像

4階調画像の生成、表示は  
`IMG0 = ORG>64;`  
`IMG1 = ORG>128;`  
`IMG2 = ORG>192;`  
`IMG = IMG0 + IMG1 + IMG2;`
`imagesc(IMG); colormap(gray); colorbar;  axis image;`

図3 4階調画像

8階調画像の生成は  
`IMG0 = ORG>32;`  
`IMG1 = ORG>64;`  
`IMG2 = ORG>96;`  
`IMG3 = ORG>128;`  
`IMG4 = ORG>160;`  
`IMG5 = ORG>192;`  
`IMG6 = ORG>224;`  
`IMG = IMG0 + IMG1 + IMG2 + IMG3 + IMG4 + IMG5 + IMG6;`  
`imagesc(IMG); colormap(gray); colorbar;  axis image;`  
図4 8階調画像
