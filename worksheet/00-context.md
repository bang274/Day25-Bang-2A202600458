---
title: 00 — Bối cảnh sản phẩm của nhóm
section: Day 25 — dùng lại cho mọi cuộc trò chuyện với AI
format: Nhóm
time: Điền 5 phút đầu buổi
---

# 00-context.md — Bối cảnh sản phẩm của nhóm

## 1. Sản phẩm

- **Tên sản phẩm / bot**: Recruitment AI Assistant (ATS-integrated)
- **Sản phẩm giúp ai làm gì**: Giúp chuyên viên tuyển dụng (recruiter) tóm tắt hồ sơ ứng viên (CV), so sánh kỹ năng ứng viên với mô tả công việc (JD), và đề xuất danh sách rút gọn (shortlist) tiềm năng.
- **Người dùng gặp sản phẩm ở đâu**: Tích hợp trực tiếp bên trong hệ thống quản lý tuyển dụng (Applicant Tracking System - ATS) của doanh nghiệp.
- **Giai đoạn hiện tại**: Chuẩn bị ra mắt (Pre-launch testing).

---

## 2. Phạm vi

**AI được làm gì**

- Tóm tắt kinh nghiệm làm việc, học vấn và kỹ năng từ CV.
- So sánh các tiêu chí trong CV với yêu cầu trong JD.
- Xếp hạng sơ bộ mức độ phù hợp của ứng viên.
- Gợi ý câu hỏi phỏng vấn dựa trên các khoảng trống kiến thức hoặc kỹ năng trong hồ sơ.

**AI không được làm gì**

- Tự động gửi email từ chối hoặc chấp nhận ứng viên mà không có sự phê duyệt của con người.
- Lưu trữ thông tin cá nhân (PII) vào dữ liệu huấn luyện công khai.
- Đưa ra các nhận xét mang tính định kiến về giới tính, tuổi tác, vùng miền hoặc tình trạng gia đình.

**Vì sao có giới hạn này**

Để đảm bảo tính công bằng trong tuyển dụng, tuân thủ các quy định về bảo mật dữ liệu (PDPL) và tránh rủi ro pháp lý về phân biệt đối xử. Quyết định cuối cùng luôn phải thuộc về con người (Human-in-the-loop).

---

## 3. Người dùng

- **Là ai**: Recruiter hoặc Hiring Manager, từ 22-45 tuổi, quen thuộc với các công cụ quản lý văn phòng, đang chịu áp lực sàng lọc hàng trăm hồ sơ mỗi ngày.
- **Họ hỏi AI khi nào**: Khi cần sàng lọc nhanh một lượng lớn hồ sơ mới đổ về hoặc khi cần so sánh nhanh 2-3 ứng viên cuối cùng.
- **Họ cần quyết định gì sau khi hỏi AI**: Có nên đưa ứng viên này vào vòng phỏng vấn tiếp theo hay không.
- **Khi nào họ dễ bị tổn thương / dễ hiểu sai**: Khi họ quá tin vào điểm số (ranking score) mà AI đưa ra mà không xem xét các yếu tố bối cảnh (như gap year hợp lý).
- **Họ thường tin AI đến mức nào**: Có xu hướng tin tưởng cao (over-reliance) vì áp lực thời gian, cần được cảnh báo để kiểm tra lại các nguồn dữ liệu gốc (CV gốc).

---

## 4. Bối cảnh ngành

- **Sự cố tương tự đã từng xảy ra**: Amazon từng phải hủy bỏ công cụ tuyển dụng AI vì nó tự học cách phân biệt đối xử với phụ nữ dựa trên dữ liệu lịch sử.
- **Quy định hoặc ràng buộc liên quan**: Luật lao động Việt Nam cấm phân biệt đối xử trong tuyển dụng; Nghị định bảo vệ dữ liệu cá nhân (PDPL).
- **Nguồn chính thức nên ưu tiên**: CV gốc của ứng viên, Job Description đã được phê duyệt, tiêu chuẩn kỹ năng của ngành.

---

## 5. Ghi chú thêm

Trọng tâm của nhóm là giải quyết rủi ro **Bias/Fairness** liên quan đến việc AI hạ điểm ứng viên có gap year (nghỉ thai sản/chăm sóc gia đình), đảm bảo công cụ hỗ trợ đa dạng và công bằng.
