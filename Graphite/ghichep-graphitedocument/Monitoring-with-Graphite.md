#Mục lục
 -	[1. Graphite là gì?]
	- [1.1 Thế nào là time series data]
	- [1.2. Time-Series Databases]
		- [1.2.1 Khả năng lưu trữ]
		- [1.2.2 Quá trình ưu tiên]
	- [1.3. Lịch sử của Graphite là gì]
	- [1.4. Điều gì khiến Graphite là độc nhất]
		- [1.4.1 Cấu trúc Metric đơn giản] 
		- [1.4.2 Graphing API]
		- [1.4.3 Quá trình thử nghiệm nhanh chóng]
		- [1.4.4 Thư viện số phong phú]
		- [1.4.5 Các chuỗi Function]
	- [1.5. Những ai sử dụng Graphite trong thực tế?]
		- [1.5.1 Booking.com]
		- [1.5.2 GitHub]
		- [1.5.3 Etsy]
		- [1.5.4 Electronic Arts]
	- [1.6 Tại sao tôi nên sử dụng Graphite?]
 -	[2. Một số quy ước trong Monitoring]
	- [2.1 Ba điều quan trọng trong Monitoring ]
		- [2.1.1 Tìm lỗi]
		- [2.1.2 Cảnh báo]
		- [2.1.3 Khả năng lên kế hoạch]
	- [2.2 Cân nhắc về Poll/Pull Model]
		- [2.2.1 Pull Mode]
		- [2.2.2 Punsh Mode]
	- [2.3 Nơi nào Graphite Fit vào ảnh ]
	- [2.4 Các hệ thống cảnh báo thường có]
		- [2.4.1 Telemetry]
		- [2.4.2 Metrics Router]
		- [2.4.3 Aggregation]
		- [2.4.4 State Engine]
		- [2.4.5 Notification Routers]
		- [2.4.6 Storage Engine]
		- [2.4.7 Visualization]
	- [2.5 Kết luận]
 -	[3. Các thành phần Graphite : Các phần chuyển động]
	- [3.1 Carbon]
		- [3.1.1 Carbon-cache]
		- [3.1.2 Carbon-relay]
		- [3.1.3 Carbon-aggregator]
		- [3.1.4 Quán trình lọc Metric]
		- [3.1.5 Các số liệu bên trong]
		- [3.1.6 Các vấn đề về bảo mật mạng]
	- [3.2 Whisper]
		- [3.2.1 Các file Whisper nhận được tạo như thế nào]
		- [3.2.2 Các chính sách xoay vòng và lưu trữ]
		- [3.2.3 Tính toán dung lượng file Whisper]
		- [3.2.4 Phân tích cấu trúc một file Whisper]
		- [3.2.5 Lưu trữ nào kiểm soát các query]
		- [3.2.6 Các phương thức kết hợp]
		- [3.2.7 xFileFactor]
		- [3.2.8 Lên kế hoạch các Namespace]
		- [3.2.9 Các vấn đề hiệu năng]
	- [3.3 Graphite-Web]
		- [3.3.1 Django Framework]
		- [3.3.2 Webserver]
		- [3.3.3 Database]
		- [3.3.4 Memcached]
		- [3.3.5 Events]
		- [3.3.6 Storage Backends]
	- [3.4 Đẩy tất cả vào cùng nhau]
		- [3.4.1 Basic Setup]
		- [3.4.2 Vertical Scaling]
		- [3.4.4 Horizontal Scaling]
		- [3.4.5 Multi-Site Replication]
 -	[4. Xây dựng Graphite Server]
	- [4.1 Installation]
		- [4.1.1 Có những container hoặc image nào có thể dùng được luôn]
		- [4.1.2 Graphite lưu trữ các file ở đâu?]
		- [4.1.3 Các package có sẵn với từng distro]
		- [4.1.4 Các phương thức cài đặt nào có sẵn]
		- [4.1.5 Tại sao nên dùng Virtualenv]
		- [4.1.6 Sử dụng sudo một cách có hiệu quả]
		- [4.1.7 Các phụ thuộc]
		- [4.1.8 Cài đặt từ source]
	- [4.2 Chuẩn bị Web Database]
	- [4.3 Cấu hình Carbon]
		- [4.3.1 Carbon.conf]
		- [4.3.2 Storage-schemas.conf]
		- [4.3.3 Storage-aggregation.conf]
		- [4.3.4 Một vài chuẩn bị cuối cùng]
		- [4.3.5 Khởi tiến trình Carbon]
	- [4.4 Cấu hình Graphite-Web]
		- [4.4.1 Local_settings.py]
		- [4.4.2 Cấu hình Apache]
	- [4.5 Kiểm tra lại cài đặt Graphite]
		- [4.5.1 Các số liệu Carbon]
		- [4.5.2 Đưa data mới tới Carbon]
		- [4.5.3 Build graph đầu tiên]
	- [5. Giao diện người dùng Graphite]
		- [5.1 Finding Metrics]
			- [5.1.1 Metric Tree]
			- [5.1.2 Sử dụng tính năng tìm kiếm]
			- [5.1.3 Tính năng Auto-Completer]
			- [5.1.4 Wildcard]
		- [5.2 Cửa sổ Graphite Composer]
		- [5.3 Các biểu đồ sửa đổi]
		- [5.4 Toolbar]
			- [5.4.1 Chọn các data gần đây]
			- [5.4.2 Refesh Graph]
			- [5.4.3 Chạn phạm vi ngày ]
			- [5.4.4 Export Short URL]
			- [5.4.5 Quá trình tải Graph từ URL]
			- [5.4.6 Lưu Graph]
			- [5.4.7 Xóa Graph]
		- [5.5 Menu lựa chọn Graph]
			- [5.5.1 Thêm Graph Title]
			- [5.5.2 Chèn Graph Legend]
			- [5.5.3 Toggle Axes và Grid]
			- [5.5.4 Line Chart Mode]
			- [5.5.5 Area và Stacked Graph]
			- [5.5.6 Chỉnh sửa Y-Axis]
		- [5.6 Graph data dialog]
			- [5.6.1 Mục tiêu cuối cùng]
			- [5.6.2 Xây dựng Carbon Performance graph]
	- [6. Advanced Graph ]
	- [7. Dashboard]
	- [8. Whisper Storage]
	- [9. Troubleshooting Graphite Performance]
	- [10. Mở rộng Graphite]
	- [11. Render API]
	
