GIT
===========

Git là gì?
----------------
- Git là một **Hệ thống quản lý phân tán** (Distributed Version Control System) là hệ thống giúp mỗi máy tính có thể lưu trữ nhiều phiên bản khác nhau của một mã nguồn được clone từ một kho chứa mã nguồn (Repository). 
- Git giúp việc quản lý code và làm việc nhóm của developer trở nên đơn giản, thuận tiện hơn, linh hoạt hơn.
- Git có 3 trạng thái Working directory, Staging area và repository

Repository
----------
- Là nơi mà ta sẽ lưu trữ các file source code và mọi người có thể tạo clone từ mã nguồn đó để làm việc, tại đây sẽ lưu trữ lại tất cả thay đổi đã thực hiện(Commit).
- **Repository** có hai loại là **Local Repository** và **Remote Repository**
- Để tạo Repository tà dùng lệnh `git init`
- Để tạo clone từ Remote Repository ta dùng `git clone /path/to/repository`

HEAD
-----
- Trong Git, từ khóa HEAD sẽ tượng trưng cho con trỏ chỉ cho bạn biết bạn đang nằm ở đâu.

SnapShot
-------
- Là bản lưu trữ của tất cả tác động trong **Repository**(file, source code)


Branche
--------
- Branch là để phân nhánh và ghi lại luồng của lịch sử. Branch đã phân nhánh sẽ không ảnh hưởng đến branch khác nên có thể tiến hành nhiều thay đổi đồng thời trong cùng 1 repository.

- Branch đã phân nhánh có thể chỉnh sửa tổng hợp lại thành 1 branch bằng việc **Merge** với branch khác.

- Để tạo một Branch ta dùng: `git checkout -b <branchname>`
- Để chuyển sang một branch khác ta dùng: `git checkout <branchname>`
- Xóa branch:`git branch -d <branchname>`
- merge branch: `git merge <branchname>`
### Branche master
- Khi tiến hành commit lần đầu trong repository thì Git sẽ tạo ra một branch có tên là master. Vì thế những lần commit sau sẽ được thêm vào branch master cho đến khi chuyển đổi branch.

Commit
--------
- Mỗi Commit sẽ tạo ra 1 **Snapshot**
- Gồm các thông tin về những file được thay đổi, thông tin về parent commit(nếu có) và 1 hashcode để lưu trữ name
Câu lệnh: `git commit -m "message"`
Để xem lịch sử commit: `git log` hoặc dùng `git diff` để xem chi tiết những thay đổi

Git Rebase
-------
- Git Rebase là một chức năng được dùng khi gắn nhánh đã hoàn thành công việc vào nhánh gốc, chính vì thế sẽ có đặc trưng là dễ nhìn hơn sau khi xác nhận commit.
- Câu lệnh: `git rebase <branche>`

Các câu lệnh git khác
----------------
- `git status`: Để xem những file nào đã bị thay đổi
- `git push`: Những thay đổi ở phía local và được đẩy lên remote
- `git pull`:Fetch và Merge những thay đổi trên remote để cập nhật local repository đồng thời sẽ báo những file bị conflict(nếu có)
- `git add <filename>`: Thêm 1 hoặc nhiều file vào staging (index)
```
git config --global user.name "Sam Smith"
git config --global user.email sam@example.com
```
- `global` được sử dụng để áp dụng cho tất cả các projects. Nếu bạn ko sử dụng `--global` thì settings sẽ chỉ dùng cho riêng project đó.
-`git commit --amend`: Để ghi đè lại commit mới nhất Nếu bạn chỉ muốn add thêm file mà không muốn sửa commit message thi có thể dùng option `--no-edit`
- `git blame`: Để xác định ai là người gây ra lỗi