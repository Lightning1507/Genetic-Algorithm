# 🧬 Traveling Salesman Problem (TSP) with Optimized Genetic Algorithms

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange)
![License](https://img.shields.io/badge/License-MIT-green)

Dự án này triển khai và so sánh hiệu năng của các biến thể **Giải thuật Di truyền (Genetic Algorithms - GA)** khác nhau để giải quyết bài toán Người du lịch (Traveling Salesman Problem - TSP).

Mục tiêu là tìm ra lộ trình ngắn nhất đi qua `N` thành phố và quay trở lại điểm xuất phát, sử dụng các chiến lược tiến hóa tối ưu.

## 📊 Kết quả Demo

![Kết quả so sánh](results.png)
*(Hình ảnh minh họa so sánh giữa Nearest Neighbor và 3 chiến lược GA)*

## 🚀 Các tính năng chính

Dự án so sánh 4 phương pháp tiếp cận:

1.  **Nearest Neighbor (Heuristic):** Thuật toán tham lam đơn giản để tạo mốc so sánh (Baseline) và khởi tạo quần thể (Seeding).
2.  **Standard GA:** Giải thuật di truyền tiêu chuẩn (Generational).
3.  **Steady State GA:** Duy trì trạng thái ổn định, chỉ thay thế một phần nhỏ quần thể yếu mỗi thế hệ.
4.  **GA + Elitism:** Kết hợp bảo tồn tinh hoa (Elitism) để đảm bảo cá thể tốt nhất luôn sống sót.

### Các kỹ thuật tối ưu hóa đã sử dụng:
* **Ordered Crossover (OX1):** Lai ghép giữ thứ tự gen, tránh trùng lặp thành phố.
* **Inversion Mutation:** Đột biến đảo ngược chuỗi (hiệu quả cao trong việc gỡ các đường chéo).
* **Tournament Selection:** Chọn lọc cạnh tranh.
* **Caching:** Tối ưu hóa tính toán khoảng cách (Fitness function).

## 🛠 Cài đặt & Sử dụng

### Yêu cầu
* Python 3.x
* Jupyter Notebook
* Các thư viện: `numpy`, `matplotlib`

### Hướng dẫn chạy

1.  Clone repository này về máy:
    ```bash
    git clone [https://github.com/Lightning1507/Genetic-Algorithm.git](https://github.com/Lightning1507/Genetic-Algorithm.git)
    ```

2.  Cài đặt các thư viện cần thiết:
    ```bash
    pip install numpy matplotlib notebook
    ```

3.  Mở Jupyter Notebook:
    ```bash
    jupyter notebook
    ```

4.  Mở file `TSP_Genetic_Algorithm.ipynb` và chạy chọn **Run All** để xem quá trình huấn luyện và biểu đồ so sánh.

## 📈 Phân tích kết quả

Dựa trên thực nghiệm với `100` thành phố và `2000` thế hệ:

* **Nearest Neighbor:** Cho kết quả cực nhanh nhưng thường bị kẹt ở tối ưu cục bộ.
* **Standard GA:** Cải thiện đáng kể so với NN nhưng đôi khi hội tụ chậm.
* **GA + Elitism:** Thường cho kết quả tốt nhất về độ dài quãng đường (Fitness) nhờ việc không đánh mất các gen tốt nhất.

## 📂 Cấu trúc dự án

```text
├── TSP_Genetic_Algorithm.ipynb  # Main notebook chứa toàn bộ code và visualization
├── results.png                  # Ảnh chụp kết quả chạy thực tế
└── README.md                    # Tài liệu hướng dẫn
```

## 🤝 Đóng góp

Mọi đóng góp (Pull requests) để tối ưu hóa thêm tốc độ hoặc thử nghiệm các toán tử lai ghép/đột biến mới đều được hoan nghênh! 

## 👥 Nhóm tác giả

Dự án này được thực hiện bởi nhóm sinh viên/nghiên cứu:

1. **[Đặng Hoàng Quân]**
   * **GitHub:** [@Lightning1507](https://github.com/Lightning1507)

2. **[Nguyễn Minh Quân]**
   * **GitHub:** [@mingquanjp](https://github.com/mingquanjp)