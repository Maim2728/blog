---
title: "Đề xuất dự án"
date: "2025-5-11"
updated: "2025-5-11"
categories:
  - "sveltekit"
  - "markdown"
coverImage: "https://camo.githubusercontent.com/b1d7b6267939d9a3e3b6335ad4261f9fd6047b8855a28f89a26b95885cf3c45d/68747470733a2f2f696d6775722e636f6d2f5a454746566f362e706e67"
coverWidth: 16
coverHeight: 9
excerpt: Check out how heading links work with this starter in this post.
---

## Đề xuất đề tài
Tên đề tài:
Ứng dụng GhostDB làm hệ thống cache phân tán cho ứng dụng web

Mô tả:
Trong các hệ thống web có lượng truy cập lớn, dữ liệu thường được truy vấn nhiều lần (như danh sách sản phẩm, thông tin người dùng, top trending, v.v). Việc mỗi lần truy vấn đều phải gọi đến cơ sở dữ liệu chính (database) sẽ gây quá tải, làm giảm hiệu suất hệ thống.

Giải pháp:
Sử dụng GhostDB như một lớp cache phân tán giúp lưu trữ tạm thời các dữ liệu được truy xuất thường xuyên. Khi có yêu cầu, ứng dụng web sẽ kiểm tra GhostDB trước (cache hit). Nếu không có, nó mới gọi đến database (cache miss), sau đó lưu lại kết quả vào GhostDB.

Thực nghiệm:
So sánh hiệu năng của hệ thống web (tốc độ phản hồi, số lần truy cập DB chính) khi có và không có GhostDB, dựa trên một trang web bán hàng mẫu.

## Mục đích, điểm mạnh, điểm yếu, so sánh với thư viện khác
 Mục đích của GhostDB:
GhostDB là một cơ sở dữ liệu key-value in-memory (lưu trên RAM), hoạt động thông qua TCP socket. Mục đích là để lưu trữ dữ liệu tạm thời, dễ truy cập, nhanh, và có thể phân tán trên nhiều node.

 Giải quyết vấn đề gì?

Tăng hiệu suất truy cập dữ liệu tạm thời (cache)

Tối ưu khả năng xử lý đồng thời

Giảm tải cho cơ sở dữ liệu chính

Tương thích dễ dàng với các ứng dụng phân tán

 Điểm mạnh:

Giao tiếp nhanh qua TCP, không cần máy chủ nặng

Dễ triển khai, cài đặt nhẹ

Hỗ trợ tự động xóa key theo thời gian (TTL)

Hoạt động tốt trong các kiến trúc microservices, realtime

 Điểm yếu:

Không có tính năng lưu dữ liệu bền vững (persistent storage)

Bảo mật cơ bản, không hỗ trợ xác thực phức tạp

Chưa phổ biến như Redis, ít tài liệu và cộng đồng hỗ trợ
## Mục tiêu:
Xây dựng một ứng dụng web mẫu (web bán hàng) và tích hợp GhostDB làm lớp cache để tăng hiệu năng khi truy xuất dữ liệu.
## Kế hoạch dự kiến:
Dưới đây là kế hoạch công việc chi tiết cho từng tuần:

- Tuần 1: Tìm hiểu GhostDB, cài đặt server
Nghiên cứu GhostDB: Tìm hiểu về GhostDB, các tính năng, cách hoạt động và lợi ích của việc sử dụng GhostDB làm lớp cache.
Cài đặt server GhostDB:
Tải và cài đặt GhostDB từ trang web chính thức.
Cấu hình server GhostDB để đảm bảo hoạt động ổn định.
Kiểm tra kết nối và xác nhận server hoạt động đúng cách.
- Tuần 2: Xây dựng ứng dụng web mẫu (Node.js/Express hoặc Django)
Chọn framework: Quyết định sử dụng Node.js/Express hoặc Django để xây dựng ứng dụng web mẫu.
Xây dựng ứng dụng web:
Tạo cấu trúc dự án.
Xây dựng các chức năng cơ bản như đăng nhập, đăng ký, hiển thị danh sách sản phẩm và profile người dùng.
Kiểm tra và đảm bảo ứng dụng hoạt động đúng cách.
- Tuần 3: Tích hợp GhostDB làm lớp cache
Tích hợp GhostDB:
Cài đặt và cấu hình GhostDB trong ứng dụng web.
Lưu danh sách sản phẩm và profile người dùng vào GhostDB.
Kiểm tra và đảm bảo dữ liệu được lưu và truy xuất từ GhostDB đúng cách.
- Tuần 4: So sánh hiệu năng
Đo hiệu năng:
Sử dụng Apache Benchmark và Postman để đo hiệu năng của ứng dụng web có và không có GhostDB.
Đo log DB để phân tích chi tiết hiệu năng.
So sánh kết quả:
So sánh kết quả đo hiệu năng giữa hai trường hợp.
Phân tích sự khác biệt và xác định lợi ích của việc sử dụng GhostDB.
- Tuần 5: Viết báo cáo
Đánh giá và biểu đồ hiệu năng:
Tổng hợp kết quả đo hiệu năng và tạo biểu đồ để minh họa sự khác biệt.
Đánh giá ưu nhược điểm của việc sử dụng GhostDB.
Viết báo cáo:
Viết báo cáo chi tiết về quá trình thực hiện, kết quả đo hiệu năng, và đánh giá tổng quan.
Đưa ra kết luận và khuyến nghị dựa trên kết quả thu được.