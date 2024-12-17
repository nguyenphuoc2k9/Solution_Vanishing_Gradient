
# Dự án: Vanishing Gradient

## Giới thiệu

Hiện tượng **Vanishing Gradient** là một trong những thách thức lớn trong quá trình huấn luyện các mạng neural sâu. Khi mô hình trở nên phức tạp hơn với nhiều lớp (layers), gradient qua từng lớp dần trở nên nhỏ, dẫn đến việc cập nhật trọng số không hiệu quả và mô hình gần như không học được.

### Mục tiêu của dự án:
- Phân tích hiện tượng Vanishing Gradient trong các mạng MLP.
- Triển khai và đánh giá hiệu quả của các giải pháp khắc phục Vanishing Gradient.

---

## Các bước thực hiện

### 1. **Thiết lập baseline model**
- Sử dụng mạng MLP gồm 7 lớp ẩn với hàm kích hoạt Sigmoid, để quan sát hiện tượng Vanishing Gradient.
- Dữ liệu sử dụng: Fashion MNIST.

### 2. **Thử nghiệm các giải pháp cải tiến**
Dự án triển khai các giải pháp sau:
1. **Weight Initialization**: Khởi tạo trọng số với giá trị lớn hơn.
2. **Activation Functions**: Thay thế Sigmoid bằng các hàm tiên tiến hơn như ReLU.
3. **Optimizers**: Sử dụng thuật toán Adam thay vì SGD.
4. **Normalization**: Áp dụng Batch Normalization hoặc lớp chuẩn hóa tùy chỉnh.
5. **Skip Connections**: Thêm skip connections vào kiến trúc mạng.
6. **Fine-tuning Layers**: Huấn luyện từng phần của mạng (layer-wise training).
7. **Gradient Normalization**: Chuẩn hóa gradient trong quá trình lan truyền ngược.

---

## Yêu cầu môi trường

- **Ngôn ngữ lập trình**: Python  
- **Thư viện chính**:  
  - PyTorch  
  - torchvision  
  - matplotlib  
  - numpy

---

## Hướng dẫn cài đặt

1. **Clone dự án**  
   ```bash
   git clone <repository-url>
   cd VanishingGradient
   ```

2. **Cài đặt thư viện yêu cầu**  
   ```bash
   pip install -r requirements.txt
   ```

3. **Chạy chương trình**  
   ```bash
   python main.py
   ```

---

## Kết quả và đánh giá

- Hiệu suất của từng giải pháp được đo lường dựa trên các chỉ số như:  
  - Độ chính xác (Accuracy)  
  - Loss trên tập train, validation, và test.  

- Kết quả được trực quan hóa qua đồ thị.

---

## Phụ lục
- **Tài liệu tham khảo**:  
  - [Survey on Activation Functions for Deep Learning](https://medium.com/@shrutijadon/survey-on-activation-functions-for-deep-learning-9689331ba092)  
  - [Skip Connections in ResNet](https://arxiv.org/pdf/1512.03385)  

---

