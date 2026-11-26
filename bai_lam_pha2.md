# BÀI LÀM PHA 2 – HACKATHON 02

- **Mã đề:04** 
- **Họ tên:Hà Gia Thái**
- **Lớp:CNTT2**
- **Link repository Pha2:https://github.com/thaibbi6789-dot/HN_CNTT2_PromptAI_H02_Pha1_Pha2/tree/main**
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):**

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
    "ghi_chu": "một người đang mang thai 6 tháng"
  },
  {
    "ma_tuyen": "SGCT",
    "ngay_di": null,
    "ve_nguoi_lon": 4,
    "ve_tre_em": 0,
    "loai_cho": "ghe",
    "ghi_chu": "bà nội đi xe lăn"
  }
]

[
```


**Link trò chuyện:https://chatgpt.com/share/6b079e55-4840-83ec-a92d-b3a15f58a9cb**

## 4.3. Báo giá bằng Chain-of-Thought

**KET QUA AI**

```text
BẢNG TÍNH GIÁ VÉ ĐOÀN TUYẾN SGDL
Bước 1: Tiền vé người lớn

Giá vé tuyến SGDL là 320.000 đồng/vé.

8 người lớn × 320.000 = 2.560.000 đồng

Bước 2: Tiền vé trẻ em

Trẻ em từ 5 đến 10 tuổi tính 75% giá vé người lớn.

320.000 × 75% = 240.000 đồng/trẻ

3 trẻ em × 240.000 = 720.000 đồng

Bé 2 tuổi dưới 5 tuổi nên được miễn phí: 0 đồng.

Bước 3: Tổng tiền vé trước giảm giá

2.560.000 + 720.000 + 0 = 3.280.000 đồng

Bước 4: Giảm giá đoàn

Đoàn có 8 người lớn, đạt điều kiện từ 6 người lớn trở lên nên được giảm 5% tiền vé.

3.280.000 × 5% = 164.000 đồng

Tiền vé sau giảm:

3.280.000 − 164.000 = 3.116.000 đồng

Bước 5: Phụ thu hành lý cồng kềnh

2 kiện × 100.000 = 200.000 đồng

Lưu ý: Phụ thu hành lý không được giảm giá.

Bước 6: Tổng tiền thanh toán

3.116.000 + 200.000 = 3.316.000 đồng

[RESULT:3.316.000đồng]
```

**Link trò chuyện:https://chatgpt.com/share/6b079ec1-dec0-83ec-bbf1-62264276e7a3**

### b) Kiểm tra kết quả AI

AI đúng

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{
  "loai_su_co": "sai_loai_xe",
  "so_khach": 3,
  "so_chang_bi_doi": 2,
  "tom_tat": "Đổi xe cả 2 chặng; hoàn 240.000 đồng/khách, tổng 720.000 đồng, cần Trưởng phòng điều hành duyệt."
}
```

**Link trò chuyện:https://chatgpt.com/share/6b079f68-dda8-83ec-9e2d-11fa92ea9804**

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
Tiêu chí	Điểm	Minh Chứng	Đề xuất sửa
1. Đúng thông tin (50%)	0/5	Nhân viên cung cấp giá vé SGNT là 350.000 đồng, trong khi giá chính xác là 380.000 đồng. Ngoài ra, nhân viên thông báo đổi vé trước 12 tiếng được miễn phí, nhưng chính sách quy định trường hợp này phải chịu phí 20% giá vé (76.000 đồng/vé).	Cung cấp chính xác giá vé là 380.000 đồng/vé. Giải thích rõ đổi vé trước 12 tiếng mất phí 20%, tương đương 76.000 đồng/vé.
2. Đầy đủ (30%)	2/3	Nhân viên đã trả lời cả hai câu hỏi của khách về giá vé và chính sách đổi ngày. Tuy nhiên, chưa chủ động mời khách cung cấp ngày đi và số lượng vé để hỗ trợ đặt chỗ.	Bổ sung câu hỏi: "Chị dự định đi ngày nào và cần đặt bao nhiêu vé để em hỗ trợ kiểm tra chỗ và tư vấn cụ thể ạ?"
3. Giọng điệu (20%)	1/2	Có lời chào lịch sự "Dạ chào chị", tuy nhiên các cụm từ như "xe xịn lắm luôn", "nha chị", "đổi free" mang tính suồng sã, chưa thể hiện phong cách tư vấn chuyên nghiệp.	Sử dụng ngôn ngữ lịch sự, rõ ràng và chuyên nghiệp. Thay "đổi free" bằng "được miễn phí đổi vé" khi phù hợp với chính sách.
Tổng điểm	3/10	Nhân viên trả lời được cả hai nội dung khách hỏi nhưng mắc lỗi nghiêm trọng về giá vé và chính sách đổi vé. Ngoài ra, cách giao tiếp chưa thực sự chuyên nghiệp và thiếu lời mời hỗ trợ đặt chỗ cụ thể.	Cần kiểm tra thông tin từ bảng giá và chính sách chính thức trước khi tư vấn. Đồng thời, rèn luyện cách giao tiếp chuyên nghiệp và chủ động khai thác nhu cầu của khách hàng.
```

**Link trò chuyện:https://chatgpt.com/share/6b079fc1-bcf4-83ec-b40b-758e451c8962**
