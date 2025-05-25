# git-convention

## 1. Quy tắc đặt tên branch
- **Tính năng mới**: `feature/tên-tính-năng`  
  *VD:* `feature/login-page`
- **Sửa lỗi**: `fix/mô-tả-lỗi`  
  *VD:* `fix/typo-in-header`
- **Cải tiến code**: `refactor/mô-tả-công-việc`  
  *VD:* `refactor/authentication-flow`
- **Hotfix (sửa lỗi khẩn cấp)**: `hotfix/mô-tả-lỗi`  
  *VD:* `hotfix/fix-crash-on-login`
- **Branch chính**: `main`, `develop`  

## 2. Quy tắc đặt tên commit message
Commit message nên tuân theo cấu trúc:
```plaintext
<Loại commit>: <Mô tả ngắn gọn>
```
Các loại commit phổ biến:
- `feat`: Thêm tính năng mới
- `fix`: Sửa lỗi
- `docs`: Cập nhật tài liệu
- `style`: Chỉnh sửa code không ảnh hưởng đến logic (formatting, dấu cách, dấu phẩy)
- `refactor`: Cải tiến code mà không thay đổi chức năng
- `test`: Thêm hoặc sửa test case
- `chore`: Công việc lặt vặt (cấu hình, build, v.v.)
- `perf`: Cải thiện hiệu suất

**Ví dụ commit message chuẩn:**
```plaintext
feat: add user authentication feature
fix: resolve bug in login form validation
docs: update API documentation for user endpoints
```

## 3. Quy tắc viết Pull Request (PR)
Một PR tốt nên có:
- **Tiêu đề rõ ràng**: `Add login feature`
- **Mô tả ngắn gọn nhưng đầy đủ**: Mô tả vấn đề, cách giải quyết, ảnh hưởng đến hệ thống, cách kiểm thử.
- **Gắn issue liên quan (nếu có)**: `Closes #123`
- **Reviewers**: Chỉ định người review phù hợp.
- **Kiểm tra kỹ trước khi merge** (kiểm tra xung đột, chạy test).

## 4. Quy tắc Rebase & Merge
- **Sử dụng `git pull --rebase` thay vì `git pull`** để giữ lịch sử commit gọn gàng.
- **Squash commit** khi merge nếu có quá nhiều commit nhỏ lẻ không cần thiết.
- **Không commit code trên branch `main` hoặc `develop` trực tiếp** (luôn tạo branch riêng).

## 5. Quy tắc Tag & Versioning
- **Tag phiên bản theo SemVer**: `v<MAJOR>.<MINOR>.<PATCH>`  
  *VD:* `v1.0.0`, `v2.3.1`
- **Dùng tag khi release bản mới**:  
  ```bash
  git tag -a v1.0.0 -m "First stable release"
  git push origin v1.0.0
  ```

## Tổng kết
 **Đặt tên branch có quy tắc**  
 **Viết commit message rõ ràng, có loại commit**  
 **Viết PR chi tiết, dễ review**  
 **Dùng rebase thay vì merge để giữ lịch sử sạch**  
 **Tag phiên bản khi release sản phẩm**  
