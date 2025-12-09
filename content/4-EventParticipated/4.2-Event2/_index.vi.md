---
title: "Event 2"
date: 2024-09-09
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---


# Bài thu hoạch GenAI-powered App-DB Modernization workshop & DevOps on AWS Workshop

### 1. MỤC ĐÍCH CỦA SỰ KIỆN

Sự kiện kết hợp này nhằm mục đích **chia sẻ văn hóa và các nguyên tắc DevOps** cùng với các phương pháp thực hành tốt nhất trên nền tảng AWS. Đồng thời, workshop cung cấp cơ hội cho người học **tiếp cận nền tảng Cloud và AI**.

**Bối cảnh và Tầm quan trọng:**
- Các nền tảng máy vật lý, máy ảo, và các server cũ hiện tại của doanh nghiệp **không đáp ứng được việc chạy các chip công nghệ AI**
- Doanh nghiệp đang tập trung đầu tư lên Cloud để hỗ trợ công nghệ AI
- Mở ra cơ hội lớn cho các bạn trẻ trong lĩnh vực Cloud và AI

**Workshop nhằm trang bị kiến thức về:**
1. **Các chỉ số đo lường hiệu suất DevOps cốt lõi:**
   - DORA (DevOps Research and Assessment)
   - MTTR (Mean Time to Resolution)
   - Tần suất triển khai (Deployment Frequency)

2. **Triển khai các công nghệ hiện đại trên AWS:**
   - Tích hợp liên tục/Triển khai liên tục (CI/CD)
   - Cơ sở hạ tầng dưới dạng Mã (IaC)
   - Giám sát (Monitoring & Observability)

3. **Xây dựng nền tảng vững chắc:**
   - AI và Cloud
   - Tận dụng cơ hội lớn trong tương lai

---

### 2. DANH SÁCH DIỄN GIẢ

Các diễn giả chính tham gia chia sẻ nội dung bao gồm:

**Lâm Thứ Kiệt** - Senior DevOps Engineer tại FPT Software
- Chia sẻ kinh nghiệm về domain banking
- Triển khai các con chatbot trong thực tế
- Chia sẻ về quy trình DevOps trong môi trường enterprise

**Danh Hoàng Hiếu Nghị** - AI Engineer tại Renob (công ty đối tác của AWS)
- Chia sẻ kinh nghiệm triển khai những ứng dụng AI hoạt động thực tế ngoài đời
- Hướng dẫn về các best practices trong AI deployment

**Linh Lan Hoàng Anh** - Sinh viên năm cuối
- Chia sẻ góc nhìn về các dịch vụ AI mới nhất của AWS
- Đặc biệt là các dịch vụ ngoài Bedrock/SageMaker

---

### 3. NỘI DUNG NỔI BẬT

Nội dung nổi bật của chuỗi workshop bao gồm các phần chính về **DevOps trên AWS** và các **kỹ thuật AI cốt lõi**.

#### A. DevOps Mindset và Principles

**Tinh thần DevOps:**
- Chia sẻ văn hóa và nguyên tắc DevOps
- Lợi ích và các chỉ số chính:
  - **DORA** (DevOps Research and Assessment)
  - **MTTR** (Mean Time to Resolution)
  - Deployment Frequency
  - Change Failure Rate

#### B. CI/CD Pipeline trên AWS

**1. Source Control:**
- Sử dụng **AWS CodeCommit**
- Các chiến lược Git:
  - GitFlow
  - Trunk-based development

**2. Build & Test:**
- Cấu hình **CodeBuild**
- Automated testing
- Build optimization

**3. Deployment:**
- Sử dụng **CodeDeploy** với các chiến lược triển khai:
  - **Blue/Green**: Triển khai song song, chuyển đổi nhanh
  - **Canary**: Triển khai từng phần, giảm rủi ro
  - **Rolling updates**: Cập nhật tuần tự

**4. Orchestration:**
- Tự động hóa pipeline bằng **CodePipeline**
- Workflow automation
- Multi-stage deployment

#### C. Infrastructure as Code (IaC)

**AWS CloudFormation:**
- Template-based infrastructure
- Stack management

