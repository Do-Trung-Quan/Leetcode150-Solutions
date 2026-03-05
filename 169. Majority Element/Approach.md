# **Intuition**

Khởi tạo 2 biến tracking khi duyệt mảng nums: 1 biến lưu phần tử major hiện tại, 1 biến lưu độ áp đảo của phần tử major hiện tại.

Duyệt và cập nhật dần major element dựa trên biến độ áp đảo và trả về major element cuối cùng.

# **Approach**

- **Tạo 2 biến tracking:**
    - res: lưu major element hiện tại khi xét vòng lặp for
    - app: lưu độ áp đảo của res hiện tại khi xét vòng for
    
    VD: [2,2,3,3,2],
    
    - tại index = 2 -> res = 2 (vì đã xuất hiện 2 lần); app = 1 (vì 2 lần xuất hiện - 1 lần xuất hiện của 3 = 1)
    - tại index = 4 -> res = 2 (vì đã xuất hiện 3 lần); app = 1 (vì 3 lần xuất hiện - 2 lần xuất hiện của 3 = 1)
- **Xử lý vòng lặp for trên mảng nums:**
    - Nếu độ áp đảo hiện tại đang cân bằng (app == 0) -> gán luôn res = phần tử đang xét hiện tại (res = nums[i])
    - Nếu res khác phần tử đang xét (res != nums[i]) -> cập nhật độ áp đảo của res giảm 1 đơn vị (app--)
    - Nếu res bằng phần tử đang xét (res == nums[i]) -> cập nhật độ áp đảo của res cộng 1 đơn vị (app++)
- **Vì đề bài đảm bảo luôn có major element cuối cùng -> luôn trả về res thỏa mãn db khi duyệt xong mảng nums**

# **Complexity**

- Time complexity: O(n) với n là độ dài nums
- Space complexity: O(1)
