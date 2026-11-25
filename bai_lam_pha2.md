# BÀI LÀM PHA 2 (ĐỀ LUYỆN TẬP CHỦ ĐỀ CHẠY AFFILIATE)

- **Họ tên:** PHẠM NGỌC DUY
- **Lớp:** CNTT3
- **Link repository Pha2:** https://github.com/Phamduy2206/HN-KS26-CNTT3_PromptAI_H04.git
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):** Gemini

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đăng ký gói Affiliate ra JSON

**KET QUA AI**

```text
[
  {
    "ma_goi": "TT",
    "ngay_bat_dau": "2026-12-20",
    "creator_chinh": 2,
    "thuc_tap_sinh": 1,
    "hang_tai_khoan": "thuong",
    "ghi_chu": null
  },
  {
    "ma_goi": "SP",
    "ngay_bat_dau": "2027-01-08",
    "creator_chinh": 3,
    "thuc_tap_sinh": 0,
    "hang_tai_khoan": "thuong",
    "ghi_chu": "bó bột chân cần ngồi bàn gần cửa ra vào"
  },
  {
    "ma_goi": "PRO",
    "ngay_bat_dau": null,
    "creator_chinh": 4,
    "thuc_tap_sinh": 0,
    "hang_tai_khoan": "vip",
    "ghi_chu": "cần mượn thêm đèn trợ sáng và phông xanh để quay mẫu"
  }
]
```

**Link trò chuyện:** https://share.gemini.google/3qkwuyaqf72l

## 4.3. Báo giá gói Affiliate bằng Chain-of-Thought

**KET QUA AI**

```text
1. **Tiền Creator chính:**
* Gói TT (TikTok Affiliate) có đơn giá 1.500.000 đồng/Creator chính. Team có 4 Creator chính.
* Phép tính: $4 \times 1.500.000 = 6.000.000$ đồng.


2. **Tiền thực tập sinh:**
* Team có 2 thực tập sinh (16 tuổi và 17 tuổi, thuộc độ tuổi từ 15 đến dưới 18 tuổi) được tính 60% giá Creator chính. Bé 7 tuổi (dưới 15 tuổi, ngồi khu chờ) được miễn phí (0 đồng).
* Phép tính: $2 \times (1.500.000 \times 60\%) + 0 = 2 \times 900.000 = 1.800.000$ đồng.


3. **Tổng tiền gói:**
* Tổng tiền gói bằng tiền Creator chính cộng tiền thực tập sinh.
* Phép tính: $6.000.000 + 1.800.000 = 7.800.000$ đồng.


4. **Giảm giá team:**
* Team có 4 Creator chính (đạt điều kiện từ 4 Creator chính trở lên) nên được giảm 10% trên tổng tiền gói.
* Phép tính: $7.800.000 \times 10\% = 780.000$ đồng.


5. **Phụ thu thuê mic:**
* Team thuê 2 bộ mic thu âm không dây với giá 250.000 đồng/bộ (không áp dụng giảm giá).
* Phép tính: $2 \times 250.000 = 500.000$ đồng.


6. **Tổng tiền:**
* Tổng tiền thanh toán bằng tiền gói sau giảm giá cộng phụ thu.
* Phép tính: $(7.800.000 - 780.000) + 500.000 = 7.020.000 + 500.000 = 7.520.000$ đồng.



[RESULT: 7.520.000 đồng]
```

**Link trò chuyện:** https://share.gemini.google/Pe0cngvLVDpe

### b) Kiểm tra kết quả AI