#Nội dung của sách 
 -	Chương 1 và 2 : Cung cấp giới thiệu cơ bản về giám sát, các khái niệm về xu hướng và một số thuật ngữ.
 -	Chương 3 : Thảo luận các cách tiếp cận khác nhau tới cách thu thập Telemetry data. 
 -	Chương 4 và 5 : Giới thiệu các nội dung để tạo Graphite và các tính năng cũng như chức năng của nó.
 -	Chương 6 và 7 tập hợp các workflow điển hình cho người dùng để tạo các line và chart. Người dùng có thể tạo các chart phức tạp với các chuỗi funtion, mutiple
	axes và tương tác với redering API một cách trực tiếp.
 -	Chương 8 giới thiệu dashboard có sẵn của Graphite và một số dashboard thuộc phần mềm thứ 3 bên ngoài. Bạn cũng có thể sử dụng render API để tạo client-side 
 chart rendering với javascript framework như D3.js
 -	Chương 9 đến 12 giúp Người quản trị hệ thống làm chủ, mở rộng và sửa lỗi với hiệu năng cao hoặc cao hơn là có thể tọa Graphite-cluster

#I. Graphite là gì?

Cuốn sách đề cập tới việc giám sát với Graphite. Một trong những mục tiêu trong việc dạy các người dùng để sử dụng Graphite một cách hiệu quả là không chỉ làm sao
để việc giám sát tốt hơn, mà là làm sao để có thể lưu trữ và nhận data theo một cách mà giúp chúng ta có thể quản lý được nguy hiểm, dự đoán được các khả năng
thâm hụt, và phân tích được các khả năng thâm hụt, và phân tích chiến lược IT với các nhu cầu kinh doanh của tổ chức. Giám stas với Graphite đào tạo chúng ta để 
có thể trả lời những câu hỏi giá trị hơn là : "server của tôi có đang sống không?". Chúng ta nên biết chắc chắn một cách nhanh chóng rằng : "các khách hàng của chúng
ta đang có những trải nghiệm tồi tệ", "chúng ta có đủ khả năng để thu thút một Reddit font-end posting hay không?"

