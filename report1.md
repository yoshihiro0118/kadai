# 課題1レポート

標準画像を「police.png」を現画像とする。

`ORG=imread('police.png'); % 原画像の入力`  
`imagesc(ORG); axis image; % 画像の表示`

によって、現画像を読み込み、表示した結果を図1に示す。

![現画像](image/police.png)

図1　現画像


現画像を1/2サンプリングするには、画像を1/2倍に縮小し、2倍に拡大する。拡大する際には，単純補間するために「box」オプションを設定する。

`IMG = imresize(ORG,0.5); % 画像の縮小`  
`IMG2 = imresize(IMG,2,'box'); % 画像の拡大`

図2　1/2サンプリング
