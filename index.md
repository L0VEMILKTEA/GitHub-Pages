
```
以新手的角度記錄第一次使用GitHub建立靜態網頁的情況
並使用 No-IP 動態域名指向及除錯過程
```

## 0. 註冊GitHub及No-IP帳號
----

架設個人靜態網頁並綁定網域會使用到 [GitHub][1] 及 [No-IP][2] 的功能，

已經妥備帳號可以省略這個步驟，申請帳號沒有太多複雜的手續，亦有不少能派上用場的時候。

在我查資料嘗試綁定時看到大部分的文獻都是使用 DNS 綁定 GitHub Pages，

在我的認知中 DNS 有個動態域名的技術，我覺得可以直接使用 DDNS，

一方面我沒有個別申請或購買過一個網域域名，先前在 No-IP 申請過免費的 DDNS 做為網域，

便直接沿用，也成功指向，就決定把這個經過寫成教學記錄。

[1]: https://github.com/
[2]: https://www.noip.com/

## 1. 在GitHub建立個人專案
----

登入 GitHub 後點選右上角的**頭像**，接著點 `Your repositories` 建立新的專案，

![image](https://raw.githubusercontent.com/L0VEMILKTEA/GitHub-Pages/653823aeca7b42ccc99614efe61a941e978627b7/1%E5%BB%BA%E7%AB%8B%E5%B0%88%E6%A1%88.jpeg "建立專案")

替你的專案**命名**，可以加上**簡述**，再按下面的 `Create repository` 即可。

![image](https://raw.githubusercontent.com/L0VEMILKTEA/GitHub-Pages/653823aeca7b42ccc99614efe61a941e978627b7/2%E5%89%B5%E5%BB%BA%E5%84%B2%E5%AD%98%E5%BA%AB.jpeg "命名簡述專案")

GitHub 有提供一些網頁範本用，先點選上排 `Setting` 後左下有 `Pages` ，就能點 `Chooes a theme` 選個喜歡的範本囉！

![image](https://raw.githubusercontent.com/L0VEMILKTEA/GitHub-Pages/653823aeca7b42ccc99614efe61a941e978627b7/3%E4%BD%BF%E7%94%A8%E7%AF%84%E6%9C%AC.jpeg "建立成功")

我自己比較習慣用深色背景，對觀看者來說負擔比較小，選定後點右上角 `Select theme` 就好囉。

![image](https://raw.githubusercontent.com/L0VEMILKTEA/GitHub-Pages/653823aeca7b42ccc99614efe61a941e978627b7/4%E6%8C%91%E9%81%B8%E7%AF%84%E6%9C%AC.jpeg "挑選範本")

建立完成上面會有一段**網址**，就是使用 GitHub 網域產生的個人網頁，

網址應該是 `https://你的 GitHub 帳號.github.io/你的專案名稱/`，

GitHub 給的網址已經有**憑證**了，這時候可以選擇要不要綁定**個人網域**，或著單純放作品到 GitHub 上。

![image](https://raw.githubusercontent.com/L0VEMILKTEA/GitHub-Pages/653823aeca7b42ccc99614efe61a941e978627b7/5%E5%80%8B%E4%BA%BA%E7%B6%B2%E5%9D%80.jpeg "網頁產生")


## 2. 在No-IP建立個人網域
----

登入 No-IP 後點 `My Account` 進入後台，

![image](https://raw.githubusercontent.com/L0VEMILKTEA/GitHub-Pages/653823aeca7b42ccc99614efe61a941e978627b7/6%E9%BB%9E%E9%81%B8%E5%84%80%E8%A1%A8%E6%9D%BF.jpeg "進入後台")

點選 `More Records` 創建 **DDNS** ，

![image](https://raw.githubusercontent.com/L0VEMILKTEA/GitHub-Pages/653823aeca7b42ccc99614efe61a941e978627b7/7%E5%BB%BA%E7%AB%8B%E5%9F%9F%E5%90%8D2.jpeg "建立DDNS")

我在一開始用指向 IP 建立 `A` ，遇到 GitHub 要求指向名稱 `CNAME` ，

 `A` 是 `Address` 指向 IP 位址， `CNAME` 是 `Canonical Name` 指向真實名稱，運作方式不一樣。

![image](https://raw.githubusercontent.com/L0VEMILKTEA/GitHub-Pages/653823aeca7b42ccc99614efe61a941e978627b7/8%E5%BB%BA%E7%AB%8BA.jpeg "綁定失敗")

所以我們類型點下面的`CNAME` ，右邊的 **Target** 綁定自己的 GitHub 網域，

然後選想要的 **Domain** 並取個好名 **Hostname** 點右下角 `Create Hostname` 就成功建立指向，

![image](https://raw.githubusercontent.com/L0VEMILKTEA/GitHub-Pages/653823aeca7b42ccc99614efe61a941e978627b7/8%E5%BB%BA%E7%AB%8BCNAME.jpeg "建立CNAME")

回到 GitHub 把 No-IP 的網域綁定，它會花一些時間驗證，之後上面就會有綁定成功的網址，

點開來會發現 GitHub 的憑證沒了，把 `Enforce HTTPS` 勾起來，一段時間後會幫你弄憑證，

![image](https://raw.githubusercontent.com/L0VEMILKTEA/GitHub-Pages/653823aeca7b42ccc99614efe61a941e978627b7/9%E5%BC%B7%E5%88%B6HTTPS.jpeg "綁定成功")

到這邊就算完成了，之後可以再寫一些網頁的東西放上來。




