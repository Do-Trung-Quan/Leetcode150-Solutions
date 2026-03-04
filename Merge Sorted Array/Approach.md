1. Hướng tiếp cận (Approach)
sử dụng kỹ thuật Hai con trỏ (Two Pointers) duyệt ngược từ cuối mảng
Thay vì trộn từ đầu mảng (sẽ gây rủi ro ghi đè mất dữ liệu của nums1 và tốn thêm bộ nhớ đệm), em tận dụng khoảng trống có sẵn ở cuối nums1. Việc so sánh và điền các số lớn nhất từ cuối lên đầu giúp giải quyết bài toán In-place (ngay trên mảng gốc) một cách an toàn.

2. Giải thích Logic (Logic Execution)
Em sẽ khởi tạo 3 con trỏ:

p1 = m - 1: Trỏ vào phần tử hợp lệ lớn nhất (cuối cùng) của nums1.

p2 = n - 1: Trỏ vào phần tử lớn nhất (cuối cùng) của nums2.

i = nums1.length - 1: Trỏ vào vị trí cuối cùng của mảng nums1, nơi trống để điền dữ liệu.

Tiến hành dùng vòng lặp for chạy i lùi dần về 0:

Điều kiện dừng sớm: Nếu p2 < 0, nghĩa là toàn bộ mảng nums2 đã được ghép xong. Em gọi break để thoát vòng lặp ngay lập tức vì phần còn lại của nums1 vốn dĩ đã được sắp xếp sẵn.

Xử lý ghép mảng: Em kiểm tra nếu p1 < 0 (đã cạn phần tử ở nums1) hoặc phần tử nums2[p2] lớn hơn nums1[p1], em sẽ bốc nums2[p2] điền vào nums1[i] và lùi con trỏ p2.

Trường hợp còn lại: Nếu nums1[p1] lớn hơn hoặc bằng, em điền nums1[p1] vào nums1[i] và lùi con trỏ p1.

3. Độ phức tạp thuật toán (Complexity Analysis)
Độ phức tạp thời gian (Time Complexity): O(m + n). Em duyệt qua các phần tử của cả hai mảng tối đa đúng một lần. Vòng lặp chạy nhiều nhất là m + n bước.

Độ phức tạp không gian (Space Complexity): O(1). Em thao tác trực tiếp trên mảng nums1 đầu vào, chỉ sử dụng thêm 3 biến con trỏ kiểu số nguyên nên không tiêu tốn thêm bộ nhớ phụ trợ.
