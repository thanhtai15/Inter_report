---
title: "Worklog Tuần 4"
date: "2025-11-05"
weight: 1
chapter: false
pre: " <b> 1.4. </b> "
---


### Mục tiêu Tuần 4:

* Nắm vững quy trình Hybrid Cloud - kết nối giữa On-premises và AWS Cloud:
  * Xuất và nhập Virtual Machines (VMs) giữa VMWare và AWS
  * Tạo AMIs từ VMs đã nhập và triển khai EC2 Instances
  * Tìm hiểu VM Import/Export Service và các yêu cầu kỹ thuật
* Đào sâu kiến thức về AWS Storage Services:
  * EFS (Elastic File System) - file storage chia sẻ được
  * FSx - fully managed file systems (Windows File Server, Lustre)
  * Storage Gateway - kết nối on-premises storage với AWS
  * EC2 Autoscaling để tự động điều chỉnh số lượng instances
  * Lightsail - giải pháp VPS đơn giản cho beginner
* Xây dựng nền tảng toán học cho NLP và Machine Learning:
  * Không gian Vector (Vector Spaces) và các phép toán
  * Euclidean Distance & Cosine Similarity để đo lường tương đồng
  * Xác suất và Bayes' Rule trong phân loại văn bản
  * Đại số tuyến tính với Python Numpy
* Chốt ý tưởng dự án cuối kỳ và thiết lập khung tài liệu:
  * Lựa chọn Hugo theme phù hợp
  * Học cách viết Workshop report bằng Hugo
  * Thống nhất ý tưởng cuối cùng cùng nhóm

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Tìm hiểu về EC2 Autoscaling - EFS/FSx - Lightsail <br> - Bổ sung thêm kiến thức về Basic Storage & Compute services on AWS <br> - Tìm hiểu về Probability and Bayes’ Rule                                                                                             | 29/09/2025   | 29/09/2025      | <https://www.youtube.com/@AWSStudyGroup/> <br><br> <https://www.coursera.org/learn/classification-vector-spaces-in-nlp/>
| 3   | - Tìm hiểu mở rộng về các dịch vụ Database and Security trên AWS <br> - Tìm hiểu VMWare Workstation <br> - Thực hành xuất Virtual Machine từ On-premises <br> - Thực hành upload Virtual Machine lên AWS  | 30/09/2025   | 30/09/2025      | <https://www.youtube.com/@AWSStudyGroup/> |
| 4   | - Học về Linear algebra in Python with Numpy <br> - Học Euclidean Distance & Cosine Similarity <br> - Tìm hiểu Manipulating Words in Vector Spaces <br> - Thực hành các bài lab code về Vector Space Model | 01/10/2025   | 01/10/2025      | <https://www.coursera.org/learn/classification-vector-spaces-in-nlp/>
| 5   | - Nhập Virtual Machine vào AWS <br> - Triển khai Instance từ AMI <br> - Thiết lập ACL bucket S3 <br> - Xuất máy ảo từ Instance <br> - Dọn dẹp tài nguyên trên AWS Cloud <br> - Tạo cổng lưu trữ <br> - Mount File shares on On-premises machine | 02/10/2025   | 02/10/2025      | <https://www.youtube.com/@AWSStudyGroup/> |
| 6   | - Tìm hiểu về Hugo Theme <br> - Tim hiểu cách viết Workshop báo cáo cuối kì <br> - Meeting tổng kết và đưa ra ý tưởng cuối cùng cho báo cáo cuối kì cùng nhóm                                                                                        | 03/10/2025   | 03/10/2025      | <https://www.youtube.com/@AWSStudyGroup/> |


### Thành tựu Tuần 4:

* Đã triển khai thành công các chiến lược Hybrid Cloud:
  * Xuất các máy ảo (VMs) từ VMWare Workstation cục bộ và tải chúng lên AWS.
  * Nhập các máy ảo (VMs) để tạo AMIs và khởi chạy các Instances hoạt động.
  * Xuất các AWS Instances trở lại môi trường cục bộ.

* Cấu hình các Giải pháp Lưu trữ Nâng cao:
  * Triển khai AWS Storage Gateway.
  * Gắn kết (mount) thành công các chia sẻ tệp AWS trực tiếp lên các máy tại chỗ (on-premises).
  * Quản lý S3 Access Control Lists (ACLs) để bảo mật chi tiết.

* Ứng dụng Nền tảng Toán học cho NLP (Machine Learning):
  * Sử dụng Python (Numpy) cho các phép toán Đại số tuyến tính.
  * Tính toán Khoảng cách Euclid & Độ tương đồng Cosine để phân tích văn bản.
  * Hiểu và áp dụng Định lý Bayes và Mô hình Không gian Vector.

* Sự sẵn sàng cho Dự án & Tài liệu:
  * Đã chọn và cấu hình giao diện (Theme) Hugo cho báo cáo cuối cùng.
  * Đạt được sự thống nhất về ý tưởng dự án cuối khóa với nhóm.


