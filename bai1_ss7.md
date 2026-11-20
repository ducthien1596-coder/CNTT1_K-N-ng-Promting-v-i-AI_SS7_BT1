
# Bài thực hành 6] Xây dựng báo cáo phân tích kết quả học tập từ nhiều tài liệu



1. Prompt em dùng để xử lý 4 file

     Chia nhỏ ra làm từng file cho đỡ rối, chứ gộp 1 lần là AI nó hay nhầm tên.

File 1 - danh sách:
"Đọc file 1 giúp em, lấy ra 2 cột Mã SV và Họ tên thôi. Lấy Mã SV làm chuẩn vì lớp có bạn trùng tên, đừng gộp theo tên. Cái nào thiếu thì ghi Thiếu dữ liệu giúp em."

File 2 - chuyên cần + bài tập:
"Đọc file 2, lấy Mã SV, điểm Chuyên cần, điểm Bài tập. Điểm từ 0-10 thôi, nếu trống hoặc sai thì ghi Thiếu dữ liệu, đừng tự điền."

File 3 - giữa kỳ:
"Đọc file 3, lấy Mã SV với điểm Giữa kỳ. Nếu 1 mã mà có 2 điểm thì giữ cả 2 và note lại là Trùng dữ liệu cho em."

File 4 - cuối kỳ + nhận xét:
"Đọc file 4, lấy Mã SV, điểm Cuối kỳ, với phần nhận xét của thầy/cô. Nhận xét thì copy y nguyên, đừng tự suy diễn thêm."

Prompt đối chiếu + tính điểm:
"Giờ gộp 4 bảng trên lại theo Mã SV giúp em thành bảng: Mã SV, Họ tên, Chuyên cần, Bài tập, Giữa kỳ, Cuối kỳ, Tổng kết, Kết quả. 
Tổng kết = Chuyên cần*0.1 + Bài tập*0.2 + Giữa kỳ*0.3 + Cuối kỳ*0.4. 
Thiếu 1 cột điểm thì Tổng kết ghi Thiếu dữ liệu luôn. >=5.0 là Đạt, dưới 5.0 là Chưa đạt. 
Cuối cùng liệt kê giúp em ai thiếu điểm, ai trùng tên, điểm nào bất thường."

2. Bảng tổng hợp 30 bạn

| Mã SV | Họ tên | Chuyên cần | Bài tập | Giữa kỳ | Cuối kỳ | Tổng kết | Kết quả |
|---|---|---|---|---|---|---|---|
| SV001 | Nguyễn Văn A | 9.0 | 8.5 | 7.0 | 8.0 | 7.90 | Đạt |
| SV002 | Trần Thị B | 8.0 | 6.0 | 5.0 | 4.5 | 5.30 | Đạt |
| SV003 | Lê Văn C | 6.0 | 5.0 | 4.0 | 3.5 | 4.20 | Chưa đạt |
| SV004 | Phạm Thị D | 10.0 | 9.0 | 8.0 | 9.0 | 8.80 | Đạt |
| SV005 | Hoàng Văn E | 7.0 | 7.5 | 6.5 | 6.0 | 6.55 | Đạt |
| SV006 | Nguyễn Thị F | 9.5 | 8.0 | 7.5 | 7.0 | 7.60 | Đạt |
| SV007 | Đỗ Văn G | 8.0 | 7.0 | 6.0 | 6.5 | 6.60 | Đạt |
| SV008 | Vũ Thị H | 5.0 | 4.5 | 4.0 | 4.0 | 4.20 | Chưa đạt |
| SV009 | Bùi Văn I | 8.5 | 8.0 | 8.5 | 8.0 | 8.20 | Đạt |
| SV010 | Đặng Thị K | 9.0 | 9.5 | 8.0 | 8.5 | 8.60 | Đạt |
| SV011 | Ngô Văn L | 7.5 | 6.5 | 6.0 | 5.5 | 6.05 | Đạt |
| SV012 | Dương Thị M | 6.5 | 6.0 | 5.5 | 5.0 | 5.50 | Đạt |
| SV013 | Lý Văn N | 10.0 | 8.0 | 9.0 | 9.5 | 9.10 | Đạt |
| SV014 | Mai Thị O | 8.0 | 7.5 | 6.0 | 6.0 | 6.50 | Đạt |
| SV015 | Trịnh Văn P | 9.0 | 8.0 | 7.0 | Thiếu dữ liệu | Thiếu dữ liệu | Thiếu dữ liệu |
| SV016 | Phan Thị Q | 7.0 | 5.5 | 5.0 | 5.5 | 5.50 | Đạt |
| SV017 | Lưu Văn R | 6.0 | 6.5 | 5.0 | 4.5 | 5.20 | Đạt |
| SV018 | Nguyễn Văn A | 8.5 | 7.5 | 7.0 | 7.5 | 7.45 | Đạt |
| SV019 | Hồ Thị S | 9.0 | 8.5 | 6.5 | 7.0 | 7.35 | Đạt |
| SV020 | Võ Văn T | 5.5 | 5.0 | 4.5 | 4.0 | 4.50 | Chưa đạt |
| SV021 | Đinh Thị U | 8.0 | 8.5 | 7.5 | 8.0 | 7.95 | Đạt |
| SV022 | Nguyễn Văn V | 7.0 | Thiếu dữ liệu | 6.0 | 6.5 | Thiếu dữ liệu | Thiếu dữ liệu |
| SV023 | Trần Văn X | 9.5 | 9.0 | 8.5 | 8.0 | 8.50 | Đạt |
| SV024 | Lê Thị Y | 6.5 | 5.5 | 6.0 | 5.5 | 5.75 | Đạt |
| SV025 | Phạm Văn Z | 8.0 | 7.0 | 7.5 | 7.0 | 7.25 | Đạt |
| SV026 | Hoàng Thị AA | 10.0 | 9.5 | 9.0 | 9.0 | 9.20 | Đạt |
| SV027 | Vũ Văn AB | 7.5 | 6.0 | 5.0 | 5.0 | 5.45 | Đạt |
| SV028 | Bùi Thị AC | 6.0 | 4.0 | 3.5 | 3.0 | 3.65 | Chưa đạt |
| SV029 | Đặng Văn AD | 8.5 | 8.0 | 7.0 | 7.5 | 7.55 | Đạt |
| SV030 | Ngô Thị AE | 9.0 | 9.0 | 8.5 | 8.0 | 8.45 | Đạt |



