---
title: "Ứng dụng phân tán - Bài 1"
date: "2025-4-29"
updated: "2025-4-29"
categories:
  - "sveltekit"
  - "markdown"
coverImage: "https://solutionias.com/wp-content/uploads/2023/05/dien-toan-phan-tan-1.jpg"
coverWidth: 16
coverHeight: 9
excerpt: Check out how heading links work with this starter in this post.
---

## Ứng dụng phân tán là gì?
![He thong phan tan](https://www.fiahub.com/blog/wp-content/uploads/2024/08/a1-4.png)
Hệ thống phân tán (Distributed System) là một hệ thống trong đó các thành phần tính toán được phân bố trên nhiều vị trí địa lý khác nhau, nhưng hoạt động như một hệ thống thống nhất . Các máy tính trong hệ thống phân tán có thể độc lập và không phụ thuộc lẫn nhau, nhưng chúng kết nối với nhau qua mạng để phối hợp và chia sẻ tài nguyên
## Ứng dụng của hệ thống phân tán.
Hệ thống phân tán được sử dụng rộng rãi trong nhiều lĩnh vực, bao gồm:

- Mạng xã hội: Các nền tảng như Facebook và Twitter sử dụng hệ thống phân tán để xử lý lượng lớn dữ liệu người dùng.
- Điện toán đám mây: Các dịch vụ như Amazon Web Services (AWS) và Google Cloud Platform sử dụng hệ thống phân tán để cung cấp tài nguyên tính toán và lưu trữ dữ liệu.
- Bán lẻ trực tuyến: Các trang web như Amazon và eBay sử dụng hệ thống phân tán để quản lý hàng triệu giao dịch mỗi ngày.
## Các khái niệm chính của hệ thống phân tán
Một số khái niệm chính trong hệ thống phân tán bao gồm:

- Scalability (Khả năng mở rộng): Khả năng của hệ thống để xử lý lượng công việc tăng lên bằng cách thêm tài nguyên.
- Fault Tolerance (Khả năng chịu lỗi): Khả năng của hệ thống để tiếp tục hoạt động khi một phần của hệ thống gặp lỗi.
- Availability (Tính sẵn sàng): Khả năng của hệ thống để luôn sẵn sàng phục vụ người dùng.
- Transparency (Tính trong suốt): Người dùng không cần biết chi tiết về vị trí hoặc cách thức thực hiện tác vụ.
- Concurrency (Tính đồng thời): Khả năng của hệ thống để xử lý nhiều tác vụ cùng một lúc.
- Parallelism (Tính song song): Khả năng của hệ thống để thực hiện nhiều tác vụ đồng thời.
- Openness (Tính mở): Khả năng của hệ thống để tích hợp với các thành phần khác nhau.
- Vertical Scaling (Mở rộng theo chiều dọc): Tăng khả năng xử lý của một máy tính bằng cách thêm tài nguyên.
- Horizontal Scaling (Mở rộng theo chiều ngang): Tăng khả năng xử lý bằng cách thêm nhiều máy tính.
- Load Balancer (Cân bằng tải): Phân phối công việc đều giữa các máy tính trong hệ thống.
- Replication (Sao chép): Tạo bản sao của dữ liệu để tăng tính sẵn sàng và khả năng chịu lỗi.
## Kiến trúc của hệ thống phân tán.
Kiến trúc của hệ thống phân tán có thể được phân loại thành nhiều kiểu khác nhau:   
- Kiến trúc máy khách - máy chủ (Client-Server): Máy khách gửi yêu cầu đến máy chủ để xử lý dữ liệu và trả kết quả.
- Kiến trúc ngang hàng (Peer-to-Peer, P2P): Mỗi nút đều có thể đóng vai trò là máy khách hoặc máy chủ, giúp chia sẻ tài nguyên giữa các nút.  
- Kiến trúc phân tầng: Các chức năng của hệ thống được phân rã thành các tầng, mỗi tầng thực hiện một nhiệm vụ cụ thể.
![Phan tang](https://images.viblo.asia/3096d3e9-720b-4e1f-a3a3-9c02034745d8.png)