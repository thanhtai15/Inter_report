---
title: "Event 1"
date: 2024-09-09
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---


# Bài Thu hoạch: AWS AI/ML and Generative AI Workshop

### I. THÔNG TIN VÀ CHƯƠNG TRÌNH 

**Thời gian:** Thứ Bảy, ngày 15 tháng 11 năm 2025, từ 8:30 sáng đến 12:00 trưa  
**Địa điểm:** Văn phòng AWS Việt Nam

#### A. Tóm tắt Chương trình

Chương trình tập trung vào việc giới thiệu các dịch vụ học máy và AI sinh tạo của AWS:

**1. Tổng quan Dịch vụ AWS AI/ML (9:00  10:30 AM)**
- Giới thiệu chi tiết về **Amazon SageMaker** - nền tảng Học máy (ML) end-to-end của AWS
- Nội dung bao gồm:
  - Chuẩn bị và gán nhãn dữ liệu
  - Huấn luyện và tinh chỉnh mô hình
  - Triển khai mô hình
  - Các khả năng MLOps tích hợp
- **Live Demo**: SageMaker Studio

**2. AI Sinh tạo với Amazon Bedrock (10:45 AM  12:00 PM)**
- Tập trung vào việc sử dụng Amazon Bedrock để triển khai AI Sinh tạo
- Các chủ đề chính:
  - So sánh và lựa chọn các Foundation Models (Claude, Llama, Titan)
  - Kỹ thuật Prompt Engineering
    - Chain-of-Thought reasoning
    - Few-shot learning
  - Kiến trúc Retrieval-Augmented Generation (RAG)
  - Tích hợp Knowledge Base
  - Bedrock Agents cho quy trình làm việc đa bước
  - Guardrails để đảm bảo an toàn và lọc nội dung

---

### II. PHƯƠNG PHÁP LUẬN PHÁT TRIỂN HƯỚNG AI (AIDLC)

AIDLC (AI-Driven Development) là một phương pháp luận (methodology) và cách tiếp cận (approach) nhằm tăng tốc độ phát triển phần mềm, với khả năng **rút ngắn thời gian làm việc từ hai tuần xuống khoảng 1.5 ngày**.

#### A. Triết lý Human-Centric (Con người là Trung tâm)

**Không tự động quyết định:**
- Triết lý cốt lõi của AIDLC là **không cho phép AI quyết định bất kỳ điều gì thay thế con người**

**Vai trò của con người:**
- Trách nhiệm của nhà phát triển (developer) và các bên liên quan:
  - **Validation** (Xác nhận)
  - **Decisioning** (Quyết định)
  - **Oversight** (Giám sát)
- Nếu AI đưa ra câu hỏi để làm rõ yêu cầu, con người là người phải trả lời để AI làm tiếp

**Tạo Plan bắt buộc:**
- Khi yêu cầu AI thực hiện bất kỳ công việc nào, bắt buộc nó phải **tạo ra một kế hoạch (plan) trước**
- Lợi ích:
  - Giúp người dùng biết chính xác những gì AI muốn làm
  - Tránh bị quá tải ngữ cảnh (overcontext)
- Nếu plan không chính xác, yêu cầu AI tạo plan mới
- **Lặp lại là một phần quan trọng** của phương pháp luận AIDLC

#### B. Quy trình và Quản lý Ngữ cảnh

**1. Các giai đoạn (Faces) của AIDLC:**

- **Inception**: Giai đoạn bắt đầu
  - Định hình yêu cầu (requirement)
  - Phân chia thành các User Story
  - Nhóm các User Story thành các Unit (Unit of Work)

- **Construction**: Giai đoạn xây dựng
  - Thực hiện triển khai dựa trên các Unit đã được nhóm

- **Operation**: Giai đoạn vận hành
  - Triển khai (deploy)
  - CI/CD

**2. Quản lý Ngữ cảnh (Context Management):**

- **Ưu tiên Ngôn ngữ:**
  - AI hiểu ngữ cảnh ngôn ngữ tốt hơn là code
  - Thay vì đưa toàn bộ source code làm input, nên rút trích thông tin thành:
    - Project summary
    - Kiến trúc kỹ thuật (technical architect)
    - Domain model
  - Điều này giúp AI hiểu rõ hơn và tránh bị quá tải ngữ cảnh

- **Sử dụng Session riêng:**
  - Tạo các session làm việc riêng cho từng task (giống như từng Unit)
  - Kiểm soát ngữ cảnh tốt hơn
  - Giảm thiểu nguy cơ bị sai lệch (hallucination) do ảnh hưởng bởi ngữ cảnh từ các tác vụ trước

**3. Phát triển theo Nhóm (Mob Development):**

- AIDLC đề xuất phương pháp Mob Development
- Nhiều vai trò làm việc chung trên cùng một máy tính:
  - BA (Business Analyst)
  - Engineer
  - Solution Architect
  - QA (Quality Assurance)
