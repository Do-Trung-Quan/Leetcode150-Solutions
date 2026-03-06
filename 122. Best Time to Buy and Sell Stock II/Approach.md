# **Intuition**

**Yêu cầu: Được mua-bán nhiều lần và chỉ cần quan tâm profit giữa các lần trade**

=> Duyệt mảng và để ý nếu giá hôm nay

- thấp hơn hôm qua -> mua luôn
- cao hơn hôm qua-> bán luôn (không cần quan tâm hôm nào bán thì lời nhất)

# **Approach**

- Tạo biến lợi nhuận (pro = 0)
- Duyệt mảng:
    - Nếu giá hôm nay nhỏ hơn giá hôm qua (prices[i] < prices[i-1]) -> ko làm gì (mua)
    - Nếu giá hôm nay lớn hơn hôm qua (prices[i] > prices[i-1]) -> cập nhật pro += chênh lệch trade (bán)
- trả về pro

# **Complexity**

- Time complexity: O(n)
- Space complexity: O(1)
