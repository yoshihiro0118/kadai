# 課題4 レポート
### 画像のヒストグラムの表示

原画像の読み込み、白黒濃淡化、白黒濃淡画像の表示は

`ORG=imread('Lenna.png'); % 原画像の入力`  
`ORG=rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換`  
`imagesc(ORG); colormap(gray); colorbar;`

![原画像](https://github.com/yoshihiro0118/kadai/blob/master/image04/cat4-1.jpg)

図1 原画像　グレースケール


画像のヒストグラムの表示は

`imhist(ORG); % ヒストグラムの表示`

![ヒストグラム](https://github.com/yoshihiro0118/kadai/blob/master/image04/cat4-2.jpg)

図2 画像のヒストグラム
