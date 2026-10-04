# mua proxy us: phân biệt gói theo IP và theo GB, chọn đúng cho nuôi tài khoản, scraping hay kiểm tra quảng cáo

Người gõ "mua proxy us" lên Google thường rơi vào một trong hai tình huống: cần một IP Mỹ cho một việc rất cụ thể, hoặc đã từng mua một lần, bị chặn, và giờ đang tìm chỗ khác. Cả hai nhóm gặp chung một vấn đề: bảng giá giữa các nhà cung cấp chênh nhau không nhiều, nhưng loại proxy thì khác hẳn nhau.

Mua sai loại thường không lộ ra ngay. Bạn vẫn kết nối được, check ipinfo vẫn thấy United States, nhưng tài khoản lập vài ngày đã bị checkpoint, hoặc request liên tục trả về captcha. Đến lúc đó thì tiền đã trả và IP đã nằm trong balance.

Bài này đi theo thứ tự thực tế: bạn cần IP Mỹ để làm gì, hai kiểu gói khác nhau ở đâu, giá hiện tại của từng gói, rồi cách cấu hình để có IP Mỹ trong vài phút.

## Proxy Mỹ dân cư khác proxy thường ở chỗ nào

Các site Mỹ như Facebook, eBay, Etsy, Nike hay hệ thống chống gian lận của ngân hàng Mỹ không chỉ nhìn quốc gia của IP. Chúng nhìn ASN — tức là IP đó thuộc về nhà mạng dân dụng (Comcast, Cox, Verizon) hay thuộc về một dải datacenter (AWS, DigitalOcean, một hosting nào đó). Dải datacenter bị chấm điểm thấp gần như mặc định, bất kể IP nằm ở Mỹ hay không.

Proxy dân cư Mỹ giải quyết đúng điểm đó: IP đến từ thiết bị thật của người dùng tại Mỹ, nên request trông giống lưu lượng gia đình. Đổi lại, IP dân cư không bền như bạn tưởng. Chúng có vòng đời, thường từ vài giờ đến khoảng 24 giờ, rồi tự đổi. Ai cần "IP Mỹ cố định mãi mãi" nên biết trước điều này thay vì phát hiện sau khi mua.

Với mục đích xem nội dung bị chặn theo vùng, cần nói thẳng: proxy dân cư không phải công cụ tối ưu cho việc xem phim hay YouTube. Các nền tảng streaming chặn IP dân cư rất mạnh, và bản thân nhiều nhà cung cấp cũng siết lại chính sách sử dụng cho mục đích này.

## Bạn thuộc nhóm nào trước khi trả tiền

Câu hỏi "mua proxy US ở đâu" ít quan trọng hơn câu hỏi "mua loại nào". Ba nhóm nhu cầu dưới đây dẫn tới ba lựa chọn khác nhau:

| Việc bạn đang làm | Thứ quan trọng nhất | Loại gói phù hợp |
| --- | --- | --- |
| Nuôi nhiều tài khoản US (Facebook, TikTok, eBay, Etsy), mỗi profile một IP | IP ổn định trong phiên, một IP gắn một tài khoản, không giới hạn dung lượng tải | Gói tính theo số IP |
| Scrape dữ liệu, theo dõi giá, kiểm tra quảng cáo, check SERP Mỹ | Xoay IP liên tục, mỗi request tốn rất ít băng thông | Gói tính theo GB |
| Vừa nuôi tài khoản vừa chạy scraper | Cần cả IP cố định lẫn dung lượng xoay | Gói bundle (IP + GB) |

Nếu bạn không chắc mình thuộc nhóm nào, hãy nhìn vào cách bạn dùng proxy: bạn có đăng nhập vào một tài khoản nhiều lần trong ngày không? Nếu có, đó là bài toán IP ổn định. Nếu mỗi lần chạy là một phiên mới, không cần nhớ IP, thì đó là bài toán băng thông.

## 9Proxy có gì cho người cần IP Mỹ

