# [Day 1] 前言
---
## winform base
以前任職於醫療產業，主要都是以winform為主，server都是實體主機。\
因為是winform的程式，所以基本上只要client主機硬體夠強，除非寫的code太爛(呃....)，\
都能靠著硬體的威能(淫威?)，COVER掉大部份的效能問題。\
尤其是現在效能過剩的時代(看著amd zen2 8c起跳，AMD真香~~~~)，\
但是SERVER就正好相反，主機基本上很難大更新，更舊一點的主機可能還是win server 2003以下，\
如果是multi tier的架構，大概是多架了一層APP SERVER層，\
基本上就是一台APP SERVER 應付N台CLIENT的連線，好一點的是架VM，\
一台不夠就是再開一台起來(如果授權夠話XD)，\
這樣子的情形就很麻煩，因為每個APP要使用的環境可能有點不同，\
EX ORACLE的連線要用舊版的，什麼SDK要用特定版本，用錯版本還會造成APP無法啟動，這都是隱藏性的成本。\
還需要考慮到load balance的問題，常常遇到美其名會進行load balance，\
但是一執行時發現都在同一個app server上面，變成半hardcode在元件上面，\
基本上是沒有任何彈性，部署上也是直接更新EXE檔，所以執行到一半的JOB就是強制被中斷，如果交易中進行強制更新也是有機率造成LOCK，所以一般是找休息時間進行更新。
---
## WEB BASE
轉入.net mvc後，也是需要win server去架設iis server，因為沒實作反向代理進行load balance，所以成一台iis主機打天下，完全需要靠硬體去克服沒load balance的問題點。\
因oracle client的屎尿特性，變成9i跟11g以上的oracle版本的client要同時安裝，常常在搞db連線就讓人整個無名火都上來了。

---
## 轉機
偶然機會上到保哥的CONTAINER課程，整個就是發現新大陸阿，
以前在實體機上面遇到的問題居然可以透過CONTAINTER技術進行克服，
讓部署程式可以簡化到以前無法想像到境界。
