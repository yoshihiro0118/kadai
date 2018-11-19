
# 課題1　レポート
##### 標本化間隔と空間解像度

標準画像「cat.jpg」とする。   
`ORG=imread('cat.jpg'); % 原画像の入力`  
`imagesc(ORG); axis image; % 画像の表示`

![現画像](https://github.com/yoshihiro0118/kadai/blob/master/image/cat.jpg)　　

図1原画像

原画像を1/2サンプリングするには，画像を1/2倍に縮小した後，2倍に拡大すればよい．なお，拡大する際には，単純補間するために「box」オプションを設定する．

`IMG = imresize(ORG,0.5); % 画像の縮小`  
`IMG2 = imresize(IMG,2,'box'); % 画像の拡大`

1/2サンプリングの結果を図２に示す．

![1/2](https://github.com/yoshihiro0118/kadai/blob/master/image/cat1-1.jpg)

図2 1/2サンプリング  
同様に原画像を1/4サンプリングするには，画像を1/2倍に縮小した後，4倍に拡大すればよい．すなわち，

`IMG = imresize(ORG,0.5); % 画像の縮小`  
`IMG2 = imresize(IMG,4,'box'); % 画像の拡大`

とする．1/4サンプリングの結果を図３に示す．


![1/4](https://github.com/yoshihiro0118/kadai/blob/master/image/cat1-2.jpg)

図3 1/4サンプリング  

1/8サンプリングは，

`IMG = imresize(ORG,0.5); % 画像の縮小`  
`IMG2 = imresize(IMG,8,'box'); % 画像の拡大`

1/8サンプリングの結果を図３に示す．


![1/8](https://github.com/yoshihiro0118/kadai/blob/master/image/cat1-3.jpg)

図4 1/8サンプリング

1/16サンプリングは、

`IMG = imresize(ORG,0.5); % 画像の縮小`  
`IMG2 = imresize(IMG,16,'box'); % 画像の拡大`

1/16サンプリングの結果を図３に示す．

![1/16](https://github.com/yoshihiro0118/kadai/blob/master/image/cat1-4.jpg)

図5 1/16サンプリング

1/32サンプリングは、

`IMG = imresize(ORG,0.5); % 画像の縮小`  
`IMG2 = imresize(IMG,32,'box'); % 画像の拡大`

1/32サンプリングの結果を図３に示す．

![1/32]https://github.com/yoshihiro0118/kadai/blob/master/image/cat1-5.jpg)

図6 1/32サンプリング
