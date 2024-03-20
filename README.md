### Hướng dẫn triển khai máy chủ trên Linux

`Lưu ý:` Đọc kỹ trước khi thực hiện tránh clone nhiều repo

#### 1. Cài đặt môi trường:

```bash
cd ~
sudo apt-get update && sudo apt-get install -y vim python-pip curl git
pip install docker-compose
```

#### 2. Cài Docker:

```bash
sudo curl -sSL get.docker.com | sh
```


#### 3. Clone repo:

```bash
git clone https://github.com/anhphoang-vncn/code-tour-de-challenge-back-end.git && cd code-tour-de-challenge-back-end
```

#### 4. Khởi động:

```bash
docker-compose up -d
```

> Luu ý: Nếu bạn không dùng user `root`，hãy sử dụng lệnh sau:

```bash
sudo -E docker-compose up -d
```
> Quá trình cài đặt có thể tốn từ 5 đến 30 phút phụ thuộc vào tốc độ mạng!
> Sau đó, hãy kiểm tra bằng lệnh `docker ps -a`，nếu không có container nào ở trạng thái `unhealthy` hoặc `Exited (x) xxx` thì bạn đã triển khai thành công trển cổng 80 hoặc 443.

#### 5. Sử dụng:

Truy cập vào `http://localhost:7676/admin` (cổng `7676` là website [FRONT-END](https://github.com/anhphoang-vncn/code-tour-de-challenge) đang chạy) để đăng nhập vào phân hệ quản trị và bắt đầu sử dụng.

### Chú ý

Tên người dùng quản trị viên được tự động thêm vào trong quá trình cài đặt là `root` và mật khẩu là `rootroot`. **Vui lòng thay đổi mật khẩu ngay**.

### Tài liệu 

http://opensource.qduoj.com/
