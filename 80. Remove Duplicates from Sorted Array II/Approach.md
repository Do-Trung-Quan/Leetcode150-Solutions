# **Intuition**

Sử dụng phương pháp 2 con trỏ, đưa các phần tử không lặp quá 2 lần về hết bên trái, cần 1 biến check xem phần tử trước đó có đang lặp lại 2 lần chưa để không cho phép lặp lại lần nữa khi duyệt vòng for

# **Approach**

- **Tạo biến và 2 con trỏ:**
    - con trỏ p = 1: thể hiện vị trí có thể đưa phần tử tại index đang xét vào nếu thỏa mãn đk
    - con trỏ i = 1: thể hiện index của phần tử đang xét khi duyệt vòng for
    - biến check lặp dup = 0: thể hiện trạng thái của phần tử được thêm gần nhất có đang lặp lại ptu trước đó hay không
- **Xử lý vòng for trên mảng nums:**
    - Nếu phần tử trước p (nums[p-1]) khác phần tử đang xét (nums[i]): cập nhật nums[p] = nums[i], p++, dup = 0;
    - Nếu phần tử trước p (nums[p-1]) bằng phần tử đang xét (nums[i]) và phần tử trước p chưa bị lặp lại: cập nhật nums[p] = nums[i], p++, dup = 1
- **Trả về p là số phần tử được giữ lại và mảng nums đã thỏa mãn db**

# **Complexity**

- Time complexity: O(n) với n là độ dài của nums
- Space complexity: O(1)
