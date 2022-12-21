# Kiểm tra xác thực ssh với github

#### Chạy lệnh

```
ssh -T git@github.com
```

#### Kết quả

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption><p>Kết quả khi thành công</p></figcaption></figure>

Check kỹ hơn

```
ssh -Tv git@github.com
```

Thêm SSH&#x20;

Chạy lệnh

```
ssh-add -K ~/.ssh/id_ed25519
```
