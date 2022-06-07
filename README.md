# 資安期中

# 一、安裝辛酸史

## 網路上找的方法

> 參考網址
> 

> [https://ithelp.ithome.com.tw/articles/10206165](https://ithelp.ithome.com.tw/articles/10206165)
> 

### 第一步

先確認電腦上有安裝JRE。

### 第二步

到官方github上下載最新版WebGoat（網址：[https://github.com/WebGoat/WebGoat/releases](https://github.com/WebGoat/WebGoat/releases) ）

### 第三步

如果你安裝的JRE是第8版，則使用下面的指令來啟動WebGoat，其中Port跟Server網址都可以在這邊作設定，如果不特別設定，Port預設就是8080，而Server網址則是localhost。

![image](https://user-images.githubusercontent.com/105283235/172363454-3d24e878-250e-473f-9188-ee55c421307b.png)

如果你安裝的JRE是第9或以上的版本，根據網路上苦主經驗，直接使用上述指令會出現錯誤，但也不用擔心，只要在執行的時候使用下面的語法就可以了：

![image](https://user-images.githubusercontent.com/105283235/172363599-4b0acc7b-b902-4604-be6f-f08b6ed93b6f.png)

上面兩項指令中的VERSION部分是依看你下載的版本來改字串，例如你如果下載的是目前最新的版本v8.0.0.M21，那你的指令就要寫成：

![image](https://user-images.githubusercontent.com/105283235/172363656-6233f242-a82d-45ac-8131-fcda29ea738e.png)

我的電腦安裝的是JRE 8，而輸入指令後就會看到畫面如下，告訴你網頁伺服器已經跑起來了！

![image](https://user-images.githubusercontent.com/105283235/172363782-efb0f5a5-8570-4c48-816c-1d74ff99130e.png)

### 第四步

使用瀏覽器，輸入剛剛你所設定的Port及Server網址，如果沒有特別設定的話網址就會長這樣：[http://localhost:8080/WebGoat](http://localhost:8080/WebGoat)
 ，接著就可以看到WebGoat的畫面出現啦！

![image](https://user-images.githubusercontent.com/105283235/172363840-ab30edf0-14be-4da7-b938-366826a2d193.png)

由於WebGoat是專門讓人來練習漏洞的，所以裡面包含的都是漏洞百出的網頁，因此官方也建議在使用WebGoat練習時，最好是把網路中斷，以免有心人士利用，讓使用者反而變成受害者。

另外，WebGoat只供教育使用，在這邊學到的任何技術都不能拿去隨便測試外面的網頁，以免觸法，就算被抓時跟執法單位說你只是在研究也是沒用的，因為每個駭客被抓的時候一開始也都是這樣說的。

## 我的操作

首先，我真的很難過我的webgoat一直執行不了QQ

![image](https://user-images.githubusercontent.com/105283235/172364461-98f404a9-00d5-49b8-93ad-3ed463bcbbc7.png)

正在嘗試重新下載jdk以及jre

![image](https://user-images.githubusercontent.com/105283235/172364410-99a07c13-f9f6-4dba-bee9-dcd4946232c3.png)

並且在嘗試變更環境變數

![image](https://user-images.githubusercontent.com/105283235/172364533-377c9e2b-3900-4b01-a693-30985dd32ac4.png)

![image](https://user-images.githubusercontent.com/105283235/172364601-496b916b-16f7-4464-b584-c87ed9ef34e2.png)

參考網址：[https://www.kjnotes.com/devtools/35](https://www.kjnotes.com/devtools/35)

![image](https://user-images.githubusercontent.com/105283235/172364641-02c82dad-6bf0-4a1b-9b48-525e03a51d67.png)

![image](https://user-images.githubusercontent.com/105283235/172364682-b2597812-f0a3-49ed-83ec-78f8c29555ac.png)

經過多次嘗試還是無法安裝WebGoat QQ

希望能找到解決方法將它安裝好><

# 二、WebGoat安裝心得

在做期中報告時花了很多時間在安裝WebGoat上，花了好幾天還是沒有完成安裝，也有參考同學的方式用Windows Powershell安裝，但卻不知為何找不到同學所使用右鍵開啟的方式。而期中報告最讓我煩惱的是其實我對於本學期的課程仍不太了解，範例的演練也不太理解，只能努力跟上老師的腳步，上課及錄影對於我來說可能需要再花更多時間去吸收，在未來課程的路上，會更努力去看資料及了解，希望能夠更好的吸收上課內容><

# 三、課堂範例

## 原因

通過課程簡介後最令我感興趣的是第22章**Account Auditing**，因為這是與我身活比較息息相關的，我們常常在不知不覺中輸入了好多帳號密碼、電話號碼等等，也有許多被盜用的情形在身邊發生，若能將資安相關的概念利用在這我相信會很有成就感！

## **Account Auditing**

在找尋相關資料時發現一個參考網站：[https://blog.twnic.tw/2021/05/06/18063/](https://blog.twnic.tw/2021/05/06/18063/)

其中有說到：

> 目前大量個資儲存在網路上，因此其落入網路罪犯手中的情況日益普遍，大規模資料洩漏事件的發生頻率正在上升。
> 

> 企業和政府組織的網路經常遭駭並因此造成用戶個資外洩，駭客透過買賣這些資料，以冒充他人或進行詐騙。
> 

以下是您可用於確認個資是否外洩並保護自己的步驟。

### 檢查自己的個資是否外洩

可利用此網站：[HaveIBeenPwned.com](https://haveibeenpwned.com/)

只要輸入電子郵件地址便能確認其是否曾遭偽造或破壞。此網站還提供密碼搜尋，使用者可依此查詢密碼是否曾經落入駭客之手。

### 資料外洩的處理方式

依據機密程度

- 重要身分識別證號被盜

> 必須立即通報主管機關
> 
- 非敏感資訊外洩

> 例如電子郵件地址及用戶名稱，若您的電子郵件地址被盜，則應更改密碼，並設置[多重身分驗證（multi-factor authentication，MFA）](https://www.nist.gov/blogs/cybersecurity-insights/back-basics-whats-multi-factor-authentication-and-why-should-i-care)
> 

### 發現自己密碼外洩怎麼辦？！

應立即更改所有相關帳戶的密碼，設置多重身分驗證也不失為最佳做法。

最後，您應對帳戶中任何可疑活動保持警惕，必要時，請更改密碼並通知帳號管理員。

## 我的嘗試

> **無**外洩會呈現**綠色**
> 

> **有**外洩會呈現**紅色**
> 

![image](https://user-images.githubusercontent.com/105283235/172364774-b7bd5e16-ceb4-4f9f-86bf-d581776b5249.png)

好來，我的mail完但了...

![image](https://user-images.githubusercontent.com/105283235/172364818-242882ce-b222-47ae-b0d5-3aefba6b7a5d.png)

值得慶幸的是我的密碼沒事~

![image](https://user-images.githubusercontent.com/105283235/172364888-41f88602-4f79-4fe4-b3cb-dcc7c2798024.png)

我的電話號碼看起來應該是安全的~但有點疑慮是我常常會收到陌生簡訊，確定真的沒有外洩嗎？！

# 四、程式碼

## 獲取帳戶的所有違規行為

> API 最常見的用途是返回特定帳戶所涉及的所有違規行為的列表。API 採用單個參數，即要搜索的帳戶。該帳戶不區分大小寫，並且將刪除前導或尾隨空格。該帳戶應始終進行 URL 編碼。
> 

按 URL 中的版本：

![image](https://user-images.githubusercontent.com/105283235/172366381-f51cf276-ec12-4ce2-a48c-2d59cfaeed9a.png)

通過 api-version 標頭：

![image](https://user-images.githubusercontent.com/105283235/172366437-1782cb11-c2cd-4b95-b8d0-941bea231e50.png)

通過內容協商：

![image](https://user-images.githubusercontent.com/105283235/172366497-3fbcb370-edef-47f8-843b-72d4800f75ba.png)

## ****獲取系統中所有被破壞的站點****

> “違規”是系統已被攻擊者破壞並洩露數據的實例。例如，Adobe 是一個漏洞，Gawker 是一個漏洞等。可以返回系統中每個漏洞的詳細信息，目前有**595 個漏洞**。
> 

按 URL 中的版本（可[單擊此處](https://haveibeenpwned.com/api/v2/breaches)進行測試）：

![image](https://user-images.githubusercontent.com/105283235/172366550-f51d6c8b-9b80-4291-8a35-8b46fbc53781.png)

通過 api-version 標頭：

![image](https://user-images.githubusercontent.com/105283235/172366591-be5391de-f4fc-457c-ba23-fbbae173f814.png)

通過內容協商：

![image](https://user-images.githubusercontent.com/105283235/172366632-61a49edf-3dde-4481-8d38-96a9e2348b32.png)

## ****獲取單個違規站點****

> 有時只需要一次違規，這可以通過違規“名稱”檢索。這是穩定值，可能與違規“標題”相同也可能不同（可能會更改）。有關更多信息，請參閱下面[的違規模型](https://haveibeenpwned.com/API/v2#BreachModel)。
> 

按 URL 中的版本（可[單擊此處](https://haveibeenpwned.com/api/v2/dataclasses)進行測試）：

![image](https://user-images.githubusercontent.com/105283235/172366675-f1034d7c-d71b-4c4d-a6a1-618fa0471947.png)

通過 api-version 標頭：

![image](https://user-images.githubusercontent.com/105283235/172366732-c6203b8c-d708-462b-88a8-58cd2ee64197.png)

通過內容協商：

![image](https://user-images.githubusercontent.com/105283235/172366765-0ca20aec-b8f3-4148-9074-da74fc0dd63e.png)

# 五、心得

上課時許多程式相關的內容真的聽不太懂，加上課本及課本內網站打開的當下一片英文真的是很頭痛QQ只好請益Google翻譯大人。

其實還是有許多內容是不了解的，但有在努力補充腦內的知識，或許還有非常多不了解的地方，但希望能一點一點慢慢進步，其實在做報告的時候一邊很怕自己電腦會不會被駭之類的哈哈哈哈，因為有許多網站真的是看不懂就點進去，然後又會突然跳出一些奇奇怪怪的東西，希望在學習資安的路上，也可以讓自己更可以避免這種狀況，以及若真的遇到時能夠如何應對。
