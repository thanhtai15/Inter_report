---
title: "Blog 3"
date: 2024-09-09
weight: 1
chapter: false
pre: " <b> 3.3. </b> "
---

# Giới thiệu trải nghiệm khởi động nhanh cho Amazon Q Developer Pro

**Bởi Matt Laver | ngày 7 tháng 4 năm 2025 | trong Amazon Q, Amazon Q Developer, Launch**

Đối với các nhà phát triển phần mềm, đội ngũ phát triển và Chuyên gia CNTT, Bậc Pro của Amazon Q Developer được khuyến nghị. Bậc pro cung cấp giới hạn cao hơn, quản trị cấp doanh nghiệp, bảng điều khiển phân tích, tùy chỉnh mã và bồi thường IP. Ngoài ra, Bậc Pro của Amazon Q Developer yêu cầu AWS IAM Identity Center. Đối với hầu hết các triển khai sản xuất, một phiên bản tổ chức (organization instance) của IAM Identity Center được khuyến nghị. Một phiên bản tổ chức hỗ trợ các phiên nhận dạng danh tính vốn là yêu cầu để sử dụng bậc Pro trong Bảng điều khiển AWS, ngoài những lợi ích được nêu trong hướng dẫn người dùng IAM Identity Center.

Tuy nhiên, điều gì sẽ xảy ra nếu nhóm của bạn muốn bắt đầu nhanh chóng để dùng thử Bậc Pro của Amazon Q Developer (Amazon Q Developer Pro Tier) trên IDE nhưng có những rào cản đang làm chậm bạn lại, chẳng hạn như:

 Bạn không có kế hoạch áp dụng IAM Identity Center trên toàn bộ tổ chức của mình.

 Bạn có một phiên bản tổ chức của IAM Identity Center, nhưng bạn muốn triển khai Amazon Q Developer Pro cho một nhóm người dùng biệt lập, khác biệt so với người dùng trong phiên bản tổ chức của bạn.

 Bạn không kiểm soát Tổ chức AWS mà bạn đang hoạt động trong đó. Ví dụ, một bên thứ ba kiểm soát tổ chức AWS quản lý các tài khoản AWS của bạn và cần thời gian để được phê duyệt các thay đổi.

Để giải quyết những tình huống này, chúng tôi gần đây đã công bố một trải nghiệm thiết lập mới, được đơn giản hóa với hai bước giúp các nhóm muốn dùng thử các tính năng của Amazon Q Developer Pro trong Môi trường Phát triển Tích hợp (Integrated Development Environment - IDE) của họ dễ dàng hơn.

---

## Tài khoản Quản lý và AWS IAM Identity Center

Trước khi chúng ta đi sâu vào chuyến tham quan thiết lập khởi động nhanh, hãy lùi lại một bước và xem xét khuyến nghị của AWS về việc sử dụng thiết lập đa tài khoản để tổ chức khối lượng công việc của bạn. Bạn có thể thấy các lợi ích trong sách trắng của AWS về việc Tổ chức Môi trường AWS của Bạn Sử dụng Nhiều Tài khoản và phương pháp tiếp cận được khuyến nghị là triển khai điều này bằng AWS Organizations. Tài khoản quản lý là tài khoản AWS bạn sử dụng để tạo tổ chức của mình và tài khoản này nên được giữ tối thiểu và bảo mật, chỉ lưu trữ các công cụ quản trị thiết yếu như thiết lập AWS Organizations và triển khai đăng nhập một lần (single sign on) thông qua IAM Identity Center.

IAM Identity Center là cốt lõi cho thiết lập Amazon Q Developer Pro. Người dùng IAM Identity Center có thể truy cập các tài khoản và ứng dụng AWS bằng thông tin xác thực tổ chức hiện có của họ, mà không cần phải tạo và quản lý các tài khoản và mật khẩu AWS riêng biệt.

Ví dụ, IAM Identity Center có thể kết nối và tự động cấp quyền (provision) người dùng từ các nhà cung cấp danh tính (identity providers) dựa trên tiêu chuẩn, bao gồm Microsoft Active Directory, Okta, Microsoft Entra ID, Google Workspace hoặc một nhà cung cấp danh tính (IdP) được hỗ trợ khác thông qua Ngôn ngữ Đánh dấu Xác nhận Bảo mật (Security Assertion Markup Language - SAML) 2.0 hoặc OIDC.

![Quản lý Truy cập Amazon Q Developer](/images/3-Blog/Blog3-1.png)

**Hình 1**  Quản lý Truy cập Amazon Q Developer thông qua AWS IAM Identity Center.

Đây là một trải nghiệm tuyệt vời cho các nhà phát triển vì họ chỉ cần ủy quyền phiên Q Developer của mình bằng quy trình đăng nhập thông thường thông qua Nguồn danh tính (Identity source) đã có sẵn trong doanh nghiệp của họ. Quản trị viên được hưởng lợi từ các tính năng như quản lý truy cập tập trung, quản lý quyền được tinh giản và các khả năng quản trị viên nâng cao để xem hoạt động người dùng Amazon Q.

---

## Trải nghiệm Thiết lập Đơn giản hóa cho Amazon Q Developer Pro

Phương pháp tiếp cận nêu trên về việc thiết lập IAM Identity Center trong một tài khoản quản lý là lý tưởng nhưng không phải lúc nào cũng khả thi, vì vậy chúng tôi đã tạo ra một trải nghiệm bắt đầu mới giúp các nhóm đang tìm cách dùng thử các tính năng của Amazon Q Developer Pro trong Môi trường Phát triển Tích hợp (IDE) của họ dễ dàng hơn, bắt đầu với:

 Một tài khoản độc lập không phải là một phần của tổ chức được quản lý bởi AWS Organizations.

 Một tài khoản thành viên, không phải là tài khoản quản lý, là một phần của Tổ chức AWS nhưng không có người dùng cấp tổ chức được quản lý trong IAM Identity Center.