- Câu trẩ lời của AI là đúng . 

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{
  "loai_su_co": "sai_phong",
  "so_khach": 3,
  "so_ca_bi_anh_huong": 2,
  "tom_tat": "Khách nhóm 3 người bị xếp sai phòng thiếu đèn livestream và cách âm trong 2 ca thực hành đầu."
}
```

**Link trò chuyện:** https://share.gemini.google/oQ7JL8GyWUlh

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
| Tiêu chí | Điểm | Minh chứng | Đề xuất sửa |
| --- | --- | --- | --- |
| **Đúng thông tin (50%)** | 0/5 | **1. Lỗi sai giá gói:**<br>

<br>- *Câu bị lỗi:* "Gói TikTok Affiliate bên mình giá chỉ 1.200.000đ/người thôi"<br>

<br>- *Lý do sai:* Báo sai giá chuẩn của trung tâm (1.500.000 đồng/Creator chính).<br>

<br>

<br>**2. Lỗi sai chính sách hoàn tiền:**<br>

<br>- *Câu bị lỗi:* "Bạn báo huỷ trước 5 ngày thì được hoàn lại đủ 100% tiền nha"<br>

<br>- *Lý do sai:* Báo sai mức hoàn tiền. Theo quy định, huỷ trước ngày bắt đầu từ 3 đến 6 ngày chỉ được hoàn 50% (chỉ hoàn 100% nếu báo trước từ 7 ngày trở lên). | "Hiện tại, gói TikTok Affiliate (TT) bên mình có mức phí là **1.500.000 đồng/Creator chính**.<br>

<br>

<br>Về chính sách huỷ đăng ký, nếu bạn báo huỷ trước ngày bắt đầu 5 ngày (nằm trong khung từ 3 đến 6 ngày) thì trung tâm sẽ **hoàn lại 50% học phí** (bạn sẽ mất 50% phí giữ suất). Trung tâm chỉ hoàn 100% khi bạn báo huỷ trước ngày bắt đầu từ 7 ngày trở lên ạ." |
| **Đầy đủ (30%)** | 2/3 | **1. Lỗi thiếu thông tin điều hướng (CTA):**<br>

<br>- *Câu bị lỗi:* Toàn bộ bài trả lời (thiếu lời mời cung cấp thông tin).<br>

<br>- *Lý do sai:* Đã trả lời được 2 câu hỏi của khách hàng (dù nội dung sai), nhưng thiếu phần mời khách hàng cung cấp ngày đợt thực chiến và số lượng suất muốn đăng ký. | Bổ sung vào cuối câu trả lời:<br>

<br>"Để bên mình hỗ trợ giữ suất và tư vấn chi tiết hơn, bạn vui lòng cho mình xin thông tin về **ngày đợt thực chiến** bạn dự định tham gia và **số lượng suất** muốn đăng ký nhé!" |
| **Giọng điệu (20%)** | 0/2 | **1. Lỗi dùng từ ngữ suồng sã:**<br>

<br>- *Câu bị lỗi:* "Dạ hello bạn nha!", "...thôi...", "...nha, cứ chốt lẹ kẻo hết slot nè!"<br>

<br>- *Lý do sai:* Sử dụng ngôn ngữ thiếu trang trọng, mang tính chất giục giã, suồng sã ("hello", "nha", "chốt lẹ", "nè"), không phù hợp với tiêu chuẩn chuyên nghiệp của trung tâm.<br>

<br>

<br>**2. Lỗi cam kết doanh thu/hoa hồng ảo:**<br>

<br>- *Câu bị lỗi:* "đăng ký xong gắn link là nổ đơn hoa hồng trăm triệu luôn ạ."<br>

<br>- *Lý do sai:* Đưa ra cam kết thu nhập/hoa hồng phi thực tế, gây hiểu lầm và vi phạm quy chuẩn tư vấn. | "Chào bạn, cảm ơn bạn đã quan tâm đến khoá học tại VietAffiliate.<br>

<br>

<br>...Khoá học sẽ trang bị cho bạn kiến thức và quy trình thực chiến để tối ưu hoá hiệu quả làm TikTok Affiliate. Nếu bạn cần hỗ trợ thêm thông tin gì trước khi đăng ký, bạn cứ nhắn cho mình nhé!" |
| **Tổng điểm** | **2/10** |  |  |
```

**Link trò chuyện:** https://share.gemini.google/26ESlHeU1ng7
