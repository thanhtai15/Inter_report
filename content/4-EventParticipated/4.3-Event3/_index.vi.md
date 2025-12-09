---
title: "Event 3"
date: 2024-09-09
weight: 3
chapter: false
pre: " <b> 4.3. </b> "
---

# Bài Thu hoạch Mastering AWS DevOps: CI/CD, IaC, and Containers


### 1. THÔNG TIN CHUNG VỀ SỰ KIỆN

**Tên Sự kiện:** Mastering AWS DevOps: CI/CD, IaC, and Containers

**Thời gian và Địa điểm:**
- Ngày: Thứ Hai, ngày 17 tháng 11, 2025
- Thời gian: 8:30 AM  5:00 PM
- Địa điểm: AWS

**Phạm vi:** Workshop chuyên sâu về DevOps trên nền tảng AWS, tập trung vào CI/CD, Infrastructure as Code, và Container technologies.

---

### 2. NỘI DUNG VÀ KHÁI NIỆM CHÍNH

#### A. Tư duy và Nguyên tắc DevOps

**Định nghĩa DevOps:**
- DevOps là **cầu nối nằm giữa Development (Dev) và Operation (Ops)**
- Đòi hỏi người làm DevOps phải hiểu rõ cả hai mảng
- **Giải quyết vấn đề:** Tại sao code chạy trên máy của lập trình viên nhưng lại không chạy trên máy chủ (server)

**Mục tiêu cốt lõi:**
- **Tự động hóa (Automation)** là ý chính đầu tiên của DevOps
- Mục đích: Giảm thiểu lỗi do yếu tố con người

**Chỉ số đo lường chính:**
1. **DORA** (DevOps Research and Assessment)
2. **MTTR** (Mean Time to Resolution - Thời gian trung bình để phục hồi)
3. **Deployment Frequency** (Tần suất triển khai)

**Giá trị của Metrics:**
- Theo dõi các chỉ số này tạo ra **bức tranh toàn cảnh** cho các bên liên quan (stakeholders)
- Giúp họ thấy được giá trị đầu tư vào DevOps

---

#### B. CI/CD Pipeline trên AWS

Workshop tập trung vào các dịch vụ cốt lõi của AWS cho **Continuous Integration/Continuous Deployment (CI/CD)**.

**1. Kiểm soát Nguồn (Source Control):**
- Sử dụng **AWS CodeCommit**
- Các chiến lược Git:
  - GitFlow
  - Trunk-based development

**2. Xây dựng và Kiểm thử (Build & Test):**
- Cấu hình **CodeBuild**
- Xây dựng các pipeline kiểm thử
- **Quan trọng:** Không chỉ là xây dựng mà còn phải liên tục kiểm tra (testing) code
- **Áp dụng với AI:** Ngay cả khi code được tạo ra bởi AI, vẫn cần testing

**3. Triển khai (Deployment):**
- Sử dụng **CodeDeploy** với các phương thức triển khai tiên tiến:
  - **Blue/Green**: Triển khai song song, chuyển đổi nhanh
  - **Canary**: Triển khai dần dần, giảm rủi ro
  - **Rolling updates**: Cập nhật tuần tự

**4. Điều phối (Orchestration):**
- Tự động hóa toàn bộ quy trình bằng **AWS CodePipeline**

**Phân biệt CI, CD và Continuous Deployment:**

**Continuous Integration (CI):**
- Quy trình hoạt động của các nhóm Dev
- Bao gồm:
  - Quản lý mã nguồn
  - Phân quyền
  - Build container (ví dụ: Docker file)
  - Tự động quét code để kiểm tra chất lượng và bảo mật

**Continuous Delivery (CD):**
- Quá trình triển khai sản phẩm tự động
- **Cần có sự can thiệp thủ công** (bấm nút đồng ý)
- Sau khi vượt qua các bước kiểm thử

**Continuous Deployment:**
- Quá trình triển khai **hoàn toàn tự động**
- Từ commit code đến khi ứng dụng chạy trên production
- **Không cần can thiệp thủ công**

---

#### C. Infrastructure as Code (IaC)

**IaC là gì:**
- Sử dụng **code để triển khai và quản lý hạ tầng**

**Ưu điểm của IaC:**

1. **Tự động hóa nhanh chóng:**
   - Tạo hàng trăm máy chủ chỉ với một công thức

2. **Tính nhất quán:**
   - Đảm bảo cấu hình không bị sai lệch

3. **Portable (Di chuyển dễ dàng):**
   - Hỗ trợ chuyển đổi môi trường dễ dàng
   - Chỉ cần đem code qua môi trường khác

4. **Documentation (Tài liệu hóa):**
   - Code đóng vai trò là tài liệu
   - Người khác có thể đọc và hiểu cách hạ tầng hoạt động

**Vấn đề Click Ops:**
- Việc cấu hình bằng cách **"bấm chuột" trên console (Click Ops):**
  -  Rất tốt để học service
  -  Không hiệu quả trong môi trường doanh nghiệp
