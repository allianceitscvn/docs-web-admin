# Luồn dev mới

Requirements

* Visual Code
  * Git graph
  * Remote SSH
    *   Test:&#x20;

        ```
        ssh -T git@github.com
        ```

Source trên github

User mới

* Chạy lệnh: ssh-keygen -t ed25519 -C "your-email@allianceitsc.com"
* Chạy lệnh: cat \~/.ssh/id\_ed25519.pub
* Copy nội dung gửi cho htruong@allianceitsc.com
* Admin add key vào github

Tạo thư viện module mới

* Theo docs: [https://www.npmjs.com/package/create-react-library](https://www.npmjs.com/package/create-react-library)
  * npm install -g create-react-library
  * npx create-react-library
* Go to folder example
  * npm install --save ../
* Start library
  * npm start
* Start example
  * cd example
  * npm start

