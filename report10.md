# 課題10　レポート
### 画像のエッジ抽出

原画像の読み込み、白黒濃淡化、白黒濃淡画像の表示は

`ORG = imread('Lenna.jpg'); % 画像の読み込み`  
`ORG = rgb2gray(ORG); % 白黒濃淡画像に変換`  
`imagesc(ORG); colormap(gray); colorbar; % 画像の表示`

![原画像](https://github.com/yoshihiro0118/kadai/blob/master/image10/cat10-1.jpg)

図1 原画像のグレースケール

プレウィット法によるエッジの抽出、またその画像の表示は  
`IMG = edge(ORG,'prewitt'); % エッジ抽出（プレウィット法`  
`imagesc(IMG); colormap('gray'); colorbar;% 画像表示`

![プレウィット法](https://github.com/yoshihiro0118/kadai/blob/master/image10/cat10-2.jpg)

図2 プレウィット法によるエッジ抽出

ソベル法によるエッジの抽出、またその画像の表示は  
`IMG = edge(ORG,'sobel'); % エッジ抽出（ソベル法）`  
`imagesc(IMG); colormap('gray'); colorbar;% 画像表示`

![ソベル法](https://github.com/yoshihiro0118/kadai/blob/master/image10/cat10-3.jpg)

図3 ソベル法によるエッジ抽出

キャニー法によるエッジの抽出、またその画像の表示は  
`IMG = edge(ORG,'canny'); % エッジ抽出（キャニー法）`  
`imagesc(IMG); colormap('gray'); colorbar;% 画像表示`  

![キャニー法](https://github.com/yoshihiro0118/kadai/blob/master/image10/cat10-4.jpg)

図4 キャニー法によるエッジ抽出
