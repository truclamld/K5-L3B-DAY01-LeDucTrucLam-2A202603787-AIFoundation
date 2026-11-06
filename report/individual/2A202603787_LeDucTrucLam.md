# Báo cáo cá nhân — Day 01: Lọc tin nhắn rác bằng ML, DL, Embedding và LLM

> Đổi tên file này thành `MSSV_HoTen.md` của bạn, ví dụ `2A20260000_NguyenVanAn.md`, rồi điền từng mục. Xoá các dòng hướng dẫn in nghiêng khi xong.

- **MSSV: 2A202603787**
- **Họ và tên: Lê Đức Trúc Lâm**
- **SEED** (in ở ô đầu notebook): 940

## 1. Bằng chứng

| Tệp | Có? |
| --- | --- |
| [`day01_lab.ipynb`](day01_lab.ipynb) — notebook đã chạy, còn output | ✔ |
| [`lab1_report.json`](lab1_report.json) — do ô "Báo cáo cuối" sinh ra | ✔ |
| [`hand_calc.jpg`](hand_calc.jpg) — ảnh tính tay có các bước | ✔ |

## 2. Kết quả chính

*Chép bảng so sánh cuối Phần 5 (F1 test, F1 SUB 40, p95 ms/tin, USD/1k tin) của chính bạn.*
 precision  recall  F1 (test)  F1 (SUB 40)  \
1. BoW + LogReg (tự code)            1.000   0.809      0.894        0.919   
3a. Encoder (MiniLM) + kNN           0.882   0.957      0.918        0.947   
3b. Encoder (MiniLM) + LogReg        0.938   0.968      0.953        0.947   
3c. Encoder (MiniLM) + MLP head      0.938   0.968      0.953        0.947   

                                 train (s)  tin/s (cả lô)  p50 ms/tin  \
1. BoW + LogReg (tự code)            3.001      26895.454       0.194   
3a. Encoder (MiniLM) + kNN          71.768         34.033      41.373   
3b. Encoder (MiniLM) + LogReg       72.240         45.984      33.092   
3c. Encoder (MiniLM) + MLP head     73.241         39.193      27.428   

                                 p95 ms/tin  USD / 1k tin  
1. BoW + LogReg (tự code)             0.234           0.0  
3a. Encoder (MiniLM) + kNN           56.305           0.0  
3b. Encoder (MiniLM) + LogReg        55.588           0.0  
3c. Encoder (MiniLM) + MLP head      37.455           0.0  

## 3. Dự đoán và thực tế

*Chọn 3 dự đoán `predict(...)` lệch nhiều nhất so với kết quả. Mỗi cái: bạn đoán gì, ra gì, vì sao lệch.*

## 4. Phân tích 50 case khó

*Model nào tụt nhiều nhất, ở nhóm case nào? Nêu 2 case cụ thể và cơ chế khiến model sai.*

## 5. Thử thách cá nhân

*Đề theo SEED của bạn, cách làm, kết quả, giải thích.*

## 6. Phương án cho sản phẩm thật

*Với yêu cầu p95 < 50 ms/tin cho 10 triệu SMS/ngày: chọn phương án nào, dẫn số liệu nào, chấp nhận đánh đổi gì.*

## 7. AI log và điều đã học

*Mỗi lần dùng AI: hỏi gì, nhận gì, bạn sửa gì. Sau đó 2–3 câu: điều bạn hiểu ra hôm nay mà trước đó chưa hiểu.*

Qua bài này, mình đã có cái nhìn sâu hơn về cách hoạt động của các thuật toán học máy. Việc không sử dụng thư viện scikit-learn giúp mình hiểu rõ hơn về thuật toán học máy bên trong và khả năng tinh chỉnh các tham số sâu giúp linh hoạt hơn theo từng trường hợp sử dụng cụ thể.
