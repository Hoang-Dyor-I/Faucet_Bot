### **1. Chuẩn bị file cần thiết**

* **wallets.txt**: danh sách địa chỉ ví, mỗi dòng 1 ví.
* **proxies.txt**: danh sách proxy dạng `host:port:user:password`, mỗi dòng 1 proxy.

> 🗂 ** Cấu trúc thư mục**

```
/thư_mục_chạy/
│-- solana.py        # file script
│-- wallets.txt
│-- proxies.txt
```

---

### **2. Cài đặt môi trường**

> 🗂 ** Cài Python & thư viện**

1. Cài Python 3.8+
2. Cài thư viện:

```bash
pip install requests
```

---

### **3. Chỉnh thông số trong script (tùy chọn)**

* `MIN_THREADS` và `MAX_THREADS`: số luồng song song (20–25 mặc định).
* `REQUEST_INTERVAL`: thời gian nghỉ giữa mỗi batch (10 giây mặc định).
* `DELAY_BETWEEN_REQUESTS`: thời gian chờ ngẫu nhiên mỗi request (1–3 giây mặc định).

---

### **4. Chạy script**

> 🗂 ** Chạy script**

```bash
python solana.py
```

* Script sẽ:

  1. Đọc danh sách ví và proxy.
  2. Gửi yêu cầu airdrop cho từng ví qua từng proxy.
  3. Chạy liên tục lặp lại.

---

### **5. Kiểm tra kết quả**

* Thành công: `✅ Airdrop thành công cho <wallet>`
* Thất bại: `❌ Airdrop thất bại`
* Lỗi proxy/kết nối: `⚠️ Lỗi proxy hoặc kết nối`

