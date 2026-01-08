# ISO 9001 – Hệ thống Quản lý Chất lượng (QMS)

---
**Author:** Vox  
**Version:** 1.0.0  
**Created At:** 2026-01-08
---

## Document Control

| Version | Date       | Author | Description |
|--------|------------|--------|-------------|
| 1.0.0  | 2026-01-08 | Vox    | Initial creation |

---

## 1. Mục đích (Purpose)
ISO 9001 quy định các yêu cầu cho **Hệ thống Quản lý Chất lượng (Quality Management System – QMS)**.

Tài liệu này cung cấp hướng dẫn **vận hành thực tế** để thiết lập, triển khai và duy trì QMS, **tương thích với DevOps, CI/CD, và vận hành doanh nghiệp**. Nó **mang tính thực hành, hướng doanh nghiệp**, không phải học thuật.

---

## 2. Phạm vi (Scope)
Phạm vi bao gồm:
- Quy trình vận hành trong DevOps pipelines
- Quản lý release phần mềm
- Quản lý thay đổi (Change Management)
- Quản lý sự cố và vấn đề (Incident & Problem Management)
- Kiểm soát và tài liệu hóa quy trình

Ngoài phạm vi:
- Chiến lược tổ chức ngoài quản lý chất lượng vận hành
- Quy trình không liên quan đến IT

---

## 3. Nguyên tắc cốt lõi (Core Principles)
Các nguyên tắc ISO 9001 áp dụng:
- **Customer Focus (Tập trung vào khách hàng):** Stakeholders nội bộ, teams sản phẩm
- **Leadership (Lãnh đạo):** Rõ vai trò, trách nhiệm, accountability
- **Engagement of People (Tham gia của mọi người):** Đào tạo, nhận thức, tham gia
- **Process Approach (Quy trình):** Workflow chuẩn hóa, lặp lại được
- **Improvement (Cải tiến liên tục):** Nâng cao quy trình
- **Evidence-based Decision Making (Quyết định dựa trên bằng chứng):** Metrics, KPI
- **Relationship Management (Quản lý quan hệ):** Teams, vendors, nhà cung cấp công cụ

---

## 4. Kiến trúc QMS cấp cao (High-Level QMS Architecture)

```
QMS
├── Governance & Policy
│   ├── Quality Policy
│   ├── Roles & Responsibilities
│   └── Process Ownership
│
├── Process Management
│   ├── DevOps Pipelines
│   ├── Change Management
│   ├── Release Management
│   └── Incident & Problem Management
│
├── Documentation Control
│   ├── SOPs
│   ├── Checklists
│   └── Versioning & Review
│
├── Performance & Metrics
│   ├── KPIs
│   ├── Process Efficiency
│   └── Audit Results
│
└── Continuous Improvement
    ├── Review Meetings
    ├── Lessons Learned
    └── Process Optimization
```

---

## 5. Quy trình tiếp cận (Process Approach)
1. **Plan (Lập kế hoạch):** Xác định workflow, tiêu chuẩn, trách nhiệm
2. **Do (Thực hiện):** Thực hiện quy trình theo tiêu chuẩn
3. **Check (Kiểm tra):** Giám sát KPI, audit quy trình, ghi nhận vấn đề
4. **Act (Hành động):** Khắc phục, phòng ngừa, tối ưu quy trình

---

## 6. Kiểm soát tài liệu (Documentation Control)
Tất cả tài liệu được kiểm soát bằng:
- Versioning
- Xác định Author và Owner
- Chu kỳ phê duyệt và review
- Lưu trữ trong repo version-controlled (Git hoặc hệ thống tài liệu)

---

## 7. Giám sát hiệu suất & chỉ số (Performance Monitoring & Metrics)
Ví dụ các chỉ số cho QMS trong DevOps:
- Mean Time to Deploy (MTTD)
- Change Failure Rate
- Incident Response Time
- Audit Findings & Closure Rate
- Process Compliance Rate

---

## 8. Cải tiến liên tục (Continuous Improvement)
- Review meeting sau major releases
- Post-mortem sau sự cố
- Audit định kỳ hàng quý
- Giám sát và báo cáo KPI

---

## 9. Kết quả mong đợi (Expected Outcomes)
- Quy trình vận hành chuẩn hóa và lặp lại được
- Chất lượng DevOps pipeline dự đoán được
- Tài liệu và quy trình audit-ready
- Cải tiến liên tục hiệu quả vận hành
- Tương thích với tiêu chuẩn QMS doanh nghiệp

