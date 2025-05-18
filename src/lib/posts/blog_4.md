---
title: "Định danh"
date: "2025-5-18"
updated: "2025-5-18"
categories:
  - "sveltekit"
  - "markdown"
coverImage: "https://images.viblo.asia/0a2f42f0-7cde-4457-bdfc-24433c6a4c68.png"
coverWidth: 16
coverHeight: 9
excerpt: Check out how heading links work with this starter in this post.
---

## 1: Diễn giải quy trình khi duyệt trang web www.motvidu.com (Không dùng LLMs)
Quy trình duyệt một trang web:
Khi bạn truy cập www.motvidu.com từ trình duyệt, quy trình xảy ra như sau:

Gõ URL: Người dùng nhập địa chỉ trang web www.motvidu.com vào trình duyệt.

Tra cứu DNS (DNS Lookup):

Trình duyệt kiểm tra bộ nhớ cache cục bộ để xem địa chỉ IP của www.motvidu.com đã được lưu chưa.

Nếu không có trong cache, trình duyệt sẽ hỏi hệ điều hành, rồi đến router, và cuối cùng là DNS resolver của ISP (Nhà cung cấp dịch vụ Internet).

DNS resolver truy vấn DNS root server, sau đó đến top-level domain (TLD) server (.com), và cuối cùng đến authoritative DNS server chứa bản ghi IP của motvidu.com.

Resolving DNS (Giải phân giải DNS):

DNS server trả về địa chỉ IP của www.motvidu.com.

Caching:

Địa chỉ IP được lưu lại ở nhiều cấp: trình duyệt, hệ điều hành, router, DNS resolver để tăng tốc cho lần truy cập sau.

Kết nối TCP và gửi yêu cầu HTTP/HTTPS:

Trình duyệt thiết lập kết nối TCP (hoặc TLS nếu HTTPS) với địa chỉ IP nhận được.

Gửi yêu cầu HTTP GET để lấy nội dung của trang web.

Nhận phản hồi và hiển thị:

Server trả lại nội dung HTML, trình duyệt phân tích và hiển thị nội dung trang web cho người dùng.

Nguồn tham khảo:
Cloudflare DNS Explanation

Mozilla - DNS Basics
## 2: Thuật toán Chord (Distributed Hash Table)
Giới thiệu ngắn gọn:
Chord là một thuật toán phân tán dùng để định vị các node lưu trữ khóa trong hệ thống phân tán (Distributed Hash Table – DHT). Các node được sắp xếp thành vòng tròn với định danh (ID) được băm từ địa chỉ IP hoặc port. Mỗi node biết một số node khác gọi là "finger table" để tìm nhanh vị trí chứa một khóa.

![Code4](/images/code4.png)  
Testcase
![testcase](/images/testcase.png) 
Kết quả testcase  
Khóa 'somekey' (hash=4) được lưu tại: Node(6)
