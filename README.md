# Phân Tích Hiệu Suất Bán Hàng Online của Contoso (2007 - 2009)

## Mục lục

- [Tổng quan dự án](#tổng-quan-dự-án)
- [Mục tiêu](#mục-tiêu)
- [Dữ liệu](#dữ-liệu)
- [Phân tích dữ liệu](#phân-tích-dữ-liệu)
- [Insights](#insights)
- [Kết luận và Đề xuất](#kết-luận-và-đề-xuất)
- [Tài liệu tham khảo](#tài-liệu-tham-khảo)

### Tổng quan dự án

Contoso là một tập đoàn bán lẻ đa quốc gia có trụ sở tại Paris (Pháp) với danh mục sản phẩm hơn 100 nghìn loại khác nhau. Việc phân tích dữ liệu sẽ tập trung vào các chỉ số về bán hàng online như lợi nhuận, doanh thu, và các chỉ số liên quan đến sản phẩm. Từ đó, dự án đề xuất giải pháp cho sales manager để cải thiện chiến lược bán hàng và tối ưu hóa doanh thu cho Contoso.

### Mục tiêu

- Phân tích doanh thu, doanh số bán hàng online theo thời gian (2007-2009)
- Xác định những mặt hàng bán chạy và danh mục sản phẩm đóng góp lớn đến doanh thu

### Dữ liệu

Dự án sử dụng database được cung cấp bởi Microsoft, tham khảo tại [đây](https://www.microsoft.com/en-us/download/details.aspx?id=18279). Vì bộ dữ liệu này bao gồm thông tin từ nhiều phòng ban trong doanh nghiệp như C-level, Sales/Marketing, IT, Finance... nên dự án sẽ chỉ tập trung vào các bảng sau:

- **FactOnlineSales**: lưu dữ liệu bán hàng về doanh thu, doanh số, chi phí, lượng hàng trả về và giá trị mặt hàng giảm giá cho mỗi giao dịch online
- **DimDate**: mô tả thời gian diễn ra giao dịch theo năm, quý, tháng, tuần và ngày
- **DimProduct**: thông tin về sản phẩm như nhà sản xuất, thương hiệu, đặc điểm bên ngoài và chi phí, giá bán cho mỗi sản phẩm
- **DimProductCategory**: mô tả tên và key cho từng danh mục sản phẩm bao gồm: Audio, Computers, Cellphones...)
- **DimProductSubCategory**: Phân loại sản phẩm con (được chia nhỏ hơn so với danh mục sản phẩm) bao gồm: Televisions, VCD&DVD, Accessories...
- **DimPromotion**: chi tiết về từng loại giảm giá và mức giảm giá
- **DimGeography**: thông tin địa lý theo từng quốc gia, từng vùng gắn với nơi khách hàng sinh sống

Database diagram được mô tả như hình dưới đây:
![](https://github.com/Toridotoji/Project-1/blob/main/database%20diagram.png?raw=true)

### Phân tích dữ liệu
Xem thêm tại file [Phương pháp phân tích dữ liệu](https://github.com/Toridotoji/Project-1/blob/bb46d5e1fc9250ce68c0dcb509ce43bd0805d4a6/ph%C6%B0%C6%A1ng%20ph%C3%A1p%20ph%C3%A2n%20t%C3%ADch%20d%E1%BB%AF%20li%E1%BB%87u.md)

### Insights

## Tình hình kinh doanh
Năm 2009, doanh thu và lợi nhuận ròng Contoso đạt được lần lượt là 857,73 triệu đô và 437,91 triệu đô. Từ quý 3/2008, doanh thu và lợi nhuận giảm mạnh và bắt đầu hồi phục vào quý 1/2009. Tuy nhiên, tình hình kinh doanh nhìn chung năm 2009 của Contoso không ổn định và không có dấu hiệu tích cực.

![{8098E5FE-E2F8-472D-8700-CD092D98418B}](https://github.com/user-attachments/assets/1dc7d28d-0c14-4766-9afd-63d21da5dfdb)

Số liệu năm 2009 cho thấy 5 quốc gia đóng góp phần lớn doanh thu cho Contoso là Mỹ, Anh, Nhật, Úc và Trung Quốc. Mặc dù Nhật và Trung Quốc - 2 nước ở khu vực châu Á có mức độ đóng góp rất nhỏ vào năm 2007 và 2008 nhưng lại tăng trưởng doanh thu mạnh mẽ vào năm 2009. Trái ngược lại là Úc có sự suy giảm rõ rệt và giảm nhẹ ở Anh vào năm 2009 so với năm trước đó.

![{9D3C5F3B-6F94-4A1D-BD14-114E0F87363A}](https://github.com/user-attachments/assets/2a857f71-399e-4c0d-be4e-4495ffed1351)

![{7587AE31-8499-4A7B-B8E0-444E73ACFB2A}](https://github.com/user-attachments/assets/ef19312f-6d1e-4115-bdb7-37ce0cb497e3)

Doanh thu vào mùa giảm giá đóng góp lớn đến tổng doanh thu cả năm, trong đó mức giảm giá 10% và 20% kích thích doanh thu mạnh mẽ.

![{E6C6E53A-FC6F-4713-9816-0B26AAB19858}](https://github.com/user-attachments/assets/677fe477-1d6a-48ba-87ae-5894e3452cb1)

**Phân chia doanh thu theo mùa kinh doanh** tại các khu vực là châu Âu, Bắc Mỹ và châu Á cho thấy: tại châu Âu, doanh thu tháng vào mùa Back to School đều cao hơn so với các mùa khác nhưng vì chỉ diễn ra trong 2 tháng nên đóng góp tổng doanh thu cả năm chủ yếu đến từ mùa Holiday (diễn ra trong 4 tháng).

![{FE8EDC21-72D4-4DD4-A3C2-DB906474B06C}](https://github.com/user-attachments/assets/6caf4a38-d287-4265-beaa-0a2120108079)


Bắc Mỹ có xu hướng ngược lại khi tổng doanh thu trong mùa Back to School chiếm ưu thế với 27,41%, trong đó tổng doanh thu Holiday xếp thấp nhất.

![{4CF0E31A-8219-4BC0-9987-8F8ED15CC7D2}](https://github.com/user-attachments/assets/49a51c4e-5926-4bc4-a793-a8c3dbe8c595)

Tại khu vực châu Á, thời gian không diễn ra mùa kinh doanh chiếm đến 5 tháng, do đó có sự chênh lệch khá lớn về sự đóng góp doanh thu với mùa Holiday. Mức đóng góp của các mùa có sự tỉ lệ thuận với khoảng thời gian diễn ra, khi mùa Holiday và Spring/Back to School đều diễn ra trong 3 tháng có mức tỷ trọng lần lượt là 22,5% và 22,22%.

![{B318F8DD-58D2-4FB1-BB5E-0982475DF2C0}](https://github.com/user-attachments/assets/44dd46a5-bf2b-4294-882a-9ee189294f01)

Điểm chung của 3 khu vực trên là doanh thu đều tăng vào các tháng giữa năm, từ tháng 5 đến tháng 7.


## Sản phẩm

Sản phẩm bán chạy nhất trong 2 năm liên tiếp (2008 - 2009) là Tủ lạnh LitWare 24.7CuFt X980 (màu nâu) với doanh thu lần lượt 4 triệu đô và 3,12 triệu đô.

Năm 2009, danh mục các sản phẩm về thiết bị gia dụng chiếm đến 30,68% doanh thu cả năm, tiếp đến là các mặt hàng về máy ảnh, máy ghi hình (22,15%), máy tính (22,14%), TV (15,17%) và các danh mục còn lại chiếm tỷ trọng dưới 10%.

![{67C8293D-A241-4BAB-81B6-6598D8B8F176}](https://github.com/user-attachments/assets/2dbb0ec1-c927-4676-8565-1e699026a149)

Trong các danh mục con đóng góp đến 80% tổng doanh thu năm 2009 thì có gần một nửa (7/16) là thuộc về danh mục sản phẩm Thiết bị gia dụng.

![{A1074CB3-0468-4BFF-8B89-485D6EA2AF3D}](https://github.com/user-attachments/assets/83ba22d2-8ee8-483d-9d62-0ff3f42c7122)

### Kết luận và Đề xuất

- Áp dụng các chiến lược khác nhau cho từng khu vực: thúc đẩy các hoạt động marketing nhằm tăng doanh thu vào mùa Holiday tại châu Âu, Back to School tại Bắc Mỹ và mùa Holiday, Spring/Back to School tại châu Á.
- Áp dụng các mức ưu đãi 10% và 20% trong các hoạt động xúc tiến bán để tăng doanh thu.
- Danh mục sản phẩm Thiết bị gia dụng chiếm tỷ trọng doanh thu lớn nên được coi là danh mục chiến lược của Contoso. Do đó, cần đẩy mạnh doanh số các mặt hàng trong danh mục này nhằm tăng doanh thu và lợi nhuận.
