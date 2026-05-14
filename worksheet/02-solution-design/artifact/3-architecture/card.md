---
title: Artifact 3 — Kiến trúc (Architecture)
section: Bài 2 — Thiết kế giải pháp
---

# Card: Kiến trúc Tách lớp và Kiểm soát (Human-in-the-loop)

## 1. Vấn đề giải quyết
Sự phụ thuộc hoàn toàn vào một luồng xử lý duy nhất của AI dễ dẫn đến sai sót mang tính hệ thống.

## 2. Ý tưởng giải pháp
Sử dụng kiến trúc **Multi-Agent** hoặc **Tách lớp xử lý (De-coupled processing)** để kiểm chéo kết quả.

## 3. Các thành phần chính
- **Skill Scorer Agent**: Chỉ đọc phần kinh nghiệm/kỹ năng để chấm điểm (đã ẩn phần thời gian/tên tuổi).
- **Context Analyzer Agent**: Nhận diện các sự kiện đặc biệt (gap year) và đưa ra giải thích thay vì trừ điểm.
- **Fairness Gate**: Một module rule-based để so sánh kết quả của 2 Agent trên, nếu có sự chênh lệch lớn (do gap year), hệ thống sẽ gắn cờ "Manual Review required".

## 4. Hành vi hệ thống thay đổi
Thay vì một kết quả duy nhất, hệ thống tạo ra một quy trình kiểm duyệt nội bộ trước khi hiển thị cho recruiter, đảm bảo tính khách quan tối đa.