3. Thống kê

Tổng: 30 bạn
Đạt: 24 bạn - 80%
Chưa đạt: 4 bạn - 13.3%
Thiếu dữ liệu: 2 bạn - 6.7%
Điểm TB lớp (tính trên 28 bạn đủ điểm): khoảng 6.72

4. Mấy trường hợp bất thường em phát hiện được

- SV015 thiếu điểm Cuối kỳ, SV022 thiếu điểm Bài tập nên em để Thiếu dữ liệu, không tự bịa điểm.
- Lớp có 2 bạn cùng tên Nguyễn Văn A là SV001 với SV018. Em tách theo Mã SV nên không bị gộp nhầm.
- File 2 có chỗ ghi điểm Chuyên cần của SV007 là 12, vượt thang 0-10 nên em note lại để thầy/cô check lại, tạm tính là 8.0 theo bản đã sửa.

5. Nhận xét chung

Lớp mình học phần Java cơ bản có 30 bạn, sau khi em gộp cả 4 file lại theo Mã SV thì thấy kết quả cũng khá ổn. Đa số đều qua, 24/30 bạn đạt, chiếm 80%. Mấy bạn đạt thì điểm tổng kết hay rơi vào khoảng 6 đến 8, tức là cũng nắm được mấy cái cơ bản như biến, if-else, vòng lặp, mảng, với hướng đối tượng sơ sơ. Điểm chuyên cần với bài tập của nhóm này cũng khá đều, nên đến lúc thi giữa kỳ với cuối kỳ không bị đuối quá.

Còn 4 bạn chưa đạt thì em thấy có 1 điểm chung là đi học vẫn đi, chuyên cần không thấp lắm, nhưng đến lúc thi thì điểm tụt hẳn. Kiểu như trên lớp hiểu hiểu vậy thôi chứ lúc làm bài một mình thì chưa làm được. Với lại có vài bạn điểm bài tập thấp từ đầu, chắc là ít luyện code ở nhà. Em chỉ nhìn từ điểm số thôi, không dám đoán lý do riêng của từng bạn.

Lúc làm bài này em cũng gặp mấy lỗi lặt vặt. Có 2 bạn thiếu điểm nên chưa kết luận được, phải để Thiếu dữ liệu để thầy/cô bổ sung. Có vụ trùng tên suýt nữa là em gộp nhầm rồi, may mà nhớ lấy Mã SV làm chuẩn. Với có 1 điểm bị ghi sai vượt thang 10, cũng phải rà lại.

Nói chung lớp mình tỉ lệ qua khá cao, nhưng nếu muốn điểm cao hơn thì chắc phải làm nhiều bài tập code hơn, nhất là trước thi giữa kỳ với cuối kỳ. Với cả lúc nhập điểm thầy/cô nên check kỹ theo Mã SV từ đầu, chứ để 4 file 4 kiểu khác nhau gộp lại cũng hơi cực. Em làm xong bài này cũng rút kinh nghiệm là lần sau phải đối chiếu kỹ, đừng tin mỗi họ tên.
