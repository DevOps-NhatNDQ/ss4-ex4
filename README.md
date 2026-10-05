## 1. Nội dung tệp .gitignore

```text
credentials.txt
```

## 2. Giải thích câu lệnh git rm --cached
- Lệnh `git rm --cached <file>` gỡ bỏ tệp tin khỏi **Staging Area / Index (cache theo dõi của Git)**.
- Điểm quan trọng: Lệnh này **không xóa tệp tin vật lý** trong thư mục làm việc cục bộ, đáp ứng đúng ràng buộc bảo toàn dữ liệu trên ổ cứng.

## 3. Quy trình thực hiện
1. Trót add và commit nhầm file `credentials.txt`.
2. Chạy `git rm --cached credentials.txt` để gỡ file khỏi sự theo dõi của Git.
3. Thêm `credentials.txt` vào `.gitignore` để Git không gợi ý theo dõi file này nữa.
4. Thêm `.gitignore` vào Staging Area bằng `git add .gitignore`.
5. Sử dụng `git commit --amend -m "Add gitignore to ignore sensitive credentials"` để ghi đè commit lỗi trước đó.

## 4. Kết quả kiểm tra lịch sử commit (git log -n 1)
```bash
commit 3be791af88afd8ec83f48ed5505f2f3a8e0ca1d7 (HEAD -> master)
Author: Quang Nhat <ngduyquangnhat03@gmail.com>
Date:   Mon Oct 5 21:31:26 2026 +0700

    Add gitignore to ignore sensitive credentials
```
