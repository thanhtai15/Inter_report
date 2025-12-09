---
title: "Blog 2"
date: 2024-09-09
weight: 1
chapter: false
pre: " <b> 3.2. </b> "
---

# Kết hợp Insight của Snyk với Hỗ trợ từ Amazon Q Developer để Hợp lý hóa Phát triển An toàn

**Bởi Omar Faruk and David Schott | ngày 28 tháng 4 năm 2025 | trong Amazon Q Developer, Developer Tools, Partner solutions, Security**

Ngày nay, các nhà phát triển đối mặt với một hành động cân bằng liên tục  xây dựng các tính năng và chức năng mới đồng thời đảm bảo tính bảo mật và độ tin cậy của cơ sở mã của họ. Hai công cụ mạnh mẽ, Snyk và Amazon Q Developer, có thể hoạt động song song để giúp các nhà phát triển vượt qua thách thức này với hiệu quả và tính năng suất cao hơn.

Snyk là một nền tảng bảo mật hàng đầu dành cho nhà phát triển, trao quyền cho các nhà phát triển bảo mật liền mạch mã, các phần phụ thuộc mã nguồn mở, ảnh container, và cơ sở hạ tầng đám mây của họ, tất cả từ một nền tảng thống nhất duy nhất. Amazon Q Developer là một trợ lý được hỗ trợ bởi AI tạo sinh, được thiết kế để tăng tốc nhiều tác vụ khác nhau trong vòng đời phát triển phần mềm. Bằng cách kết hợp các insight bảo mật từ Snyk với các khả năng hỗ trợ của Amazon Q Developer, các nhà phát triển có thể hợp lý hóa quy trình làm việc của họ và tập trung vào việc bàn giao sản phẩm.

---

## Bắt đầu với Amazon Q Developer và Snyk IDE Plugins

Để bắt đầu với Amazon Q Developer, bạn cần có AWS Builder ID hoặc là một phần của tổ chức có phiên bản AWS IAM Identity Center cho phép bạn sử dụng Amazon Q. Để sử dụng các tác nhân Amazon Q Developer cho phát triển phần mềm trong Visual Studio Code, hãy bắt đầu bằng cách cài đặt tiện ích mở rộng Amazon Q. Tìm phiên bản mới nhất của tiện ích mở rộng trên trang Amazon Q Developer. Tiện ích mở rộng này cũng có sẵn cho các IDE JetBrains, Eclipse (Bản xem trước), và Visual Studio. Để có danh sách chi tiết các IDE được hỗ trợ và các tính năng có sẵn trong mỗi IDE, hãy tham khảo tài liệu Amazon Q Developer.

Để bắt đầu với Snyk, hãy đăng ký tài khoản Snyk miễn phí hoặc đăng nhập bằng tài khoản hiện có của bạn. Để sử dụng Snyk trong IDE của bạn nhằm tự động tìm các vấn đề bảo mật, hãy xem xét tài liệu IDE và cài đặt Snyk bằng cách sử dụng marketplace tiện ích mở rộng IDE của bạn. Sau khi Snyk được cài đặt, hãy điều hướng đến bảng điều khiển Snyk trong IDE của bạn và làm theo hướng dẫn trên màn hình để xác thực với tài khoản Snyk của bạn.

Sau khi xác thực, Snyk sẽ tự động quét toàn bộ cơ sở mã của bạn để tìm các vấn đề bảo mật. Snyk sẽ tiếp tục quét định kỳ khi bạn viết mã hoặc tạo mã bằng Amazon Q Developer.

---

## Hướng dẫn

Hãy cùng khám phá cách Snyk và Amazon Q Developer có thể được sử dụng cùng nhau thông qua một vài ví dụ. Hãy tưởng tượng rằng bạn đang duy trì một dự án mã nguồn mở. Là người dùng Snyk mới, bạn muốn tìm và khắc phục các vấn đề bảo mật trong dự án. Trong kịch bản đầu tiên và đơn giản này, Snyk đã xác định nhiều trường hợp lỗ hổng bảo mật trong các dòng mã cụ thể. Trong số các lỗ hổng, chúng ta sẽ tập trung vào lỗ hổng Phơi bày Thông tin.

