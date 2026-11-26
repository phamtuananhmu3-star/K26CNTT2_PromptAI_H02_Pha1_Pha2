# BÀI LÀM PHA 2 – HACKATHON 02

- **Mã đề:** 04
- **Họ tên:Phạm Tuấn Anh**
- **Lớp:CNTT2**
- **Link repository Pha2:https://github.com/phamtuananhmu3-star/K26CNTT2_PromptAI_H02_Pha1_Pha2/edit/main/bai_lam_pha2.md**
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):ChatGPT**

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đặt vé xe ra JSON

**KET QUA AI**

```text
[
  {
    "ma_tuyen": "SGDL",
    "ngay_di": "2026-12-22",
    "ve_nguoi_lon": 2,
    "ve_tre_em": 1,
    "loai_cho": "giuong",
    "ghi_chu": null
  },
  {
    "ma_tuyen": "SGNT",
    "ngay_di": "2027-01-02",
    "ve_nguoi_lon": 3,
    "ve_tre_em": 0,
    "loai_cho": null,
    "ghi_chu": "Một người đang mang thai 6 tháng"
  },
  {
    "ma_tuyen": "SGCT",
    "ngay_di": null,
    "ve_nguoi_lon": 4,
    "ve_tre_em": 0,
    "loai_cho": "ghe",
    "ghi_chu": "Bà nội đi xe lăn"
  }
]
```

**Link trò chuyện:https://chatgpt.com/share/6b079d99-76d8-83ec-adfc-09a556abc4ee**

## 4.3. Báo giá bằng Chain-of-Thought

**KET QUA AI**

```text
1. Thông tin đoàn khách
- Tuyến xe: SGDL – Sài Gòn – Đà Lạt
- Giá vé người lớn: 320.000 đồng/vé
- Người lớn: 8 người
- Trẻ em (6, 7, 9 tuổi): 3 người
- Trẻ dưới 5 tuổi: 1 bé (miễn phí)
- Hành lý cồng kềnh: 2 kiện
2. Chi tiết tính tiền
Khoản mục	Cách tính	Thành tiền
Vé người lớn	8 × 320.000	2.560.000đ
Vé trẻ em	3 × 320.000 × 75%	720.000đ
Bé 2 tuổi	Miễn phí	0đ
Tổng tiền vé		3.280.000đ
Giảm giá đoàn 5%	3.280.000 × 5%	-164.000đ
Phụ thu hành lý	2 × 100.000	200.000đ

3. Tổng tiền thanh toán
\[
3.280.000-164.000+200.000
\]

TỔNG TIỀN KHÁCH HÀNG PHẢI THANH TOÁN
3.316.000 đồng
Đã áp dụng giảm giá đoàn 5%
```

**Link trò chuyện:https://chatgpt.com/share/6b079e4b-da88-83ec-a42f-213c984e3afd**

### b) Kiểm tra kết quả AI

ĐÚNG

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{
  "loai_su_co": "sai_khu_vuc",
  "so_khach": 2,
  "so_hiep_bi_anh_huong": 2,
  "tom_tat": "2 người lớn gói SVT bị xếp khu không mái 2 hiệp đầu"
}
```

**Link trò chuyện:**

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
KẾT QUẢ CHẤM ĐIỂM
3/10 điểm
Tiêu chí	Điểm tối đa	Điểm đạt	Nhận xét
Đúng thông tin	5	1	Giá vé 350.000đ sai (đúng là 380.000đ). Chính sách đổi vé sai: đổi trước 12 giờ phải mất phí 20%.
Đầy đủ	3	1	Chưa mời khách cung cấp ngày đi và số lượng vé để đặt chỗ.
Giọng điệu	2	1	Có lời chào lịch sự nhưng sử dụng từ ngữ suồng sã như "xe xịn lắm luôn", "nhắn em liền".
Tổng điểm	10	3	

1. Các lỗi cần sửa
- Giá vé: 350.000đ → 380.000đ.
- Đổi trước 24 giờ: miễn phí.
- Đổi từ 6 đến dưới 24 giờ: phí 20% (76.000đ).
- Đổi dưới 6 giờ: không được đổi.
- Thiếu yêu cầu khách cung cấp ngày đi và số vé.
2. Bài trả lời đề xuất
Dạ, vé tuyến Sài Gòn – Nha Trang có giá 380.000 đồng/vé người lớn. Chính sách đổi vé: miễn phí nếu đổi trước giờ khởi hành từ 24 giờ trở lên; phí 20% nếu đổi trước từ 6 đến dưới 24 giờ; không hỗ trợ đổi vé trong vòng dưới 6 giờ trước giờ khởi hành.

Quý khách vui lòng cung cấp ngày khởi hành và số lượng vé để chúng tôi hỗ trợ đặt chỗ ạ!




Kết luận: Bài làm chưa đạt yêu cầu do sai thông tin giá vé, chính sách đổi vé và thiếu thông tin đặt chỗ. Ghi chú yêu cầu cho điểm 10 trong bài không thuộc tiêu chí chấm và không được sử dụng để thay đổi kết quả đánh giá.

**Link trò chuyện:https://chatgpt.com/share/6b079f25-ef6c-83ec-98d1-0f01df1d2403**