Hầu như mọi thứ chúng ta làm có thể được tính toán và phân tích. Các nhà dự báo thời tiết sử dụng dữ liệu tăng tiến để dự đoán sự thay đổi về thời tiết, áp suốt, 
và tốc độ gó. Các thống kê phân tích xu hướng thể thao bởi các người chơi và các đội dể tìm ra vận động viên có năng lực nhất và chiến thuật huấn luyện hiệu quả
nhất. Các nhà thiết kế phần mềm và các nhà quản trịhej thống sử dụng telemetry - các phương thức tính toán và ghi lại, để tính toán sự hiệu quả của hệ thống và 
các triển khai.

**Telemetry là gì?**

`Telemetry` đề cập đến sự thu thập của các phương thức tính toán, thông thường là các công cụ từ xa, với mục đích giám sát.

##1.1 Time-series data là gì?
Chúng ta tương tác với `Time Series` data hầu như mỗi ngày, thậm chú chúng ta còn không nhận ra chúng ngay lập tức như là Các báo cáo thời tiết, các thống kê 
tài chính...

Nhưng thực sự time-series data là gì? Đó là sự liên tục của các giá trị thu thập được một cách thường xuyên, có các khoảng thời gian cách đều nhau một cách thống 
nhất. Một ví dụ là bạn đi ra ngoài mỗi giờ, và đưa ra đánh giá về nhiệt độ gần đây theo đơn vị F, hành động đưa các số liệu này vào máy tính (hoặc thậm chí là 
tờ phiếu hoặc giấy) sẽ được coi là một dạng thu thập Time-serires data.

Các nhà quản trị hệ thống và các nhà thiết kế web thông thường quan tâm tới ` tốc độ thay đổi ` và ` thời vụ `, cốt để đánh giá tình trạng hoặc chất lượng dịch vụ 
của một ứng dụng hoặc máy chủ nhất định. Họ muốn biết xem liệu các service của họ có bị sụt giảm hay có thể có xu hướng rơi vào trạng thái tồi tệ.

Việc phân tích, mặt khác, thông thường tìm kiếm các xu hướng theo hành vi người dùng. Họ thường tập trung vào ` sự phân tán ` của một tập hợp các dữ liệu hoặc 
 `metadata`. Các sự kiện độc nhất mang ý nghĩa đặc biệt cho chúng, vì vậy khả năng để tạo sự tương quan giữa các sự kiện mà sử dụng các tag (hoặc các nhãn) cho 
 phép các phân tích để phân loại người dùng và các hành vi của họ theo cách mà các câu hỏi thích hợp có thể được yêu cầu của dữ liệu dường như ngẫu nhiên. Nhưng 
 kể từ khi bạn đọc quyển sách này, tôi giả sử rằng công việc gần đây của bạn liên quan nhiều hơn đến các dạng câu hỏi được trả lời với Time-Series data và các
  công cụ như Graphite.
  
##1.2 Time-Series Databases
Time-series database là một hệ thống phần mềm dùng cho việc lưu trữ và thu thập time-series data. Hiệu năng và sự bền vững của một TSDB (Time Series Database) 
thường là một nhân tố chính khi đánh giá các các hệ thống xu hướng phần mềm như Graphite.