![Snyk IDE Plugin](/images/3-Blog/Blog2-1.png)

**Hình 1**  Snyk IDE Plugin hiển thị phân tích lỗ hổng của vấn đề Phơi bày Thông tin, cho thấy mức độ nghiêm trọng, mã bị ảnh hưởng và các mẹo phòng ngừa.

Thay vì tự nghiên cứu và tự thực hiện bản sửa lỗi, bạn chỉ cần đánh dấu dòng mã bị gắn cờ, gọi trò chuyện nội tuyến của Amazon Q Developer bằng cách nhấn +I (Mac) hoặc Ctrl+I (Windows), và yêu cầu hỗ trợ. Amazon Q Developer sẽ phân tích vấn đề, đề xuất các thay đổi mã cần thiết và cung cấp cho bạn một bản diff nội tuyến để xem xét và chấp nhận. Điều này cho phép khắc phục nhanh chóng các lỗi bảo mật, tiết kiệm thời gian đồng thời cải thiện mã.

![Amazon Q Developer Inline Fix](/images/3-Blog/Blog2-2.png)

**Hình 2**  Kích hoạt tính năng tạo mã nội tuyến của Amazon Q Developer để khắc phục lỗ hổng phơi bày thông tin đã được phát hiện.

Chúng tôi hài lòng với thay đổi mà Amazon Q Developer đã đề xuất, vì vậy chúng tôi chỉ cần nhấn enter để chấp nhận các gợi ý. Tất nhiên, chúng tôi luôn có thể nhấn escape để từ chối gợi ý nếu cần.

![Code Generation Process](/images/3-Blog/Blog2-3.png)

**Hình 3**  Amazon Q Developer hiển thị quá trình tạo mã nội tuyến để khắc phục lỗ hổng phơi bày thông tin đã được phát hiện.

---

## Sử dụng Tác nhân /dev

Ngoài trò chuyện nội tuyến, bạn có thể chuyển chi tiết lỗ hổng trực tiếp từ chế độ xem Vấn đề (Problems view) của plugin Snyk vào khả năng tác nhân /dev của Amazon Q Developer.

Trong giao diện trò chuyện của Q Developer, khả năng tác nhân /dev cho phép trò chuyện dài hơn, ngữ cảnh không gian làm việc rộng hơn và xử lý các thay đổi trong nhiều tệp và chủ đề. Khi quy trình làm việc này được gọi, Tác nhân Amazon Q Developer sẽ tạo mã dựa trên mô tả và mã hiện có trong không gian làm việc, cung cấp danh sách các gợi ý để xem xét và thêm vào không gian làm việc, và nếu cần, lặp lại việc tạo mã dựa trên phản hồi.

![Dev Agent Project-wide Fixes](/images/3-Blog/Blog2-4.png)

**Hình 4**  Sử dụng tác nhân /dev của Amazon Q để thực hiện các bản sửa lỗi trên toàn dự án đối với các lỗ hổng do Snyk phát hiện trên nhiều tệp.

---

## Xử lý Các Vấn đề Phức tạp

Không phải tất cả các vấn đề đều đơn giản như ví dụ trước. Trong một trường hợp phức tạp hơn, Snyk có thể làm lộ ra một lỗ hổng đòi hỏi sự hiểu biết sâu sắc hơn về mã và rủi ro tiềm ẩn. Hãy xem xét một vấn đề khác mà Snyk đã xác định trong dự án chúng ta đang thảo luận.

![Snyk XSS Vulnerability](/images/3-Blog/Blog2-5.png)

**Hình 5**  Snyk Plugin làm nổi bật lỗ hổng cross-site scripting (XSS), cho thấy dòng mã bị ảnh hưởng và các đề xuất phòng ngừa.

Ở đây, bạn có thể chuyển sang giao diện trò chuyện của Amazon Q Developer, cung cấp chi tiết về vấn đề và yêu cầu giải thích kỹ lưỡng hơn. Amazon Q Developer sau đó có thể đi sâu vào cơ sở mã, giải thích chi tiết về vấn đề và hướng dẫn bạn cách khắc phục phù hợp. Phương pháp hợp tác này trao quyền cho các nhà phát triển đưa ra các quyết định sáng suốt và có được kiến thức rộng hơn, thay vì chỉ đơn giản là thực hiện một gợi ý.

