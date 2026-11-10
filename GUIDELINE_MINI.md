# Mini guideline — bài làm cá nhân

## Định nghĩa lớp

| Lớp | Định nghĩa của bạn | Ví dụ/điểm phân biệt |
| --- | --- | --- |
| `car` | Xe con chở người cỡ nhỏ | Sedan, SUV, taxi, xe bán tải; thân thấp, có cốp hoặc thùng hở phía sau |
| `truck` | Xe tải chở hàng, xe đầu kéo,Xe cứu hộ | Cabin tách riêng với thùng hàng, thùng cao hoặc sàn tải phía sau |
| `bus` | Xe buýt, minibus chở khách | Thân dài, nhiều cửa sổ dọc hông xe, cỡ lớn |
| `van` | Xe van/minivan chở hàng hoặc chở người | Thân liền khối, mui cao, đuôi vuông dựng đứng, không tách cabin |

## Quy tắc chung

- Box bám sát vật thể nghĩa là: mỗi xe một box riêng, cạnh box chạm sát điểm ngoài cùng của phần thân xe nhìn thấy, không lấy thêm mặt đường hay xe bên cạnh.
- Vật thể bị che khuất: vẫn gán box quanh phần nhìn thấy được nếu nhận ra được lớp; hai xe chồng nhau thì vẽ hai box riêng.
- Vật thể bị cắt bởi rìa ảnh: box chạm đúng rìa ảnh, không đoán phần nằm ngoài ảnh.
- Vật thể rất nhỏ/mơ hồ: nếu còn nhận ra được lớp thì gán; nếu chỉ còn mảnh nhỏ không xác định được thì không gán. Không gán xe máy, xe đạp, người đi bộ, biển báo.

## Ghi lại quyết định cho ít nhất ba ca mơ hồ

| Ảnh | Tình huống | Quyết định cuối | Lý do theo schema |
| --- | --- | --- | --- |
| `drive_018` | xe màu đen đi sau taxi đi ở cuối | `van`  |  xe có thân hộp cao, mui phẳng, đuôi đứng và không có cốp tách riêng như sedan nhưng thuộc van|
| `drive_019` | Xe cứu hộ kéo của công an: cabin nhỏ phía trước, sàn kéo và cần cẩu phía sau | `truck` | Vì thùng đằng sau giống thùng xe tải dạng nhỏ |
| `drive_026` | xe trắng có sọc xanh dương ở thân, nhìn từ trên cao chếch phía sau, nằm giữa giao lộ .Xe có dáng hộp cao, mui phẳng và có thiết bị hoặc đèn trên nóc, giống xe tuần tra, xe dịch vụ hoặc xe cứu hộ. Khó chắc là van hay truck.| `truck` | Xe có dáng cabin và sàn tải phía sau , và là xe chuyên dụng cứu hộ chứ không phải xe chở người. Theo schema, xe tải, xe cứu hộ và xe chuyên dụng xếp vào truck. |