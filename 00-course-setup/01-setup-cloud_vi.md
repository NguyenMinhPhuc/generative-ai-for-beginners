# Thiết lập Cloud ☁️ – GitHub Codespaces

**Hãy sử dụng hướng dẫn này nếu Anh không muốn cài đặt gì trên máy tính cá nhân.**  
Codespaces cung cấp cho Anh một phiên bản VS Code chạy trực tiếp trên trình duyệt với tất cả các phụ thuộc đã được cài đặt sẵn.

---

## 1.  Tại sao nên dùng Codespaces?

| Lợi ích | Ý nghĩa dành cho bạn |
|---------|----------------------|
| ✅ Không cần cài đặt | Hoạt động trên Chromebook, iPad, máy tính phòng lab… |
| ✅ Dev container dựng sẵn | Python 3, Node.js, .NET, Java đã có sẵn |
| ✅ Miễn phí hạn mức | Tài khoản cá nhân có **120 core-hours / 60 GB-hours mỗi tháng** |

> 💡 **Mẹo**  
> Duy trì hạn mức của bạn bằng cách **dừng** hoặc **xóa** các codespace không sử dụng  
> (Menu View ▸ Command Palette ▸ *Codespaces: Stop Codespace*).

---

## 2.  Tạo một Codespace (chỉ một cú nhấp chuột)

1. **Fork** repo này (góc trên bên phải nhấn nút **Fork**).  
2. Trong repo đã fork, nhấn **Code ▸ Codespaces ▸ Create codespace on main**.  
   ![ialog showing buttons to create a codespace](./images/who-will-pay.webp)

✅ Một cửa sổ VS Code trên trình duyệt sẽ mở ra và container dev bắt đầu được dựng.  
Lần đầu tiên quá trình này sẽ mất khoảng **~2 phút**.

---

## 3. Thêm API key của bạn (cách an toàn nhất)

### Tùy chọn A: Codespaces Secrets — Khuyến nghị

1. ⚙️ Biểu tượng bánh răng → Command Palette → Codespaces: Manage user secret → Add a new secret.  
2. Tên: **OPENAI_API_KEY**  
3. Giá trị: dán key của bạn → **Add secret**

Vậy là xong — code sẽ tự động nhận API key này.

---

### Tùy chọn B: File `.env` (nếu thật sự cần)

```bash
cp .env.copy .env
code .env         # điền OPENAI_API_KEY=your_key_here
