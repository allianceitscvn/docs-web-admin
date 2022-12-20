# Tạo local key ed25519

#### Chạy lệnh từ terminal (Nhớ thay đổi your-email thành email của bạn)

```
ssh-keygen -t ed25519 -C "your-email@allianceitsc.com"
```

#### Sau khi thành công chạy tiếp lệnh

```
cat ~/.ssh/id_ed25519.pub
```

Ví dụ

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption><p>Kết quả hiển thị</p></figcaption></figure>

#### Copy dòng kết quả gửi cho người yêu cầu
