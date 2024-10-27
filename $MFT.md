# マスターファイルテーブル(Master File Table・MFT)とは
　Windowsで使用されるNTFSフォーマットのハードディスクにはMFT(マスターファイルテーブル)というデータが先頭部分に存在する。  
　ハードディスクをNTFS形式でフォーマットすると、先頭にはブートセクタが書き込まれ、その次の領域にMFT用の領域が作られる。通常、MFT用の領域としてハードディスク容量の数%の領域が確保される。  
　NTFS以前に使用されていたFAT32形式だと、ファイル名や属性情報はディレクトリエントリに、データが書き込まれている部分の情報はFAT(ファイルアロケーションテーブル)に分割して情報が格納される。
![image](https://github.com/user-attachments/assets/34664eb7-3808-4429-8ac3-319ffda0cc24)

 参考資料：  
 [マスターファイルテーブル(Master File Table・MFT)とは](https://www.rescue-center.jp/elementary/vol10.html)  
 [そんな餌で俺様が釣られクマーーー](https://sites.google.com/view/kumaa/software/mft-ntfs-explorer)
