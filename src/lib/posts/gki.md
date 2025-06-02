---
title: "Đề xuất dự án"
date: "2025-5-11"
updated: "2025-5-11"
categories:
  - "sveltekit"
  - "markdown"
coverImage: "https://digitalis.io/wp-content/uploads/2020/12/Elastic600x340.jpg"
coverWidth: 16
coverHeight: 9
excerpt: Check out how heading links work with this starter in this post.
---

## 1. Đề tài:
Ứng dụng ElasticSearch trong xây dựng hệ thống tìm kiếm phân tán cho website bán trà trực tuyến

## 2. Mô tả vấn đề cần giải quyết:
Trong các website bán trà trực tuyến, khách hàng thường tìm kiếm các loại trà theo tên, mô tả, hương vị, giá, xuất xứ... Với số lượng sản phẩm đa dạng và dữ liệu lớn, hệ thống tìm kiếm truyền thống (dựa trên SQL, LIKE query) thường chậm và không chính xác khi xử lý tìm kiếm full-text, tìm kiếm gần đúng hoặc truy vấn phức tạp.

Ngoài ra, khi lượng truy cập tăng lên đột biến (ví dụ các mùa khuyến mãi, sự kiện), hệ thống cần phải đảm bảo tốc độ phản hồi nhanh, không bị nghẽn hoặc downtime. Do đó, hệ thống tìm kiếm cần phải:

Xử lý nhanh các truy vấn tìm kiếm full-text, hỗ trợ phân tán dữ liệu.

Mở rộng linh hoạt khi dữ liệu và người dùng tăng lên.

Đảm bảo độ chính xác, khả năng lọc nâng cao, phân tích dữ liệu để gợi ý sản phẩm.

## 3. Lý do chọn đề tài:
ElasticSearch là thư viện tìm kiếm phân tán mã nguồn mở hàng đầu, tối ưu cho dữ liệu lớn, full-text, phi cấu trúc.

Thư viện hỗ trợ phân tán (cluster), tự động cân bằng dữ liệu, mở rộng quy mô dễ dàng, rất phù hợp với hệ thống thương mại điện tử có lưu lượng truy cập lớn.

Qua đề tài, ta có thể vận dụng kiến thức về hệ thống phân tán (cluster, sharding, replication), đồng thời hiểu sâu về hoạt động, ưu điểm và nhược điểm của ElasticSearch.

Giúp cải thiện trải nghiệm người dùng bằng công cụ tìm kiếm chính xác và nhanh chóng trên website bán trà.

## 4. Bản chất thư viện ElasticSearch
4.1. Nguyên lý hoạt động
ElasticSearch lưu trữ dữ liệu dưới dạng index (giống như bảng trong CSDL), mỗi index chia thành nhiều shard để phân tán dữ liệu trên nhiều node.

Dữ liệu trong index được lưu dưới dạng document (bản ghi JSON).

Tìm kiếm sử dụng công nghệ full-text search dựa trên Apache Lucene, hỗ trợ phân tích cú pháp, tokenization, stemming, fuzziness...

Hỗ trợ các loại truy vấn đa dạng: full-text, term query, range query, aggregation, geo, suggesters...

Cluster ElasticSearch tự động quản lý việc cân bằng dữ liệu, replication đảm bảo dự phòng.

4.2. Điểm mạnh
Hiệu năng cao: Tìm kiếm trong mili giây, xử lý hàng triệu document.

Phân tán dữ liệu: Dữ liệu tự động phân tán và đồng bộ giữa các node.

Khả năng mở rộng: Thêm/bớt node dễ dàng, không ảnh hưởng tới hoạt động hệ thống.

Tính năng phong phú: Tìm kiếm full-text, phân tích nâng cao, gợi ý, lọc, phân nhóm dữ liệu.

REST API: Dễ dàng tích hợp với mọi ứng dụng web, mobile.

4.3. Điểm yếu
Quản trị phức tạp: Cần kiến thức để cấu hình, tối ưu cluster.

Tốn tài nguyên: RAM và CPU tiêu tốn khá nhiều, đặc biệt với chỉ mục lớn.

Không thay thế CSDL quan hệ: Không hỗ trợ các truy vấn JOIN phức tạp.

Khó đồng bộ dữ liệu 2 chiều: Cần thiết kế kỹ để đồng bộ dữ liệu với hệ thống nguồn (DB).
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