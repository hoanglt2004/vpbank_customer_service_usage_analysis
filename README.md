# VPBank CRM Customer Service Usage Analysis

> Phân tích mức độ sử dụng dịch vụ khách hàng tại chi nhánh ngân hàng và đề xuất hướng tăng trưởng doanh thu **+20%** dựa trên dữ liệu CRM (Customer Segment, AUM, Product Holding).

📌 **Public Power BI Report (View-only):**
https://shorturl.at/YH3Ye

📄 **Slide/PDF Summary:** `VPBANK_CRM_REPORT.pdf`

---

## 1. Business Context

Giám đốc chi nhánh cần một báo cáo tổng quan để:
- Nắm **tình hình khách hàng hiện tại** theo phân khúc và khu vực.
- Hiểu **tình hình tài sản (AUM)** và mức độ đóng góp theo nhóm khách hàng.
- Đánh giá **mức độ phổ cập các sản phẩm/dịch vụ** (App, TK thanh toán, Thẻ tín dụng, Tiền gửi kỳ hạn, Vay…).
- Trả lời 2 câu hỏi:
  1) Hiện có **bao nhiêu phân khúc khách hàng**?  
  2) Nếu KPI quý tới là **tăng doanh thu 20%**, nên tập trung dịch vụ nào để bán chéo / tăng doanh thu?

---

## 2. Dataset

Dữ liệu gồm 3 file CSV:

### `cust.csv` – Thông tin khách hàng
| Column | Description |
|---|---|
| `customer_id` | Mã định danh khách hàng |
| `segment` | Phân khúc khách hàng (Regular / Silver / Gold) |
| `province_city` | Tỉnh/thành phố sinh sống |

### `aum.csv` – Tổng tài sản khách hàng
| Column | Description |
|---|---|
| `customer_id` | Mã định danh khách hàng |
| `amount` | Tổng tài sản khách hàng nắm giữ (AUM) |

### `prod_holding.csv` – Sản phẩm khách hàng sử dụng
Các cột thể hiện khách hàng có/không sử dụng sản phẩm (nhị phân hoặc số lượng tùy dữ liệu):
- `prod_ca` (TK thanh toán)
- `prod_td` (Tiền gửi có kỳ hạn)
- `prod_credit_card` (Thẻ tín dụng)
- `prod_app` (App chuyển tiền)
- `prod_secured_loan` (Vay thế chấp)
- `prod_upl` (Vay tín chấp)

> Data dictionary chi tiết nằm trong file PDF summary.

---

## 3. Dashboard Scope & KPI

### Key KPIs
- **Total Customers**
- **Customer Distribution by Segment**
- **Customer Distribution by Province/City**
- **Total AUM** & **AUM Contribution by Segment**
- **Product Penetration Rate** (tỷ lệ phổ cập từng sản phẩm)
- **Avg Products per Customer** theo phân khúc
- **Cross-sell Opportunity** (nhóm khách hàng lớn nhưng dùng ít sản phẩm lợi nhuận cao)

### Pages/Sections
1) Tổng quan dữ liệu  
2) Tổng quan khách hàng (Segment + Geography)  
3) Tổng quan tài sản (AUM)  
4) Tổng quan dịch vụ (product usage)  
5) Đề xuất tăng trưởng doanh thu 20%

---

## 4. Main Findings (Insights)

### 4.1 Customer Base
- Quy mô khách hàng lớn (~113K). **Nhóm Regular chiếm đa số (~81%)** → là “mass segment” để mở rộng bán chéo.
- Khách hàng tập trung mạnh ở **Hà Nội & TP.HCM (~68%)** → tăng trưởng & rủi ro tập trung vào 2 thị trường lớn.

### 4.2 AUM Concentration
- Nhóm **Gold chỉ ~3% khách hàng nhưng đóng góp ~78% tổng AUM** → đòn bẩy tài chính lớn, cần ưu tiên giữ chân.
- Nhóm **Regular rất đông nhưng hiệu suất sử dụng tài sản thấp** → cần sản phẩm hấp dẫn để khai thác tốt hơn tiềm năng.

### 4.3 Product Usage
- **App Mobile gần như phổ cập 100%** → kênh tốt để kích hoạt bán chéo.
- Các sản phẩm có biên lợi nhuận cao như **Thẻ tín dụng / Tiền gửi kỳ hạn / Vay** có tỷ lệ sử dụng còn thấp → cơ hội tăng doanh thu nằm ở cross-sell.

> Toàn bộ số liệu/insight chi tiết có trong report & PDF summary.

---

