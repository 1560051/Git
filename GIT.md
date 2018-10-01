GIT
===========

Git là gì?
----------------
- Git là một **Hệ thống quản lý phân tán** (Distributed Version Control System) là hệ thống giúp mỗi máy tính có thể lưu trữ nhiều phiên bản khác nhau của một mã nguồn được clone từ một kho chứa mã nguồn (Repository). 
- Git giúp việc quản lý code và làm việc nhóm của developer trở nên đơn giản, thuận tiện hơn, linh hoạt hơn.

Repository
----------
- Là nơi mà ta sẽ lưu trữ các file source code và mọi người có thể tạo clone từ mã nguồn đó để làm việc, tại đây sẽ lưu trữ lại tất cả thay đổi đã thực hiện(Commit).
- **Repository** có hai loại là **Local Repository** và **Remote Repository**
- Để tạo Repository tà dùng lệnh `git init`
- Để tạo clone từ Remote Repository ta dùng `git clone /path/to/repository`

SnapShot
-------
- Là bản lưu trữ của tất cả tác động trong **Repository**(file, source code)

Commit
--------
- Mỗi Commit sẽ tạo ra 1 **Snapshot**
- Gồm các thông tin về những file được thay đổi, thông tin về parent commit(nếu có) và 1 hashcode để lưu trữ name
Câu lệnh: `git commit -m "message"` 
Để xem lịch sử commit: `git log` hoặc dùng `git diff` để xem chi tiết những thay đổi

Branche
--------
- Branch là để phân nhánh và ghi lại luồng của lịch sử. Branch đã phân nhánh sẽ không ảnh hưởng đến branch khác nên có thể tiến hành nhiều thay đổi đồng thời trong cùng 1 repository.

- Branch đã phân nhánh có thể chỉnh sửa tổng hợp lại thành 1 branch bằng việc **Merge** với branch khác.

###Branche master
- Khi tiến hành commit lần đầu trong repository thì Git sẽ tạo ra một branch có tên là master. Vì thế những lần commit sau sẽ được thêm vào branch master cho đến khi chuyển đổi branch.