**AWS CDK (Cloud Development Kit):**
- Khả năng hỗ trợ nhiều ngôn ngữ (TypeScript, Python, Java, C#)
- Các mẫu tái sử dụng (reusable patterns)
- Type-safe infrastructure

#### D. Monitoring & Observability

**CloudWatch:**
- Metrics collection
- Logs aggregation
- Alarms configuration
- Dashboards visualization

**AWS X-Ray:**
- Phân tích vết phân tán (distributed tracing)
- Performance bottleneck detection
- Khả năng quan sát toàn diện (full-stack observability)

#### E. Foundation Models (FM)

**Đặc điểm của Foundation Models:**
- Được huấn luyện trên tập dữ liệu rất lớn với **hàng tỷ tham số (parameter)**
- Sử dụng **self-supervised learning**
- **Khác biệt so với ML truyền thống:**
  - ML truyền thống: Chỉ xử lý đúng một tác vụ
  - FM: Có thể xử lý rộng và tổng quát hóa nhiều tác vụ chỉ bằng một câu prompt

#### F. Kỹ thuật Prompting

**1. Zero-shot:**
- Chỉ đưa ra hướng dẫn cơ bản
- Không cần ví dụ

**2. Few-shot:**
- Cung cấp context và ví dụ
- Tinh chỉnh đầu ra của mô hình

**3. Chain of Thought (CoT):**
- **Kỹ thuật nền tảng** giúp LLM chia nhỏ câu hỏi
- Suy luận từng bước để đưa ra kết quả chính xác hơn
- **Là nền tảng cho việc hoạt động của AI Agent**

#### G. Retrieval-Augmented Generation (RAG)

**RAG** - Mô hình được nhiều công ty áp dụng

**Ba bước hoạt động:**
1. **Truy xuất (Retrieval)**: Truy xuất thông tin nội bộ từ knowledge space
2. **Kết hợp (Argumentation)**: Kết hợp thông tin với câu hỏi người dùng
3. **Tạo ra (Generation)**: Tạo ra câu trả lời

**Công nghệ Embedding:**
- Chuyển văn bản thành không gian vector N-chiều
- Giúp máy học có thể hiểu được câu văn
- Ví dụ: Amazon Titan Embedding

#### H. Amazon Bedrock Agent Core

**Framework thiết yếu để triển khai và scale ứng dụng AI**

**Giải quyết các bài toán phức tạp:**

1. **Memory Management:**
   - Giúp AI nhớ bối cảnh người dùng
   - Duy trì context qua nhiều phiên

2. **Identity:**
   - Phân quyền (Authorization)
   - Quản lý người dùng

3. **Tool Calling:**
   - Tự động hóa các hành động
   - Gọi API nội bộ
   - Sử dụng browser tool để tương tác với trình duyệt web

#### I. Các Dịch vụ AI được Train Sẵn của AWS

**Pre-trained AI Services** - Chỉ cần gọi qua API:

**1. Amazon Recognition**
- Thị giác máy tính (Computer Vision)

**2. Amazon Translate**
- Dịch thuật ngôn ngữ tự nhiên
- Khác với dịch dựa trên query

**3. Amazon Transcribe**
- Chuyển giọng nói thành văn bản
- Hỗ trợ streaming
- Multi-speaker recognition

**4. Amazon Polly**
- Chuyển văn bản thành lời nói
- Text-to-speech cho call center

**5. Amazon Comprehend**
- Xử lý ngôn ngữ tự nhiên (NLP)
- Phân tích cảm xúc (sentiment analysis)
- Phát hiện thông tin nhạy cảm

**6. Amazon Kendra**
- Tìm kiếm doanh nghiệp nâng cao (Enterprise search)
- Hỗ trợ tìm kiếm ngữ nghĩa
- Hỗ trợ RAG trong tài liệu nội bộ

---

### 4. NHỮNG GÌ HỌC ĐƯỢC

#### Quy trình DevOps Toàn diện
- Nắm vững các thành phần của **CI/CD pipeline trên AWS**
- Hiểu rõ các chiến lược triển khai tiên tiến:
  - Blue/Green deployment
  - Canary deployment
  - Rolling updates

#### Tiêu chí Đánh giá Sản phẩm
- Để sản phẩm được coi là **"đạt"** (để có điểm):
  - Phải là **"sản phẩm chạy được"** chứ không phải là sản phẩm trên giấy
  - Hoàn thành khoảng **5 đến 6 tính năng** trong số 10 tính năng đề xuất
- Ví dụ: Trang thương mại điện tử phải:
  - Thấy hàng
  - Bỏ vào giỏ hàng
  - Thanh toán được

#### Tư duy Hiện đại hóa Hạ tầng
- Nhận thức rõ rằng các doanh nghiệp đang tập trung đầu tư lên Cloud
- Hệ thống cũ không hỗ trợ chạy chip AI
- **Điều này mở ra cơ hội lớn cho các bạn trẻ**

#### Tối ưu hóa Chi phí AI
- Cần tối ưu hóa câu từ và tinh chỉnh keyword trong prompting
- Tránh lan man, giúp giảm input token
- Tiết kiệm chi phí tính toán của mô hình LLM

#### Khả năng Suy luận của AI
- **CoT là kỹ thuật quan trọng** giúp LLM suy luận
- Đưa ra kết quả chính xác hơn
- **Là nền tảng cho các tác vụ phức tạp của AI Agent**

---

### 5. ỨNG DỤNG VÀO CÔNG VIỆC

#### A. Tích hợp CI/CD

**Quy trình triển khai tự động:**
- Áp dụng **CodePipeline** và các dịch vụ liên quan
- Tự động hóa quy trình triển khai
- Sử dụng các chiến lược như **Blue/Green** để giảm thiểu thời gian ngừng hoạt động

**Lợi ích:**
- Tăng tốc độ delivery
- Giảm human error
- Cải thiện quality assurance

#### B. Quản lý Sự cố

**Incident Management:**
- Áp dụng các quy trình quản lý sự cố
- Báo cáo postmortem
- Continuous improvement trong môi trường DevOps

#### C. Phát triển Sản phẩm AI có khả năng Scale

**Chuyển đổi từ Local sang Production:**
1. Sử dụng **Bedrock Agent Core**
2. Chuyển các ứng dụng AI từ local host sang hệ thống multi-user
3. Đảm bảo quản lý:
   - **Memory** (context retention)
   - **Identity** (authorization)
   - **Tool calling** (API integration)

#### D. Xây dựng Hồ sơ Chuyên nghiệp

**Portfolio Development:**
- Hoàn thiện sản phẩm đạt chuẩn **"chạy được"**
- Đưa vào hồ sơ và CV
- Tăng cơ hội thực tập hoặc việc làm sắp tới

---

### 6. TRẢI NGHIỆM TRONG EVENT

#### Demo CI/CD và Observability
- Được xem **Demo trực tiếp** về việc triển khai CI/CD pipeline hoàn chỉnh
- Thiết lập khả năng quan sát toàn diện (full-stack observability setup)
- Hiểu rõ cách các thành phần tương tác với nhau

#### Bedrock Agent Core Browser Tool
- Được giới thiệu và xem demo về việc sử dụng Bedrock Agent Core
- **Browser tool** để tự động hóa các hành động trên trình duyệt web
- Thấy được khả năng mạnh mẽ của AI automation

#### Tương tác với Chuyên gia
- Có cơ hội **trao đổi với các chuyên gia**
- Kinh nghiệm thực tế trong lĩnh vực ngân hàng (domain banking)
- Triển khai chatbot trong production environment

#### Lộ trình Nghề nghiệp
- Hiểu rõ về các con đường sự nghiệp DevOps
- Lộ trình chứng chỉ AWS
- Career guidance từ senior engineers

#### Pre-trained AI Services
- Hiểu cách sử dụng các dịch vụ AI được train sẵn của AWS
- Ví dụ: Translate, Transcribe, Polly, Kendra
- Giải quyết các bài toán cụ thể **mà không cần training mô hình từ đầu**

---

### 7. BÀI HỌC RÚT RA

#### 1. Chất lượng Sản phẩm Thực tế
- **Sản phẩm công nghệ phải là sản phẩm có thể chạy được**
- Hoàn thành các tính năng cốt lõi đã đề xuất
- Không chỉ dừng lại ở thiết kế hoặc document

#### 2. Tối ưu hóa Prompting
- Việc tối ưu hóa câu từ và keyword là **rất quan trọng**
- Giảm chi phí token
- Cải thiện chất lượng phản hồi từ mô hình ngôn ngữ lớn (LLM)

#### 3. RAG là Giải pháp Kết hợp Kiến thức
- Mô hình RAG là giải pháp hiệu quả
- Tích hợp **Foundation Model** với kiến thức nội bộ của doanh nghiệp
- Thông qua quá trình **Embedding**

#### 4. DevOps Cần Sự Đồng bộ
- Thành công trong DevOps không chỉ là sử dụng công cụ
- Cần áp dụng **văn hóa và nguyên tắc phù hợp**
- Sử dụng các công cụ như CloudWatch/X-Ray để duy trì khả năng quan sát hệ thống

---

### 8. KẾT LUẬN VÀ ĐÁNH GIÁ

Workshop **"GenAI-powered App-DB Modernization & DevOps on AWS"** đã cung cấp cái nhìn toàn diện về:
- Quy trình DevOps hiện đại trên AWS
- Công nghệ Generative AI và cách triển khai thực tế
- Sự kết hợp giữa DevOps và AI để xây dựng sản phẩm scalable

#### So sánh Minh họa

> **Việc phát triển AI hiện nay giống như việc xây dựng một thành phố:**
> 
> - Ban đầu, bạn có thể xây dựng một **ngôi nhà đơn lẻ** (ứng dụng local host)
> - Nhưng nếu bạn muốn **cả ngàn người có thể sử dụng cùng một lúc** (scale)
> - Bạn không thể chỉ sao chép ngôi nhà đó
> - Mà cần một **hệ thống quản lý**:
>   - Giao thông (routing)
>   - Điện nước (resources)
>   - An ninh chung (security)
> - **Bedrock Agent Core** đóng vai trò như hệ thống quản lý này
> - Đảm bảo mọi thứ hoạt động trơn tru và có thể mở rộng

**Đây là nền tảng quan trọng** giúp sinh viên chuẩn bị cho:
- Thị trường lao động trong kỷ nguyên AI
- Sự nghiệp trong lĩnh vực Cloud và DevOps
- Xây dựng các sản phẩm công nghệ hiện đại

#### Một số hình ảnh khi tham gia sự kiện
*Thêm các hình ảnh của các bạn tại đây*