9Proxy là nền tảng proxy dân cư, công bố pool khoảng 20 triệu IP trải trên hơn 90 quốc gia. Con số này được nhiều bài đánh giá độc lập trong năm 2026 nhắc lại, dù các trang quảng cáo đôi khi ghi cao hơn — nên cứ lấy mốc 20 triệu / 90 quốc gia làm tham chiếu.

Điểm đáng quan tâm với người cần IP Mỹ nằm ở phần nhắm mục tiêu. Theo tài liệu kỹ thuật của 9Proxy, bạn có thể lọc theo quốc gia, bang, thành phố, mã ZIP và cả ISP. Đây là mức chi tiết mà phần lớn nhà cung cấp giá rẻ không có: chọn được `country-us` đã là chuyện thường, nhưng chọn tới `city-newyork` hay lọc theo ASN của một nhà mạng cụ thể thì ít nơi làm.

Nền tảng hỗ trợ cả HTTP/HTTPS và SOCKS5, và hoạt động theo mô hình balance — bạn nạp tiền, mua gói, dùng dần, không phải trả phí thuê bao hàng tháng cho phần bạn không dùng.

👉 [Xem các gói proxy Mỹ của 9Proxy](https://bit.ly/9-Proxy)

## Gói theo IP và gói theo GB khác nhau ở đâu

### Gói theo IP: trả tiền cho địa chỉ, không trả cho dung lượng

Bạn mua một số lượng IP nhất định, và mỗi IP được dùng không giới hạn băng thông trong thời gian nó còn sống. IP chưa dùng thì không mất — theo tài liệu của 9Proxy, IP chưa kích hoạt không hết hạn.

Cách này hợp với người nuôi tài khoản và với dân bán lại proxy cho khách. Nhược điểm nằm ở chỗ khác: gói theo IP yêu cầu app desktop (Windows, macOS, Linux), bạn phải forward IP ra port rồi mới dùng được. Nếu bạn muốn cấu hình trong browser, mất thêm vài bước.

### Gói theo GB: trả tiền cho dung lượng, tạo bao nhiêu endpoint cũng được

Đây là model tính theo lưu lượng. Bạn mua 5 GB hay 200 GB, và tạo endpoint không giới hạn số lượng — chỉ dung lượng bị trừ. Gói GB có hiệu lực 180 ngày, riêng gói Enterprise thì không giới hạn thời gian. Toàn bộ thao tác chạy trên dashboard, không cần cài app.

Với scraping và kiểm tra quảng cáo Mỹ, đây thường là lựa chọn hợp lý hơn: mỗi request chỉ tốn vài chục KB, nhưng bạn cần IP mới liên tục.

### Bundle: khi bạn cần cả hai

Bundle gộp IP và GB vào một gói. Kiểu dùng điển hình là vừa giữ vài chục tài khoản Mỹ vừa chạy scraper định kỳ trên cùng một tài khoản 9Proxy.

## Bảng giá toàn bộ gói hiện hành

Một lưu ý về thời điểm: ngày 1/6/2026, 9Proxy điều chỉnh giá lần đầu tiên kể từ khi thành lập. Gói tính theo IP và gói bundle tăng giá; gói tính theo GB giữ nguyên. Bảng dưới đây là mức giá sau điều chỉnh, giá USD, thanh toán một lần và dùng theo balance.

**Gói proxy dân cư theo IP** — băng thông không giới hạn, IP chưa dùng không hết hạn:

| Gói | Số IP | Đơn giá / IP | Tổng | Mua |
| --- | --- | --- | --- | --- |
| 100 IP | 100 | $0,24 | $24 | [ Mua gói 100 IP](https://bit.ly/9-Proxy) |
| 500 IP | 500 | $0,144 | $72 | [ Mua gói 500 IP](https://bit.ly/9-Proxy) |
| 1.000 + 500 IP | 1.500 (tặng thêm 500) | $0,084 | $126 | [ Mua gói 1.500 IP](https://bit.ly/9-Proxy) |
| 2.500 IP | 2.500 | $0,084 | $210 | [ Mua gói 2.500 IP](https://bit.ly/9-Proxy) |
| 5.000 IP | 5.000 | $0,072 | $360 | [ Mua gói 5.000 IP](https://bit.ly/9-Proxy) |
| 15.000 IP | 15.000 | $0,048 | $720 | [ Mua gói 15.000 IP](https://bit.ly/9-Proxy) |
| 25.000 IP | 25.000 | $0,035 | $863 | [ Mua gói 25.000 IP](https://bit.ly/9-Proxy) |
| 50.000 IP | 50.000 | $0,029 | $1.438 | [ Mua gói 50.000 IP](https://bit.ly/9-Proxy) |
| 100.000 IP (Business) | 100.000 | $0,023 | $2.300 | [ Mua gói 100.000 IP](https://bit.ly/9-Proxy) |
| 200.000 IP (Business) | 200.000 | $0,021 | $4.140 | [ Mua gói 200.000 IP](https://bit.ly/9-Proxy) |
| 500.000 IP (Business) | 500.000 | $0,018 | $8.625 | [ Mua gói 500.000 IP](https://bit.ly/9-Proxy) |

**Gói proxy dân cư theo GB** — tạo endpoint không giới hạn, hiệu lực 180 ngày:

| Gói | Dung lượng | Đơn giá / GB | Tổng | Mua |
| --- | --- | --- | --- | --- |
| 5 GB | 5 GB | $3,00 | $15 | [ Mua gói 5 GB](https://bit.ly/9-Proxy) |
| 50 + 5 GB | 55 GB (tặng thêm 5 GB) | $2,10 | $105 | [ Mua gói 55 GB](https://bit.ly/9-Proxy) |
| 100 GB | 100 GB | $1,50 | $150 | [ Mua gói 100 GB](https://bit.ly/9-Proxy) |
| 200 GB | 200 GB | $1,00 | $200 | [ Mua gói 200 GB](https://bit.ly/9-Proxy) |
| 1.000 GB | 1.000 GB | $0,80 | $800 | [ Mua gói 1.000 GB](https://bit.ly/9-Proxy) |
| 2.000 GB | 2.000 GB | $0,75 | $1.500 | [ Mua gói 2.000 GB](https://bit.ly/9-Proxy) |
| 3.000 GB (Enterprise) | 3.000 GB | $0,72 | $2.160 | [ Mua gói 3.000 GB](https://bit.ly/9-Proxy) |
| 6.000 GB (Enterprise) | 6.000 GB | $0,70 | $4.200 | [ Mua gói 6.000 GB](https://bit.ly/9-Proxy) |
| 10.000 GB (Enterprise) | 10.000 GB | $0,68 | $6.800 | [ Mua gói 10.000 GB](https://bit.ly/9-Proxy) |

Gói Enterprise không giới hạn thời gian hiệu lực, có chế độ team (1 owner + tối đa 5 thành viên) chia sẻ dung lượng trong nhóm.

**Gói bundle (IP + GB)**:

| Gói | Cấu hình | Tổng | Mua |
| --- | --- | --- | --- |
| Starter | 100 IP + 5 GB | $30 | [ Mua gói Starter](https://bit.ly/9-Proxy) |
| Popular | 1.500 IP + 50 GB | $180 | [ Mua gói Popular](https://bit.ly/9-Proxy) |
| Pro | 5.000 IP + 500 GB | $720 | [ Mua gói Pro](https://bit.ly/9-Proxy) |

## Cách mua và lấy IP Mỹ trong vài phút

**Bước 1 — Tạo tài khoản và nạp balance.** Bạn nạp trước một khoản, sau đó mua gói bằng balance. Cách này cho phép mua thêm IP lẻ sau này mà không phải giao dịch lại từ đầu.

**Bước 2 — Chọn nhóm gói.** Nếu làm tài khoản Mỹ, đi hướng theo IP. Nếu scrape, đi hướng theo GB.

**Bước 3 — Với gói theo GB: tạo proxy trong Proxy Generator.** Chọn quốc gia `us`, thêm bang hoặc thành phố nếu cần, chọn chế độ sticky hoặc rotating, rồi xuất danh sách endpoint. Thông tin nhắm mục tiêu nằm ngay trong username, theo cấu trúc:


<sub-user>-country-<mã quốc gia>-st-<bang>-city-<thành phố>-isp-<mã ISP>-sst-<phút sticky>-ssid-<id phiên>


Ví dụ một IP Mỹ giữ nguyên 15 phút: `subaccount-country-us-sst-15`. Muốn IP Mỹ ở New York: `subaccount-country-us-city-newyork`. Muốn lọc theo nhà mạng: `subaccount-isp-as22773_Cox_Communications_Inc.`

Một cảnh báo thực tế từ chính tài liệu của 9Proxy: đừng lọc quá sâu. Càng thêm nhiều điều kiện (bang + thành phố + ISP) thì pool IP khả dụng càng hẹp, tốc độ lấy IP càng chậm. Chỉ lọc tới cấp thành phố khi bạn thực sự cần.

**Bước 4 — Với gói theo IP: dùng app desktop.** Mở app, lọc theo Country / State / City / ZIP / ISP, chọn IP Mỹ rồi forward ra port. Với dòng lệnh thì gọn hơn:


9proxy proxy -c US -p 60000


Lệnh này forward một IP dân cư Mỹ về `127.0.0.1:60000`.

**Bước 5 — Kiểm tra trước khi dùng thật.** Đừng bỏ bước này, nhất là khi mua gói lớn:


curl -x socks5://127.0.0.1:60000 https://ipinfo.io/json


Kết quả phải trả về IP nằm ở Mỹ, và ASN phải là nhà mạng dân dụng chứ không phải dải datacenter. Đây là cách nhanh nhất để phát hiện bạn đang đi sai loại proxy.

👉 [Tạo tài khoản và lấy IP Mỹ ngay](https://bit.ly/9-Proxy)

## Sticky hay rotating cho tài khoản Mỹ

Với gói theo GB, bạn chọn chế độ ngay khi tạo endpoint:

- **Rotating**: mỗi request một IP mới. Dùng khi tốc độ quan trọng hơn tính liên tục — cào dữ liệu, theo dõi giá, kiểm tra chớp nhoáng.
- **Sticky**: giữ nguyên IP trong số phút bạn đặt bằng tham số `sst`. Dùng khi cần đăng nhập, duyệt qua nhiều bước, hoặc để hệ thống Mỹ nhìn thấy một phiên liền mạch.

Nếu chạy song song nhiều tài khoản trên cùng một cấu hình, thêm `ssid` khác nhau cho từng instance — cùng tham số nhưng khác `ssid` sẽ cho ra các IP khác nhau. Đây là chi tiết nhỏ nhưng ảnh hưởng trực tiếp tới việc hai tài khoản có vô tình dùng chung IP hay không.

## Những điểm cần biết trước khi trả tiền

- **Gói theo IP cần app desktop.** Nếu bạn muốn mọi thứ chạy trên trình duyệt hoặc trên server không có GUI, gói theo GB gọn hơn.
- **IP dân cư không cố định vĩnh viễn.** Vòng đời vài giờ đến khoảng 24 giờ. Nếu IP chết trong vòng 60 giây đầu, 9Proxy có chính sách thay; danh sách Today List cho phép dùng lại IP đã dùng trong 24 giờ mà không trừ thêm IP, miễn là IP đó hoạt động trở lại.
- **Chính sách hoàn tiền hẹp.** Theo tổng hợp của ProxyLook, phần lớn phản hồi tiêu cực về 9Proxy xoay quanh việc không hoàn được tiền khi dịch vụ không hợp nhu cầu, và không có bản dùng thử miễn phí được công bố rõ ràng. Nghĩa là bạn nên mua gói nhỏ nhất để kiểm tra chất lượng IP Mỹ trên chính mục tiêu của mình trước khi nạp số lớn.
- **Chỉ có proxy dân cư.** Không có datacenter, ISP tĩnh hay proxy di động trong danh mục sản phẩm. Nếu bạn cần IP 4G/5G Mỹ, đây không phải chỗ.
- **Streaming không phải sân chơi của proxy dân cư giá rẻ.** iTWire ghi nhận dịch vụ xử lý tốt các tác vụ scraping và quản lý tài khoản nhưng vấp ở Netflix; ProxyLook cho biết 9Proxy đã tuyên bố ngừng hỗ trợ media streaming trên các gói theo IP theo chính sách sử dụng cập nhật. Nếu mục tiêu chính là xem nội dung Mỹ, hãy xác nhận lại điều khoản hiện hành trước khi mua.
- **Giá đã thay đổi từ 1/6/2026.** Gói theo IP và bundle tăng; gói theo GB giữ nguyên. Nếu bạn thấy bảng giá cũ ở đâu đó với mức $20 cho 100 IP, đó là giá trước điều chỉnh.
- **Về thanh toán:** thư mục ProxyLook ghi nhận 9Proxy hỗ trợ thẻ, Apple Pay, Google Pay, Alipay và crypto qua CoinPayments, kèm ưu đãi cộng thêm 5% IP khi thanh toán bằng crypto. Đây là thông tin từ bên thứ ba, nên kiểm tra lại ở bước thanh toán.

## Vài câu hỏi hay gặp

**Mua bao nhiêu IP Mỹ là đủ?** Nếu mỗi tài khoản dùng một IP riêng, lấy số tài khoản cộng thêm 10–20% dự phòng cho IP chết hoặc bị đánh dấu. Với 10–20 tài khoản, gói 100 IP ở mức $24 là điểm bắt đầu hợp lý.

**Gói 100 IP dùng được bao lâu?** IP chưa kích hoạt không hết hạn, nên bạn dùng tới đâu tiêu tới đó. Không có chuyện balance bốc hơi sau 30 ngày như các gói thuê bao.

**Có dùng được với anti-detect browser không?** Có. ProxyLook ghi nhận tích hợp với ixBrowser và Multilogin; SaaSCounter cũng liệt kê Dolphin Anty. Với gói theo GB, bạn dán host/port/username/password vào profile; với gói theo IP, bạn dùng địa chỉ `127.0.0.1:port` sau khi forward.

**Gói GB hết hạn sau 180 ngày thì sao?** Dung lượng chưa dùng hết hiệu lực sau 180 ngày với gói thường. Gói Enterprise thì không giới hạn thời gian — đây là lý do gói Enterprise đắt hơn tính theo đơn giá GB nhưng lại hợp với người dùng không đều.

**Có cần thẻ quốc tế không?** Có, nếu trả bằng thẻ. Phương án crypto cũng được nhắc tới, kèm ưu đãi cộng IP, nhưng tỷ giá và phí chuyển đổi do bạn tự cân.

## Nên bắt đầu từ gói nào

Ba tình huống và ba gợi ý cụ thể:

- **Mới thử, cần vài IP Mỹ để nuôi 5–10 tài khoản:** gói 100 IP ($24). Đủ để đánh giá chất lượng IP Mỹ trên đúng nền tảng bạn làm việc, với chi phí thấp nhất trong bảng giá theo IP.
- **Scrape dữ liệu Mỹ, không cần nhớ IP:** gói 5 GB ($15) hoặc 50 + 5 GB ($105). Bắt đầu bằng 5 GB để đo mức tiêu thụ thực tế, rồi mới lên gói lớn.
- **Vừa nuôi tài khoản vừa scrape:** bundle Starter ($30 cho 100 IP + 5 GB) là điểm vào rẻ nhất cho mô hình kết hợp.

Với người đang phân vân giữa hai hướng, cách nhanh nhất là mua một gói nhỏ ở hướng bạn nghĩ mình cần, chạy thử trên chính mục tiêu thật trong vài ngày, rồi mới quyết định nạp lớn. Chất lượng IP Mỹ phụ thuộc khá nhiều vào nền tảng bạn nhắm tới, và không bảng giá nào trả lời được câu đó thay bạn.

👉 [Kiểm tra gói proxy Mỹ phù hợp với nhu cầu của bạn](https://bit.ly/9-Proxy)
