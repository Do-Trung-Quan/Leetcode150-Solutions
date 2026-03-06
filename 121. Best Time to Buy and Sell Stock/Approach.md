# **Intuition**

**Sử dụng 2 con trỏ lưu ngày dự định mua và ngày hiện đang xét, duyệt dần về cuối mảng để cập nhật lợi nhuận lớn nhất**

# **Approach**

- Tạo biến pro = 0 lưu lợi nhuận lớn nhất, biến buy = 0 lưu ngày dự định mua
- Duyệt mảng từ i = 1:
    - Nếu giá ngày đang xét < giá ngày mua -> cập nhật buy = i (đổi sang mua hôm đang xét)
    - Else -> cập nhật pro = max(pro, chênh lệch giá ngày mua và ngày đang xét)
- trả về pro

# **Complexity**

- Time complexity: O(n)
- Space complexity: O(1)
