# Hệ thống Y tế Cảnh báo sớm Rối loạn nhịp tim ứng dụng AI & IoT

![Tech](https://img.shields.io/badge/Tech-IoT_|_AI_|_Web-orange?style=for-the-badge)

> **Đồ án Tốt nghiệp Công nghệ Thông tin - Đại học Bách khoa Hà Nội**
> * **Sinh viên:** Vũ Ngọc Đức
> * **GVHD:** TS. Đỗ Công Thuần

---

## Giới thiệu (Introduction)

Dự án này là một hệ thống chăm sóc sức khỏe toàn diện (End-to-End Healthcare System) tích hợp IoT và Trí tuệ nhân tạo nhằm giám sát liên tục và cảnh báo sớm các bất thường về tim mạch (Rung nhĩ, Ngoại tâm thu...). Hệ thống bao gồm thiết bị đeo thu thập dữ liệu sinh tồn, mô hình học sâu phân tích điện tâm đồ (ECG) thời gian thực và ứng dụng Web đa nền tảng kết nối Bác sĩ - Bệnh nhân.

## Cấu trúc Mã nguồn (Project Structure)

Hệ thống được chia thành 3 phân hệ chính. Vui lòng truy cập các đường dẫn dưới đây để xem chi tiết mã nguồn và hướng dẫn cài đặt cho từng phần:

| Phân hệ (Module) | Công nghệ chính | Link Repo |
| :--- | :--- | :--- |
| **1. Trí tuệ nhân tạo (AI Engine)** | ![Python](https://img.shields.io/badge/Python-3.8+-blue) ![Keras](https://img.shields.io/badge/Keras-TensorFlow-red) | **[LINK REPO AI](https://github.com/DucBunny/Telemedicine-ML)**<br>Chứa mã nguồn xử lý dữ liệu MIT-BIH, kỹ thuật cân bằng dữ liệu **SMOTETomek**, và code huấn luyện mô hình lai ghép **CNN-BiLSTM**. |
| **2. Ứng dụng Web (Web App)** | ![React](https://img.shields.io/badge/React-PWA-blue) ![NodeJS](https://img.shields.io/badge/Node.js-Express-green) | **[LINK REPO WEB](https://github.com/DucBunny/Telemedicine-Web)**<br>Bao gồm Backend (Express, RabbitMQ Worker), Frontend (ReactTS, PWA) và module **WebRTC** video call. |
| **3. Thiết bị IoT (Firmware)** | ![C++](https://img.shields.io/badge/C++-ESP32-blue) ![MQTT](https://img.shields.io/badge/Proto-MQTT-orange) | **[LINK REPO FIRMWARE]()**<br>Mã nguồn C++ nạp cho vi điều khiển **ESP32**. |

---

## Tính năng nổi bật (Key Features)
- Giám sát thời gian thực: Đo và hiển thị nhịp tim (BPM), SpO2 và biểu đồ sóng ECG với độ trễ thấp.

- Cảnh báo thông minh: Tự động phát hiện 5 loại nhịp tim theo chuẩn AAMI (Bình thường, Rung nhĩ, Ngoại tâm thu...) nhờ mô hình AI độ chính xác ~97.8%.

- Telemedicine: Hỗ trợ gọi Video Call trực tiếp (WebRTC) giữa Bác sĩ và Bệnh nhân.

- Đa nền tảng: Ứng dụng dạng PWA cài đặt được trên cả điện thoại và máy tính.

## Công nghệ sử dụng (Tech Stack)
- Hardware: ESP32, MAX30102, AD8232.

- Connectivity: MQTT, HTTP/RESTful API, WebSocket, WebRTC.

- Backend: Node.js, Express.js, RabbitMQ, Redis.

- Frontend: ReactTS, PWA.

- AI/ML: Python, TensorFlow/Keras, Scikit-learn, Imbalanced-learn.

- Database: MongoDB, MySQL.
