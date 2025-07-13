# 🤖 Qwen 2.5 Chatbot (FastAPI + React)
Dự án mini xây dựng chatbot AI đơn giản bằng FastAPI cho backend và React cho frontend. Chatbot sử dụng mô hình Qwen 2.5 chạy cục bộ thông qua Ollama.

## 🧰 Công nghệ sử dụng
* ✅ Python 3.10+

* ✅ FastAPI

* ✅ ReactJS (Vite hoặc CRA)

* ✅ Axios

* ✅ Ollama (để chạy model Qwen 2.5 offline)

* ✅ Uvicorn
---

## 🚀 1. Cách chạy Backend (FastAPI)
* **✅ Cài đặt môi trường ảo:**
```bash
python -m venv myvenv
myvenv\Scripts\activate    # Windows
```
* **✅ Cài đặt thư viện cần thiết:**
```bash
pip install fastapi uvicorn pydantic[dotenv] ollama
```
* **✅ Khởi chạy server:**
```bash
uvicorn server:app --reload --host 127.0.0.1 --port 8000
```
### 📌 Không dùng 0.0.0.0 để truy cập từ chính trình duyệt. Dùng 127.0.0.1 hoặc localhost.
---

## 💬 2. Cách chạy Frontend (React)
* **✅ Cài đặt package (chạy 1 lần):**
```bash
npm install
```
* **✅ Khởi chạy:**
```bash
npm start
```
> Mặc định sẽ chạy tại http://localhost:3000


### 🔄 3. Cách hoạt động
* Người dùng nhập câu hỏi vào React frontend

* Gửi request POST /chat đến FastAPI server

* Backend sử dụng ollama gọi model "qwen2.5" để sinh phản hồi

* Phản hồi được trả lại frontend để hiển thị

📁 Cấu trúc thư mục
```bash
qwen-chatbot/
├── server.py               # FastAPI backend
├── myvenv/                 # Virtual env (bỏ vào .gitignore)
├── frontend/               # Thư mục React App
│   ├── src/
│   │   └── App.js          # Giao diện chính
│   └── public/
└── README.md
```

## 🛠️ API Endpoint
```http
POST /chat
Request Body (JSON):
```
```json
{
  "message": "Hello AI!"
}
Response:
```

```json
{
  "response": "Hi! How can I help you today?"
}
```
⚠️ Lưu ý khi dùng ollama:
Đảm bảo đã cài Ollama: [Ollama](https://ollama.com)

Tải model bằng lệnh:

```bash
ollama run qwen2.5
```

## ✍️ Tác giả
Trần Vũ Đình Chính

Liên hệ: [https://github.com/dinhchinh318](https://github.com/dinhchinh318)