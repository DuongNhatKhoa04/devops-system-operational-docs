# ISO/IEC 27001 – Hệ thống Quản lý An toàn Thông tin (ISMS)

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
ISO/IEC 27001 định nghĩa các yêu cầu để **thiết lập, triển khai, duy trì và cải tiến liên tục** Hệ thống Quản lý An toàn Thông tin (**Information Security Management System – ISMS**).

Tài liệu này được viết theo hướng **vận hành / kỹ thuật (operational & technical)**, không mang tính học thuật. Mục tiêu là cung cấp một khung ISO 27001 **áp dụng thực tế** cho môi trường DevOps, Cloud và Enterprise IT.

---

## 2. Phạm vi áp dụng (Scope)
Phạm vi ISMS trong tài liệu này bao gồm:
- Source code repositories (Git)
- CI/CD pipelines
- Infrastructure (On-premise, Cloud, Hybrid)
- Deployment environments (Dev, Staging, Production)
- Secrets, credentials, sensitive configuration
- Quyền truy cập vận hành (Developer, DevOps, SRE, Administrator)

Ngoài phạm vi (Out of scope):
- Quản lý thiết bị người dùng cuối (End-user devices) trừ khi có yêu cầu đặc biệt
- Tuân thủ pháp lý ngoài phạm vi an toàn thông tin

---

## 3. Nguyên tắc cốt lõi (Core Principles)
ISO 27001 dựa trên **risk-based approach** thay vì bảo mật dạng checklist.

Các nguyên tắc chính:
- **Confidentiality (Tính bảo mật):** Thông tin chỉ được truy cập bởi các thực thể được phép
- **Integrity (Tính toàn vẹn):** Thông tin chính xác và không bị thay đổi trái phép
- **Availability (Tính sẵn sàng):** Hệ thống và dữ liệu sẵn sàng khi cần
- **Continual Improvement (PDCA):** Plan → Do → Check → Act

---

## 4. Kiến trúc ISMS cấp cao (ISMS High-Level Architecture)

```
ISMS
├── Governance & Policy
│   ├── Information Security Policy
│   ├── Risk Management Policy
│   └── Access Control Policy
│
├── Risk Management
│   ├── Asset Identification
│   ├── Risk Assessment
│   ├── Risk Treatment Plan
│   └── Statement of Applicability (SoA)
│
├── Operational Controls
│   ├── Identity & Access Management (IAM)
│   ├── Secure CI/CD
│   ├── Infrastructure Security
│   └── Monitoring & Logging
│
├── Incident Management
│   ├── Detection
│   ├── Response
│   └── Lessons Learned
│
└── Audit & Improvement
    ├── Internal Audit
    ├── Management Review
    └── Continuous Improvement
```

---

## 5. Cách tiếp cận Quản lý Rủi ro (Risk Management Approach)
ISO 27001 yêu cầu **quản lý rủi ro có tài liệu hóa, lặp lại được và có thể audit**.

### 5.1 Xác định tài sản (Asset Identification)
Ví dụ:
- Git repositories
- CI/CD runners
- Container registries
- Cloud accounts
- Secrets (API keys, certificates)

### 5.2 Đánh giá rủi ro (Risk Assessment)
Mỗi tài sản được đánh giá dựa trên:
- Threats (Mối đe dọa)
- Vulnerabilities (Điểm yếu)
- Impact (Mức độ ảnh hưởng)
- Likelihood (Khả năng xảy ra)

Công thức rủi ro:

```
Risk = Impact × Likelihood
```

### 5.3 Xử lý rủi ro (Risk Treatment Options)
- **Mitigate:** Áp dụng biện pháp kiểm soát an toàn thông tin
- **Avoid:** Loại bỏ hoạt động có rủi ro cao
- **Transfer:** Chuyển giao rủi ro (bên thứ ba, bảo hiểm)
- **Accept:** Chấp nhận rủi ro (có phê duyệt và tài liệu hóa)

---

## 6. Statement of Applicability (SoA)
**SoA** ánh xạ các biện pháp kiểm soát trong **Annex A** với quyết định triển khai thực tế.

Ví dụ:

| Control | Status | Justification |
|-------|--------|---------------|
| A.5.15 Access Control | Applied | Bắt buộc cho CI/CD và Cloud access |
| A.8.12 Data Leakage | Applied | Áp dụng secrets management |
| A.6.3 Awareness | Planned | Lộ trình đào tạo an toàn thông tin |

---

## 7. Ánh xạ ISO 27001 với DevOps (DevOps-Focused Control Mapping)

| ISO 27001 Domain | Triển khai trong DevOps |
|-----------------|-------------------------|
| Access Control | RBAC, MFA, least privilege |
| Change Management | Pull Request, Code Review |
| Logging & Monitoring | Centralized logging, SIEM |
| Secure Development | SAST, DAST, dependency scanning |
| Incident Response | Runbook, post-mortem |

---

## 8. Cải tiến liên tục (Continuous Improvement)
Các biện pháp kiểm soát an toàn thông tin được rà soát:
- Sau mỗi security incident
- Sau thay đổi hệ thống lớn
- Theo chu kỳ review định kỳ

Ví dụ metric:
- Số lượng security incidents
- Mean Time To Detect (MTTD)
- Mean Time To Respond (MTTR)
- Xu hướng audit findings

---

## 9. Kết quả mong đợi (Expected Outcomes)
- Giảm rủi ro an toàn thông tin
- Vận hành bảo mật có thể audit và dự đoán được
- Cân bằng giữa tốc độ DevOps và yêu cầu bảo mật doanh nghiệp
- Sẵn sàng cho ISO/IEC 27001 certification khi cần
