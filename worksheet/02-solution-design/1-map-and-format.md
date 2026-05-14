---
title: 01 — Thiết kế 3 lớp giải pháp
section: Bài 2 — Thiết kế giải pháp
format: Nhóm
time: 60 phút
---

# 1-map-and-format.md — Chiến lược giải pháp 3 lớp

## 1. Rủi ro trọng tâm (Chosen Risk)

Nhóm chọn rủi ro: **Bias / Fairness - AI hạ điểm ứng viên có gap year thai sản/gia đình.**
- **Vì sao chọn**: Đây là rủi ro có tác động lớn nhất đến quyền lợi con người, dễ xảy ra do dữ liệu huấn luyện thiên kiến, và có thể gây rủi ro pháp lý/thương hiệu cực lớn cho doanh nghiệp.

---

## 2. Phân tích nguyên nhân gốc (Root Cause)

| Tầng | Nguyên nhân có thể |
|---|---|
| **Dữ liệu (Data)** | Dữ liệu lịch sử tuyển dụng thường ưu tiên những người có sự nghiệp liên tục (lineary career path). |
| **Mô hình (Model)** | AI học được mối tương quan sai lệch: "gap year = hụt kiến thức = rủi ro cam kết". |
| **Quy trình (Workflow)** | Thiết kế "one-click shortlist" khiến recruiter không có cơ hội xem xét lý do gap year. |
| **Giao diện (UI)** | Điểm số (ranking score) hiện ra quá nổi bật mà không có giải thích (lack of explainability). |

---

## 3. Thiết kế giải pháp 3 lớp (3-Layer Design)

Chúng tôi sẽ xây dựng giải pháp đồng bộ trên cả 3 tầng để giảm thiểu rủi ro này.

| Lớp giải pháp | Mục tiêu | Artifact liên quan |
|---|---|---|
| **1. Giao diện (UI/UX)** | Hiển thị cảnh báo "Gap Year detected" kèm nút "Xem lý do" và nhắc nhở "Đừng chỉ nhìn vào điểm số". | `artifact/1-uiux/` |
| **2. Chỉ dẫn AI (Prompt)** | Buộc AI phải đánh giá gap year là thông tin trung tính và ưu tiên năng lực chuyên môn. | `artifact/2-prompt/` |
| **3. Kiến trúc (Architecture)** | Tách biệt phần chấm điểm kỹ năng và phần phân tích gap year; thêm bước "Human-check" bắt buộc cho CV có gap year. | `artifact/3-architecture/` |

---

## 4. Kế hoạch Demo

| Lớp | Loại Artifact | File Demo |
|---|---|---|
| Giao diện | UI Mockup / Card | `artifact/1-uiux/demo.md` |
| Chỉ dẫn AI | System Prompt + Examples | `artifact/2-prompt/demo.md` |
| Kiến trúc | Workflow Diagram / Logic | `artifact/3-architecture/demo.md` |

---

## 5. Tự phản biện (Self-critique)

1. **Nếu Prompt layer bị "vượt rào" (jailbreak), lớp nào sẽ chặn?**
   - Lớp UI sẽ luôn hiển thị cảnh báo cho recruiter rằng ứng viên này có gap year và cần được xem xét thủ công, bất kể AI chấm điểm cao hay thấp.
2. **Nếu UI làm người dùng thấy phiền, họ có tắt đi không?**
   - Chúng tôi thiết kế cảnh báo tinh tế, tích hợp vào tooltip hoặc icon nhỏ bên cạnh điểm số để không gây gián đoạn nhưng vẫn đảm bảo tính hiển thị.
3. **Kiến trúc dữ liệu có làm hệ thống chậm đi không?**
   - Việc tách lớp xử lý có thể tăng độ trễ khoảng 1-2 giây, nhưng đổi lại là tính minh bạch và công bằng, điều này là xứng đáng trong bài toán tuyển dụng.
