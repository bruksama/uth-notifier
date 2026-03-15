# 📅 UTH Calendar Bot

[![Docker Image](https://img.shields.io/badge/Docker-v1.5.0-blue?logo=docker)](https://hub.docker.com/r/vanphat111/uth-calendar)
[![Python Version](https://img.shields.io/badge/Python-3.11+-yellow?logo=python)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

Một trợ lý Telegram thông minh hỗ trợ sinh viên trường **Đại học Giao thông Vận tải TP.HCM (UTH)** quản lý và theo dõi lịch học cá nhân một cách tự động.

## 🚀 Tính năng chính

* 🔔 **Nhắc lịch tự động:** Tự động gửi lịch học vào 05:00, 12:00 và 17:00 hàng ngày.
* 🔍 **Tra cứu thủ công:** Xem lịch hôm nay, ngày mai hoặc một ngày bất kỳ qua Menu nút bấm.
* 🔗 **Tích hợp LMS:** Tên môn học được đính kèm Hyperlink dẫn trực tiếp đến khóa học trên hệ thống LMS/Courses.
* 🐳 **Dockerized:** Hỗ trợ triển khai nhanh chóng thông qua Docker và Docker Compose.
* 🛡️ **Minh bạch:** Mã nguồn mở hoàn toàn, đảm bảo an toàn dữ liệu cá nhân.

## 🛠 Tech Stack

* **Language:** Python 3.11+
* **Library:** `pyTelegramBotAPI` (Telebot)
* **Database:** PostgreSQL
* **Automation:** `schedule`, `threading`
* **Deployment:** Docker, Docker Compose

---

## ⚙️ Cấu hình hệ thống

Hệ thống sử dụng các biến môi trường (Environment Variables) để cấu hình. Hãy chuẩn bị file `.env` với các nội dung sau:

| Biến | Mô tả |
| :--- | :--- |
| `TELE_TOKEN` | API Token của Bot (lấy từ @BotFather) |
| `ADMIN_ID` | ID Telegram của người quản trị |
| `DB_HOST` | Địa chỉ host của PostgreSQL |
| `DB_NAME` | Tên cơ sở dữ liệu |
| `DB_USER` | Tên đăng nhập Database |
| `DB_PASS` | Mật khẩu Database |

---

## 📦 Hướng dẫn cài đặt (Setup)

### Cách 1: Sử dụng Docker Compose (Khuyên dùng)

1. **Clone Repo:**
   ```bash
   git clone https://github.com/vanphat111/uthCalendar.git
   cd uthCalendar
   ```
2. **Tạo file .env và điền thông số.**

3. **Chạy hệ thống:**
    ```Bash
    docker compose up -d
    ```
### Cách 2: Cài đặt thủ công (Manual)
1. **Cài đặt thư viện:**

```Bash
pip install -r requirements.txt
```
2. **Khởi tạo Database:** Đảm bảo bạn đã có một instance PostgreSQL đang chạy.

3. **Chạy Bot:**

```Bash
python uth_tele_bot.py
```


## 🤝 Đóng góp (Contribution)
Project này được xây dựng bởi một sinh viên năm 2 với mục đích hỗ trợ cộng đồng sinh viên UTH. Mọi đóng góp (Pull Request), báo lỗi (Issue) đều được trân trọng.

1. Fork dự án.

2. Tạo branch tính năng mới (git checkout -b feature/AmazingFeature).

3. Commit thay đổi (git commit -m 'Add some AmazingFeature').

4. Push lên branch (git push origin feature/AmazingFeature).

5. Mở một Pull Request.

**Author:** vanphat111

**Project Link:** https://github.com/vanphat111/uthCalendar