![Amazon Q Developer Chat Interface](/images/3-Blog/Blog2-6.png)

**Hình 6**  Giao diện trò chuyện của Amazon Q Developer giải thích lỗ hổng XSS và các hàm ý bảo mật của nó thông qua đối thoại ngôn ngữ tự nhiên.

Lưu ý rằng Amazon Q Developer cung cấp các liên kết đến tài liệu và các nguồn khác để đọc thêm. Ngoài ra, bạn có thể tiếp tục thảo luận về vấn đề để tìm hiểu thêm. Ví dụ, hãy tưởng tượng rằng bạn muốn hiểu về các vụ vi phạm trong thế giới thực đã xảy ra do các vấn đề mà Snyk đã xác định. Q cung cấp một vài ví dụ để tôi tìm hiểu thêm.

![Real-world XSS Examples](/images/3-Blog/Blog2-7.png)

**Hình 7**  Amazon Q Developer thảo luận về các ví dụ đáng chú ý về vi phạm XSS trong thế giới thực và tác động bảo mật của chúng.

Ngoài việc khắc phục các vấn đề, Amazon Q Developer cũng có thể hỗ trợ các tác vụ phát triển khác do Snyk xác định, chẳng hạn như cập nhật các phần phụ thuộc, tái cấu trúc mã, hoặc tối ưu hóa cơ sở hạ tầng đám mây. Bằng cách tích hợp hai công cụ này, các nhà phát triển có thể hợp lý hóa việc quét bảo mật, điều tra vấn đề và khắc phục, qua đó tăng đáng kể năng suất tổng thể của họ.

---

## Kết luận

Trong bài blog này, chúng tôi đã xem xét cách Snyk và Amazon Q Developer là một bộ đôi mạnh mẽ trong bộ công cụ của nhà phát triển hiện đại. Việc tích hợp các insight bảo mật hàng đầu của Snyk với các khả năng AI tạo sinh của Amazon Q Developer trao quyền cho các nhà phát triển xác định, hiểu và giải quyết các lỗ hổng bảo mật hiệu quả hơn. Sự kết hợp này cho phép các nhà phát triển nâng cao kỹ năng và cải thiện khả năng của mình khi họ giải quyết các vấn đề bảo mật. Hãy bắt đầu bằng cách cài đặt Amazon Q Developer trong IDE và plugin Snyk.

---

## Snyk  Tiêu điểm Đối tác AWS

Snyk trao quyền cho các nhà phát triển trên thế giới xây dựng các ứng dụng an toàn và trang bị cho các đội bảo mật để đáp ứng các yêu cầu của thế giới kỹ thuật số. Được sử dụng bởi 1.200 khách hàng trên toàn thế giới, Nền tảng Bảo mật Nhà phát triển của Snyk tự động tích hợp với quy trình làm việc của nhà phát triển và được xây dựng có mục đích để các đội bảo mật cộng tác với các đội phát triển của họ.

---

## Về các tác giả:

**Omar Faruk**

Omar Faruk là Kiến trúc sư Giải pháp Đối tác DevOps tại Amazon Web Services. Ông giúp các đối tác DevSecOps thiết kế, xây dựng và vận hành khối lượng công việc của họ và của khách hàng chung trong AWS. Ông đam mê CI/CD, Cơ sở hạ tầng dưới dạng Mã (Infrastructure as Code), và trải nghiệm nhà phát triển thế hệ tiếp theo. Ngoài công việc, ông thích dành thời gian cho gia đình và du lịch.

**David Schott**

David là Kỹ sư Giải pháp DevSecOps dày dạn kinh nghiệm với hơn 15 năm kinh nghiệm giúp các công ty Fortune 100 tối ưu hóa bảo mật và hiệu quả phân phối phần mềm của họ. Sau khi thúc đẩy việc áp dụng DevOps và phát triển CI tại CloudBees, hiện ông tập trung vào DevSecOps tại Snyk, nơi ông cộng tác với các đối tác chiến lược để cho phép đổi mới an toàn trên quy mô lớn.
