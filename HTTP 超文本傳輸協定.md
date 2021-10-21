## HTTP

- [Hypertext Transfer Protocol (HTTP)](https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol)
- [超文本傳輸協定](https://zh.wikipedia.org/wiki/%E8%B6%85%E6%96%87%E6%9C%AC%E4%BC%A0%E8%BE%93%E5%8D%8F%E8%AE%AE)
  - HTTP是一種用於分佈式、協作式和超媒體訊息系統的`應用層`協定

![http](http.png)

### [HTTP版本]

## [HTTP/0.9] 
- 已過時。只接受GET一種請求方法，沒有在通訊中指定版本號，且不支援請求頭。由於該版本不支援POST方法，因此客戶端無法向伺服器傳遞太多訊息。

## [HTTP/1.0] 
- 這是第一個在通訊中指定版本號的HTTP協定版本。

## [HTTP/1.1]
- 預設採用持續連接（Connection: keep-alive），能很好地配合代理伺服器工作。還支援以管道方式在同時傳送多個請求，以便降低線路負載，提高傳輸速度。

HTTP/1.1相較於HTTP/1.0協定的區別主要體現在：
 -快取處理
 -頻寬最佳化及網路連接的使用
 -錯誤通知的管理
 -訊息在網路中的傳送
 -網際網路位址的維護
 -安全性及完整性
 
 ## [HTTP/2]
 - 目前版本，於2015年5月作為網際網路標準正式發布。
 

### [HTTP 狀態碼]


## [狀態代碼的第一個數字代表當前回應的類型]： 
- 1xx訊息——請求已被伺服器接收，繼續處理
- 2xx成功——請求已成功被伺服器接收、理解、並接受
- 3xx重新導向——需要後續操作才能完成這一請求
- 4xx請求錯誤——請求含有詞法錯誤或者無法被執行
- 5xx伺服器錯誤——伺服器在處理某個正確請求時發生錯誤
- 雖然 RFC 2616 中已經推薦了描述狀態的短語，例如"200 OK"，"404 Not Found"，但是WEB開發者仍然能夠自行決定採用何種短語，用以顯示在地化的狀態描述或者自訂訊息。

### [HTTP請求]
![http](HTTP_Request.png)
- CRLF refers to the special character elements "Carriage Return" and "Line Feed."
- These elements are embedded in HTTP headers and other software code to signify an End of Line (EOL) marker.
- Many internet protocols, including MIME (e-mail), NNTP (newsgroups) and, more importantly, HTTP, use CRLF sequences to split text streams into discrete elements.
- Web application developers split HTTP and other headers based on where CRLF is located.
- CRLF injection attack ==> Exploits occur when an attacker is able to inject a CRLF sequence into an HTTP stream.
### [請求方法]
|方法 | 說明 |
| -------|  -------|
|GET|向指定的資源發出「顯示」請求。使用GET方法應該只用在讀取資料，而不應當被用於產生「副作用」的操作中，例如在網路應用程式中。|
|HEAD|與GET方法一樣，都是向伺服器發出指定資源的請求。只不過伺服器將不傳回資源的本文部份。
|POST|向指定資源提交資料，請求伺服器進行處理（例如提交表單或者上傳檔案）。資料被包含在請求本文中。這個請求可能會建立新的資源或修改現有資源，或二者皆有。|
|PUT|向指定資源位置上傳其最新內容。|
|DELETE|請求伺服器刪除Request-URI所標識的資源。|
|TRACE|回顯伺服器收到的請求，主要用於測試或診斷。|
|OPTIONS|這個方法可使伺服器傳回該資源所支援的所有HTTP請求方法。用'*'來代替資源名稱，向Web伺服器傳送OPTIONS請求，可以測試伺服器功能是否正常運作。|
|CONNECT|HTTP/1.1協定中預留給能夠將連接改為隧道方式的代理伺服器。通常用於SSL加密伺服器的連結（經由非加密的HTTP代理伺服器）。|

### [http響應]
![http](HTTP_Response.png)
