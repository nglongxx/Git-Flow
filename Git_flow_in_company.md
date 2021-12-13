GIT - CÁC LỆNH ĐƯỢC DÙNG TỪ LÚC NHẬN TASK CHO TỚI LÚC TẠO PR 🎉
0. Nhận task, ví dụ ở đây task có id là 123
Tí nữa, đọc thấy tạo nhánh có số 123 thì các bạn hiểu ngầm nó chính là taskId nhen.
Ví dụ team mình dev trên nhánh develop.
1. Lấy code mới nhất trên branch develop
git checkout develop # switch sang nhánh develop

git pull # lấy code mới nhất về
2. Làm task trực tiếp trên nhánh develop
CODING CHANGES 😎
Sau khi code xong, nhờ review lại những thay đổi của mình, review cẩn thận, từ từ.
Review về coding convention.
Review về console log đã xoá chưa?
Review về imports (có dư thừa gì ko?)
Review về eslints
Review xem chỗ nào logic phức tạp nên add thêm comment vào.
Review xem chỗ nào code nhiều if/else quá thì refactor lại.
...
Review bằng VSCode hen, cho nó dễ nhìn, còn bạn muốn cool ngầu thì cứ git diff và check nhé! 😎
Hãy tập thói quen review code của bản thân cẩn thận trước khi đưa cho lead review nhé! 😉

3. Chuẩn bị tạo Pull Request (PR)
Sau khi đã code xong, giờ chuẩn bị tạo PR
Nhưng có thể trong lúc mình làm, ai đó đã update thêm lên nhánh develop rồi.
Nên mình phải lấy code mới nhất trên nhánh develop rồi mới apply cái changes của mình.

git add . # chấp nhận tất cả changes

git stash # save tất cả code changes vào stash (kiểu nơi giữ code tạm)

git pull  # lấy code mới nhất về
4. Tạo nhánh cho code changes của mình
git checkout -b feature/123-add-address-ui
5. Lấy code từ trong stash ra (hùi nảy lưu bằng git stash)
git stash pop
OPTIONAL: resolve conflicts nếu có, nhớ test lại để đảm bảo code còn chạy ngon 😅

6. Tạo commit, viết commit message
git status # xem các files thay đổi
git add . # chấp nhận tất cả thay đổi

git commit -m "[123] Add address ui

- More details about your PR
- Keep it short and descriptive"
📝Lưu ý chỗ chữ màu vàng
- Dòng đầu tiên là title
- Dòng thứ 2 là empty ( BẮT BUỘC )
- Dòng thứ 3 trở đi là dòng mô tả thêm về Pull Request của mình.
Convention này nó giúp bạn tự động điền title, description vào ô tương ứng trên Github, Gitlab, Bitbucket, ...

7. Push code lên remote repository (Github, Gitlab, Bitbucket, ...)
git push -u origin feature/123-address-ui 
Cuối cùng, lên remote repo tạo PR/MR vào nhánh develop. Xong nhờ lead review thôi hehe
📝LƯU Ý

Tuỳ dự án sẽ có quy định tên nhánh khác nhau, nhớ follow theo team.
Làm việc trên nhánh nào cũng tuỳ team, ko phải lúc nào cũng là develop.
Không phải ai cũng apply cái process này giống mình, mỗi người mỗi kiểu.
Ở trên là process, mình đi làm thấy nó tốt và đã apply suốt thời gian qua, thấy hiệu quả nên chia sẻ lại cho mọi người nè, mọi người đọc tham khảo, thấy hay thì có thể vận dụng nhen 😉
CHÚC CẢ NHÀ SỨC KHOẺ VÀ HỌC TẬP TỐT NHÉ! ❤️