- Lợi ích:
  - Tất cả mọi người cùng xác nhận đầu ra (validation) ngay lập tức
  - Tăng tốc độ và hiệu quả công việc

---

### III. CÔNG CỤ TÍCH HỢP AI: KIRO IDE

**Kiro** là Môi trường Phát triển Tích hợp (IDE) của AWS, được xây dựng để **tích hợp AI ngay từ đầu**, tương đối giống với Coder hoặc VS Code.

- Hiện sử dụng các mô hình ngôn ngữ lớn (LLM) như **Claude** (ví dụ: Claude 3.4, 3.7, 4.5)

#### A. Spec-Driven Development (SDD)

**Tính năng cốt lõi:**
- SDD là tính năng được tích hợp sẵn trong Kiro
- Người dùng không bắt đầu bằng code mà bằng cách tạo ra các **tài liệu spec**

**Các file Spec mặc định:**
- Kiro tạo ra ba file cơ bản trong thư mục `.kiro`:
  - `requirement`
  - `design`
  - `task list`

**Hạn chế:**
- SDD được đánh giá là cứng nhắc (rigid) và khó mở rộng cho các dự án lớn
- Phù hợp hơn cho:
  - Các dự án nhỏ
  - Tạo prototype
- Do số lượng tài liệu ít, cho phép AI có nhiều "không gian" để sai sót hơn so với quy trình AIDLC chi tiết

#### B. Tích hợp AIDLC trong Kiro

- Kiro hỗ trợ việc áp dụng các phương pháp luận tùy chỉnh thông qua **Advanced Context Management**
- Cách thực hiện:
  - Định nghĩa luồng công việc AIDLC trong file `steering`
  - Đặt trong thư mục `.kiro/steering`
  - Kiro sẽ tự động chạy các giai đoạn (face) theo quy trình AIDLC đó

#### C. Agent Hooks

- Kiro cho phép tạo **Agent Hooks**, tương tự như webhook nhưng dành cho AI Agent
- Chức năng:
  - Định nghĩa các quy tắc bằng ngôn ngữ tự nhiên
  - Ví dụ: "cứ save file JS là chạy unit test"
  - Tự động hóa các tác vụ dựa trên sự kiện
  - Cho phép AI Agent chính tập trung vào logic cốt lõi

---

### IV. CÁC BÀI HỌC VÀ LỜI KHUYÊN

#### 1. Tư duy Prompting
- Khi yêu cầu AI, cần định nghĩa rõ ràng **vai trò (persona)** của AI
- **Input và Output phải rõ ràng**
- Output nên được ghi lại vào một file cụ thể (như file Markdown) thay vì chỉ lưu trữ trong bộ nhớ tạm (memory)

#### 2. Hạn chế cấm đoán
- **Thay vì:** "đừng làm cái này" (don't implement this)
- **Nên nói:** "hãy implement cái này"
- Lý do: Xác suất AI làm những điều bị cấm là khá cao

#### 3. Tầm quan trọng của Lập trình viên
- Dù AI hỗ trợ phát triển nhanh chóng, **giá trị của lập trình viên** vẫn nằm ở:
  - Khả năng giám sát
  - Xác thực
  - Đưa ra quyết định
- Việc dành thời gian cho validation và oversight là **"thời gian xứng đáng"**

---

### V. VÍ DỤ MINH HỌA

Việc sử dụng AIDLC và Kiro trong phát triển phần mềm giống như việc điều khiển một **chiếc xe tự lái (AI)** trên một lộ trình phức tạp:

- **Bạn (nhà phát triển)** là người:
  - Cung cấp bản đồ chi tiết (Plan)
  - Xác định các điểm dừng quan trọng (Units)
  - Liên tục kiểm tra xem xe có đi đúng hướng không (Validation)

- **Bạn không cần phải lái xe từng mét**, nhưng bạn hoàn toàn **chịu trách nhiệm về mọi quyết định** trên đường đi để đảm bảo đến đích an toàn và hiệu quả.

---

### VI. KẾT LUẬN VÀ ĐÁNH GIÁ CÁ NHÂN

Sự kiện AWS AI/ML and Generative AI Workshop đã mang lại những kiến thức vô cùng quý giá về:
- Cách áp dụng AI vào quy trình phát triển phần mềm một cách có trách nhiệm
- Phương pháp luận AIDLC giúp tăng tốc phát triển mà vẫn đảm bảo chất lượng
- Công cụ Kiro IDE với khả năng tích hợp AI mạnh mẽ

Điểm nổi bật nhất là triết lý **Human-Centric** - nhấn mạnh rằng AI là công cụ hỗ trợ, không phải thay thế con người. Điều này giúp tôi hiểu rõ hơn về vai trò và trách nhiệm của developer trong kỷ nguyên AI.

#### Một số hình ảnh khi tham gia sự kiện
*Thêm các hình ảnh của các bạn tại đây*
