# レポート7
### ダイナミックレンジの拡大

原画像の読み込み、白黒濃淡化、白黒濃淡画像の表示は

`ORG = imread('Lenna.jpg'); % 画像の読み込み`  
`ORG = rgb2gray(ORG); % 白黒濃淡画像に変換`  
`imagesc(ORG); colormap(gray); colorbar; % 画像の表示`

![グレースケール](https://github.com/yoshihiro0118/kadai/blob/master/image07/cat7-1.jpg)  

図1　原画像のグレースケール

その画像の濃度ヒストグラフを表示するためには  
`imhist(ORG); % 濃度ヒストグラムを生成、表示`

![濃度ヒストグラフ](https://github.com/yoshihiro0118/kadai/blob/master/image07/cat7-2.jpg)  

図2 濃度ヒストグラフ

次に、図1の画像のダイナミックレンジを0から255にした時の画像の表示には　　
`ORG = double(ORG);`  
`mn = min(ORG(:)); % 濃度値の最小値を算出`  
`mx = max(ORG(:)); % 濃度値の最大値を算出`  
`ORG = (ORG-mn)/(mx-mn)*255;`  
`imagesc(ORG); colormap(gray); colorbar; % 画像の表示`  

![0～255](https://github.com/yoshihiro0118/kadai/blob/master/image07/cat7-3.jpg)

図3 ダイナミックレンジを拡大した時の画像

図3の画像のヒストグラフも表示には

![濃度ヒストグラフ](https://github.com/yoshihiro0118/kadai/blob/master/image07/cat7-4.jpg)  

図4 濃度ヒストグラフ

図4ではヒストグラフ上に成分がないところがある。
これは`ORG = uint8(ORG);`   
であらかじめdouble型で画像が生成されていたためint型にしたことにより小数点以下の部分が切り捨てられてしまったことにより、成分がない部分があると考えられる。