- **Lý do:**
  - Chậm
  - Dễ sai sót
  - Thiếu tính nhất quán

**Các công cụ IaC chính:**

**1. AWS CloudFormation:**

**Khái niệm cơ bản:**
- Dùng templates (công thức, menu) để định nghĩa các tài nguyên AWS
- Hỗ trợ YAML hoặc JSON

**Stack:**
- Tập hợp các tài nguyên AWS được triển khai theo template

**Drift Detection:**
- Tính năng quan trọng giúp phát hiện những thay đổi được thực hiện thủ công trên console (Click Ops)
- Những thay đổi không nằm trong template
- Đảm bảo hạ tầng luôn đồng nhất với code

**2. AWS CDK (Cloud Development Kit):**

**Đặc điểm:**
- Framework sử dụng ngôn ngữ lập trình quen thuộc:
  - Python
  - TypeScript
  - Java
  - C#

**Constructs:**
- Các khối xây dựng cơ bản
- Ba cấp độ:
  - **Level 1:** Gần với CloudFormation (L1 constructs)
  - **Level 2:** High-level abstractions (L2 constructs)
  - **Level 3:** Các pattern kiến trúc sẵn có (patterns)

**Quy trình:**
- CDK chuyển đổi code thành template CloudFormation
- Sau đó triển khai lên AWS

**3. Terraform:**

**Đặc điểm:**
- Tool IaC **đa đám mây (multi-cloud)**
- Có thể sử dụng cho:
  - AWS
  - Azure
  - GCP

**Ngôn ngữ:**
- Sử dụng **HCL (HashiCorp Configuration Language)**
- Được đánh giá là dễ hiểu

**Terraform Plan:**
- Tính năng quan trọng
- Cho phép **xem trước các thay đổi** sẽ xảy ra
- Trước khi áp dụng (apply) lên hạ tầng
- Giúp kiểm soát tốt hơn

---

#### D. Dịch vụ Container và Giám sát

**Container Services:**

**Docker:**
- Nền tảng containerization cơ bản

**Microservices:**
- Kiến trúc ứng dụng phân tán

**Amazon ECR (Elastic Container Registry):**
- Lưu trữ image

**Orchestration Services:**
- **Amazon ECS** (Elastic Container Service)
- **Amazon EKS** (Elastic Kubernetes Service)

**AWS App Runner:**
- Giải pháp triển khai container đơn giản hóa
- Deploy containerized applications nhanh chóng

**Monitoring & Observability:**

**CloudWatch:**
- Thu thập metrics
- Quản lý logs
- Cấu hình alarms
- Tạo dashboards

**AWS X-Ray:**
- Cung cấp khả năng **truy vết phân tán (distributed tracing)**
- Hiểu rõ hiệu suất của các dịch vụ
- Phân tích bottlenecks

**Tầm quan trọng của Monitoring:**
- Xây dựng hệ thống giám sát là cần thiết
- Đánh giá hiệu suất hệ thống
- Ví dụ: Trang web chạy dưới 1 giây, dưới 5 giây
- Đo lường và cải thiện user experience

---

### 3. THỰC TIỄN TỐT NHẤT (BEST PRACTICES)

#### A. Kỹ năng chữ T (T-shaped Skills)

**Mô hình T-shaped:**
- **Trục dọc (Depth):** Đi sâu vào một mảng cụ thể
  - Ví dụ: Linux, Docker
- **Trục ngang (Breadth):** Mở rộng kiến thức tổng quát
  - Ví dụ: Kubernetes, AI application support

**Lợi ích:**
- Chuyên sâu trong một lĩnh vực
- Có khả năng làm việc đa dạng
- Giao tiếp tốt với các team khác

#### B. Tập trung vào Nền tảng (Fundamental)

**Khởi điểm quan trọng:**
- Nên xuất phát từ kiến thức nền tảng:
  - **System Fundamental:** Hiểu hệ thống, networking, OS
  - **Developer Fundamental:** Lập trình, algorithms, design patterns

**Tại sao quan trọng:**
- Nền tảng vững giúp học công nghệ mới nhanh hơn
- Hiểu sâu hơn cách công cụ hoạt động

#### C. Tài liệu hóa (Documentation)

**Tầm quan trọng:**
- Ghi lại toàn bộ quá trình, tính năng, và cấu trúc
- Chia sẻ kiến thức trong team
- **Tránh việc phải giải thích lặp đi lặp lại** cho các thành viên khác

**Tiêu chí tài liệu tốt:**
- Viết rõ ràng
- **Cả những người không có chuyên môn cũng có thể hiểu**
- Có ví dụ cụ thể
- Cập nhật thường xuyên

#### D. Thực hành (Practice)

**Nguyên tắc học tập:**
- **Hạn chế:** Xem video hướng dẫn rồi bỏ qua
- **Nên:** Thực hành thực tế

