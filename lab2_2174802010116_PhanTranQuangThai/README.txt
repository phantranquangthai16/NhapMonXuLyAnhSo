
CÂU 6
apply_denoise_filters(image): Hàm này áp dụng ba bộ lọc giảm nhiễu khác nhau cho ảnh:
Gaussian Filter: Làm mịn ảnh bằng cách sử dụng bộ lọc Gaussian, giúp làm mờ nhiễu ngẫu nhiên trong ảnh.
Median Filter: Thực hiện bộ lọc trung vị, thay thế mỗi pixel với giá trị trung vị trong vùng lân cận. Bộ lọc này rất hiệu quả trong việc giảm nhiễu muối và tiêu.
Bilateral Filter: Giữ lại các biên của ảnh trong khi giảm nhiễu, giúp ảnh giữ được sự sắc nét nhưng vẫn loại bỏ nhiễu.
Các kết quả của bộ lọc được lưu lại với tên file theo định dạng tên_ảnh_gốc_tên_filter.jpg.

CÂU 7
Mã này sử dụng thuật toán Canny Edge Detection để tìm các cạnh trong ảnh:
Median Filter: Đầu tiên áp dụng bộ lọc trung vị để làm mịn ảnh.
Chuyển ảnh sang grayscale: Ảnh sau khi làm mịn được chuyển thành ảnh đơn kênh (ảnh xám).
Canny Edge Detection: Tìm các cạnh trong ảnh grayscale với ngưỡng thấp là 100 và ngưỡng cao là 200.
Kết quả (ảnh cạnh) được lưu lại với tên tên_ảnh_gốc_edges.jpg.


CÂU 8
Ở đây, bạn thay đổi màu sắc của ảnh bằng cách áp dụng một tỷ lệ ngẫu nhiên cho mỗi kênh màu (Red, Green, Blue):
rand_color = np.random.randint(0, 256, size=3): Tạo một mảng ngẫu nhiên với ba giá trị từ 0 đến 255, mỗi giá trị đại diện cho tỷ lệ màu của các kênh RGB.
Thay đổi các kênh màu: Mỗi kênh màu của ảnh được nhân với tỷ lệ ngẫu nhiên tương ứng.
Kết quả là ảnh mới có màu sắc thay đổi ngẫu nhiên và được lưu với tên tên_ảnh_gốc_randomRGB.jpg


CÂU 9
Trong đoạn mã này, bạn thay đổi giá trị kênh Hue (màu sắc) của ảnh trong không gian màu HSV:
random.randint(0, 179): Tạo một giá trị ngẫu nhiên cho kênh Hue trong phạm vi từ 0 đến 179 (kênh Hue trong không gian HSV có giá trị này).
while h in used_hues: Đảm bảo rằng giá trị Hue ngẫu nhiên chưa được sử dụng trước đó (tránh việc trùng lặp màu sắc).
Sau khi thay đổi kênh Hue, ảnh được chuyển lại về không gian màu BGR và lưu với tên tên_ảnh_gốc_randomHSV.jpg.
Mỗi lần thực hiện, ảnh sẽ có một màu sắc khác biệt do kênh Hue được thay đổi ngẫu nhiên.