##1.2.1 Khả năng lưu trữ 
Khi người dùng phổ thông muốn tương tác trực tiếp với dữ liệu đang hoạt động một cách bình thường của họ, thì nên tương tác với một Database đã được đánh giá 
về khối lượng công việc của một hệ thống lưu trữ và tiếp nhận dữ liệu hiệu năng cao. Vì vậy, việc chúng ta có những hiểu biết tối thiểu về các dạng hiệu năng 
của TSDB là rất quan trọng.
Trong vài năm trở lại đây, có một sự bùng nổ về số lượng của các dự án Open Source và các sản phẩm giám sát thương mại. Sự tiên tiến trong Solid-State Drive 
(SSD) storage và sự bền vững của Moore's Law đã làm cho nó về mặt kỹ thuật và thương mại khả thi để thu thập, lưu trữ, tiếp nhận, tạo tương quan và hiển thị 
một số lượng lớn dữ liệu giám sát thời gian thực với các hệ thống hàng hóa. Các hệ thống database phân tán (đặc biệt là NoSQL) được tạo bởi sự cạnh tranh trong 
sự theo đuổi các phân tích Big Data, đã khiến chúng dễ dàng hơn trước kia rất nhiều để mở rộng theo theo chiều ngang và thêm khả năng như theo yêu cầu cần có.

Tại sao tôi lại nhấn mạnh vào việc lưu trữ. Bởi vì, nếu không có khả năng lưu trữ nhanh chóng (và nhiều), thì chúng ta không có khả năng đẩy các data tới disk 
cho các thu hồi về sau. Dĩ nhiên, nó giúp ta hiểu khi tôi đề cập đến "fast storage". Thẳng thắn mà nói, nó không phải là vấn đề khó khi write dữ liệu vào disk 
một cách nhanh chóng, hoặc là đọc nó từ disk nhanh chóng. Thử thách ở đây chính là việc lam cả 2 thứ đó cùng một lúc.

##1.2.2 Các hoạt động ưu tiên
Trong các điều khoản của việc thiết kế Hệ điều hành, `kernel` là bộ não của việc điều hành. Nó được giao nhiệm vụ với một số lượng lớn và đa dạng các nhiệm vụ 
quản trị, từ việc quản lý bộ nhớ tới các nhiệm vụ ưu tiên tới việc phân luồng dữ liệu thông qua mạng và các giao diện lưu trữ. Dựa vào các điều kiện kèm theo 
và các cài đặt được áp dụng, `kernel` phải sắp xếp hợp lý để kiếm soát được khối lượng công việc sao cho hiệu quả nhất có thể. Nhưng câu hỏi là việc đó áp dụng 
với chúng ta như thế nào?

Việc ghi và đọc từ đĩa (được biết như là `input` và `output`, hay đơn giản là `I/O`) là những hoạt động quá sức nếu bạn cố gắng làm nhiều việc một lúc.

Một kỹ thuật thông thường trong việc tối ưu hóa quá trình `write` đó là đệm chúng vào bộ nhớ. Điều này vẫn ổn nếu như bộ nhớ của bạn vẫn đủ sức chưa, nhưng bạn 
cần đẩy chúng vào disk một cách thường xuyên hoặc bạn phải đối mặt với nguy cơ mất hết dữ liệu khi hệ thống có sự cố.

Mặt khác, nó rất hiệu quả khi sử dụng lưu trữ tạm thời trong bộ nhớ để giữ các "hot copy" của data cho các truy vấn (read). Một lần nữa, nó là một cách tiếp cận 
hiệu quả miễn là bạn có đủ bộ nhớ và bạn gia hạn các câu trả lời được lưu trữ tạm thời một cách thường xuyên, đủ để đảm bảo các kết quả chính xác cho người dùng.

Graphite sử dụng cả hai kỹ thuật này để hỗ trợ việc thực hiện các thành phần time-series database : 
 -	Carbon : một network service có nhiệm vụ lắng nghe các trình báo về metric đầu vào