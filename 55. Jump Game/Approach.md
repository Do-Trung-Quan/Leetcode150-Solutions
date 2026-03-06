# **Intuition**

**cập nhật độ vươn xa nhất khi đứng tại từng điểm trong mảng, nếu tại 1 điểm mà cách xa hơn maxReach -> false; còn nếu maxReach >= độ dài mảng-1 thì true**

# **Approach**

- Khởi tạo maxReach = 0
- Duyệt mảng:
    - Nếu vị trí hiện tại có index > maxReach (đang đứng xa hơn maxReach) => return false
    - Cập nhật maxReach = **max(maxReach, độ xa hiện tại(index i) + độ xa mà từ i nhảy tiếp được (nums[i]))**
    - Nếu maxReach đã lớn hơn hoặc bằng độ dài mảng - 1 => return true

# **Complexity**

- Time complexity: O(n)
- Space complexity: O(1)