Đối với cả tài khoản độc lập và tài khoản thành viên, có một quy trình gồm hai bước. Bước đầu tiên để thiết lập Amazon Q Developer Pro bắt đầu bằng cách điều hướng đến bảng điều khiển Amazon Q và chọn Bắt đầu:

![Bảng điều khiển Amazon Q](/images/3-Blog/Blog3-2.png)

**Hình 2**  Bảng điều khiển Amazon Q  Bắt đầu với Amazon Q.

Thiết lập sẽ hướng dẫn bạn tạo người dùng đầu tiên và kích hoạt đăng ký Amazon Q Developer Pro trong tài khoản của bạn, bước khởi đầu này cũng bao gồm việc tạo một phiên bản tài khoản của IAM Identity Center và một phiên bản ứng dụng Amazon Q Developer do AWS quản lý. Hướng dẫn chi tiết có sẵn trong tài liệu của chúng tôi  Đăng ký người dùng cho Amazon Q Developer Pro.

Khi hoàn tất, người dùng đầu tiên có thể được nhìn thấy trong phần Đăng ký Amazon Q:

![Đăng ký Amazon Q](/images/3-Blog/Blog3-3.png)

**Hình 3**  Đăng ký Amazon Q.

Bước thứ hai là đăng ký các thành viên nhóm bổ sung vào phiên bản tài khoản của IAM Identity Center và sau đó đăng ký họ vào Amazon Q Developer Pro thông qua bảng điều khiển Amazon Q.

![Người dùng IAM Identity Center](/images/3-Blog/Blog3-4.png)

**Hình 4**  Người dùng IAM Identity Center.

Khi người dùng đã đăng ký thành công, họ sẽ nhận được một email với hướng dẫn về cách kích hoạt Đăng ký Amazon Q Developer Pro của họ và bắt đầu sử dụng các tính năng.

Lưu ý rằng các phiên bản tài khoản của IAM Identity Center có những giới hạn. Ví dụ, các phiên bản tài khoản không hỗ trợ truy cập bảng điều khiển. (Người dùng vẫn có thể sử dụng Amazon Q trong bảng điều khiển, chỉ là họ sẽ phải tuân theo các giới hạn hàng tháng của bậc Miễn phí.) Nếu bạn muốn sử dụng Amazon Q Developer Pro trong bảng điều khiển và các trang web AWS khác, bạn phải là người dùng trong một phiên bản tổ chức của IAM Identity Center, trong một tài khoản quản lý.

Tại thời điểm này, cần lưu ý rằng, IAM Identity Center hiện có thể được cấu hình để thay đổi nguồn danh tính của nó thành Nhà cung cấp Danh tính Liên kết (Federated Identity Provider - IdP), hãy xem các trang tài liệu của chúng tôi về cách thay đổi nguồn danh tính của bạn.

---

## Dọn dẹp

Để dọn dẹp tài nguyên được tạo trong bài blog này, trước tiên hãy xóa người dùng Amazon Q Developer Pro bằng cách làm theo hướng dẫn của chúng tôi:

 Hủy đăng ký người dùng khỏi Amazon Q Developer Pro

Thứ hai, xóa phiên bản IAM Identity Center:

 Xóa phiên bản IAM Identity Center của bạn

---

## Kết luận

Bắt đầu với Amazon Q Developer Pro giờ đây thậm chí còn dễ dàng hơn với trải nghiệm thiết lập mới, đơn giản hóa, bạn có thể trải nghiệm các tính năng pro trong IDE của mình, chẳng hạn như giới hạn cao hơn đối với các tính năng nâng cao như:

 Trò chuyện, gỡ lỗi mã, thêm kiểm thử và nhiều hơn nữa trong môi trường nhà phát triển tích hợp (IDE) của bạn.

 Tăng tốc các tác vụ với các tác nhân Amazon Q Developer dành cho phát triển phần mềm.

 Nâng cấp ứng dụng trong một khoảng thời gian ngắn với Tác nhân Amazon Q Developer dành cho chuyển đổi mã.

Hãy tham gia với Hướng dẫn Người dùng Amazon Q Developer về Đăng ký người dùng cho Amazon Q Developer Pro.

Đọc thêm về cách cộng đồng đang sử dụng Amazon Q để viết mã và xây dựng ứng dụng nhanh hơn và dễ dàng hơn với Amazon Q trên community.aws và khám phá những gì chúng tôi đang xây dựng với Amazon Q Developer tại đây.

Lưu ý rằng mặc dù bài đăng này tập trung vào Amazon Q Developer Pro, các nhà phát triển vẫn có thể bắt đầu mà không mất phí và không cần tài khoản AWS; Amazon Q Developer cung cấp Bậc Miễn phí vĩnh viễn với các giới hạn hàng tháng có sẵn cho người dùng, hãy xem hướng dẫn người dùng của chúng tôi về bậc Miễn phí Amazon Q Developer.

---

## Về tác giả:

**Matt Laver**

Matt Laver là Kiến trúc sư Giải pháp Chuyên gia Cấp cao (Senior Specialist Solutions Architect) tại Amazon Web Services (AWS) với trọng tâm là Trải nghiệm Nhà phát triển (Developer Experience). Ông đam mê giúp đỡ khách hàng tìm ra các giải pháp đơn giản cho những vấn đề khó khăn.