**Lý do:**
- Khi thực hành sẽ gặp nhiều vấn đề phát sinh
- Giúp hiểu sâu hơn về công nghệ

**Với AI-generated Code:**
- **Hạn chế:** Sao chép code được tạo bởi AI mà không hiểu
- **Nên:** Đọc hiểu code, test kỹ càng

#### E. Quản lý Dự án (Project Management)

**Trong quá trình phát triển (ví dụ: làm đồ án):**

**Sử dụng công cụ quản lý tác vụ:**
- Jira
- Trello
- GitHub Projects

**Các thành phần cần quản lý:**
- **Chia task:** Break down công việc thành các task nhỏ
- **Quản lý backlog:** Danh sách công việc cần làm
- **Future roadmap:** Kế hoạch phát triển dài hạn

**Lợi ích:**
- Theo dõi tiến độ rõ ràng
- Phân công công việc hiệu quả
- Dễ dàng review và cải thiện

#### F. Soft Skills

**Tầm quan trọng:**
- Kỹ năng mềm **rất quan trọng đối với dân kỹ thuật**
- Đặc biệt trong vai trò DevOps

**Kỹ năng diễn đạt:**
- Khả năng diễn đạt thông tin một cách rõ ràng và dễ hiểu
- **DevOps đóng vai trò là cầu nối giữa các nhóm:**
  - Development team
  - Operations team
  - Business stakeholders

**Các kỹ năng mềm cần thiết:**
- Communication (Giao tiếp)
- Collaboration (Hợp tác)
- Problem-solving (Giải quyết vấn đề)
- Empathy (Đồng cảm)
- Presentation (Thuyết trình)

---

### 4. BÀI HỌC RÚT RA

#### 1. DevOps là Văn hóa, không chỉ là Công cụ
- Thành công trong DevOps cần:
  - Mindset đúng đắn
  - Collaboration giữa các teams
  - Automation và continuous improvement

#### 2. Infrastructure as Code là Bắt buộc
- Không thể phụ thuộc vào Click Ops trong môi trường production
- IaC đảm bảo:
  - Consistency (Nhất quán)
  - Reproducibility (Tái tạo được)
  - Version control (Kiểm soát phiên bản)

#### 3. Tự động hóa Kiểm thử là Không thể Thiếu
- Ngay cả với AI-generated code, vẫn cần testing
- CI/CD pipeline phải bao gồm:
  - Unit tests
  - Integration tests
  - Security scans
  - Performance tests

#### 4. Monitoring là Continuous Process
- Không phải "set and forget"
- Cần:
  - Theo dõi metrics liên tục
  - Analyze trends
  - Cải thiện dựa trên data

#### 5. T-shaped Skills giúp Phát triển Sự nghiệp
- Chuyên sâu một lĩnh vực
- Mở rộng kiến thức đa dạng
- Tăng giá trị trong thị trường lao động

---

### 5. ỨNG DỤNG VÀO CÔNG VIỆC

#### A. Xây dựng CI/CD Pipeline hoàn chỉnh
- Áp dụng CodeCommit, CodeBuild, CodeDeploy, CodePipeline
- Implement automated testing
- Sử dụng Blue/Green hoặc Canary deployment

#### B. Chuyển đổi sang Infrastructure as Code
- Bắt đầu với CloudFormation hoặc Terraform
- Document toàn bộ infrastructure
- Version control tất cả IaC code

#### C. Containerize Applications
- Sử dụng Docker để containerize
- Deploy lên ECS hoặc EKS
- Implement proper logging và monitoring

#### D. Cải thiện Observability
- Setup CloudWatch dashboards
- Implement X-Ray tracing
- Define meaningful alarms

#### E. Xây dựng Documentation Culture
- Document architecture decisions
- Write runbooks
- Share knowledge với team

---

### 6. KẾT LUẬN

Workshop **"Mastering AWS DevOps: CI/CD, IaC, and Containers"** đã cung cấp kiến thức toàn diện về:
- DevOps mindset và principles
- CI/CD implementation trên AWS
- Infrastructure as Code với CloudFormation, CDK, Terraform
- Container orchestration và monitoring
- Best practices cho DevOps engineers

**Điểm nhấn quan trọng:**
> DevOps không chỉ là sử dụng công cụ hay tự động hóa, mà là một **văn hóa làm việc** đòi hỏi sự hợp tác giữa các teams, tư duy về automation và continuous improvement, cùng với khả năng giao tiếp tốt để làm cầu nối giữa Development và Operations.

**Workshop này là nền tảng quan trọng** giúp:
- Hiểu rõ DevOps practices hiện đại
- Áp dụng AWS services hiệu quả
- Phát triển T-shaped skills
- Chuẩn bị cho sự nghiệp DevOps Engineer

#### Một số hình ảnh khi tham gia sự kiện
*Thêm các hình ảnh của các bạn tại đây*
