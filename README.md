# Thuat-Toan-Me-Cung
Một Số Thuật Toán Giải Mã Mê Cung

# 1. Thuật Toán Dijkstra

BẮT ĐẦU
    CHỌN đỉnh bắt đầu S
    GÁN khoảng cách[S] = 0
    GÁN khoảng cách[v] = vô cùng với mọi đỉnh v khác S

    TẠO danh sách chưa xử lý Q gồm tất cả các đỉnh

    KHI Q không rỗng THÌ
        u = đỉnh có khoảng cách nhỏ nhất trong Q
        LOẠI BỎ u khỏi Q
        
        NẾU u là đỉnh đích T THÌ
            TRẢ về khoảng cách[T]
        
        CHO MỌI đỉnh v kề với u THÌ
            alt = khoảng cách[u] + trọng số(u, v)
            NẾU alt < khoảng cách[v] THÌ
                khoảng cách[v] = alt
                tiền tố[v] = u

    KẾT THÚC KHI
KẾT THÚC
# 2. Thuật Toán A*

BẮT ĐẦU
    CHỌN đỉnh bắt đầu S và đỉnh đích T
    GÁN khoảng cách[S] = 0
    GÁN khoảng cách[v] = vô cùng với mọi đỉnh v khác S

    TẠO danh sách mở O gồm S
    TẠO danh sách đóng C rỗng

    KHI O không rỗng THÌ
        u = đỉnh có giá trị f(u) nhỏ nhất trong O
        NẾU u là T THÌ
            TRẢ về đường đi từ S đến T
        
        LOẠI BỎ u khỏi O
        THÊM u vào C
        
        CHO MỌI đỉnh v kề với u THÌ
            NẾU v đã có trong C THÌ
                TIẾP TỤC
            
            alt = khoảng cách[u] + trọng số(u, v)
            NẾU v không có trong O THÌ
                THÊM v vào O
            
            NẾU alt < khoảng cách[v] THÌ
                khoảng cách[v] = alt
                tiền tố[v] = u

    KẾT THÚC KHI
KẾT THÚC
# 3. Thuật Toán PID

BẮT ĐẦU
    GÁN Kp, Ki, Kd là các hằng số điều chỉnh
    GÁN previous_error = 0
    GÁN integral = 0
    
    KHI (có dữ liệu đầu vào) THÌ
        error = giá trị mục tiêu - giá trị hiện tại
        integral += error
        derivative = error - previous_error
        
        output = Kp * error + Ki * integral + Kd * derivative
        
        THỰC HIỆN hành động với output

        previous_error = error
    KẾT THÚC KHI
KẾT THÚC
# 4. Thuật Toán SLAM

BẮT ĐẦU
    KHỞI TẠO bản đồ và vị trí robot
    KHI (robot đang hoạt động) THÌ
        ĐỌC dữ liệu từ cảm biến
        CẬP NHẬT vị trí robot
        CẬP NHẬT bản đồ
    KẾT THÚC KHI
KẾT THÚC
# 5. Thuật Toán Genetic

BẮT ĐẦU
    KHỞI TẠO quần thể ban đầu
    KHI (điều kiện dừng không đạt) THÌ
        TẠO các cá thể mới bằng cách lai ghép
        ĐÁNH GIÁ từng cá thể trong quần thể
        CHỌN các cá thể tốt nhất cho thế hệ tiếp theo
    KẾT THÚC KHI
KẾT THÚC
# 6. Thuật Toán Bám Đường

BẮT ĐẦU
    KHI (robot chưa đến đích) THÌ
        ĐỌC dữ liệu từ cảm biến
        NẾU cảm biến phát hiện đường THÌ
            DI CHUYỂN THẲNG
        NẾU không THÌ
            QUAY TRÁI hoặc PHẢI tùy theo vị trí của đường
    KẾT THÚC KHI
KẾT THÚC
# 7. Thuật Toán Fuzzy Logic

BẮT ĐẦU
    KHỞI TẠO các luật fuzzy
    KHI (robot đang hoạt động) THÌ
        ĐỌC dữ liệu cảm biến
        ÁP DỤNG luật fuzzy để tính toán đầu ra
        THỰC HIỆN hành động dựa trên đầu ra
    KẾT THÚC KHI
KẾT THÚC
# 8. Thuật Toán K-Means

BẮT ĐẦU
    KHỞI TẠO số cụm k và vị trí ngẫu nhiên cho các tâm cụm
    KHI (các tâm cụm không thay đổi) THÌ
        Gán mỗi điểm dữ liệu vào cụm gần nhất
        CẬP NHẬT tâm cụm dựa trên các điểm được gán
    KẾT THÚC KHI
KẾT THÚC
# 9. Thuật Toán Backtracking

BẮT ĐẦU
    CHỨC NĂNG backtrack(dữ liệu, điều kiện) THÌ
        NẾU (điều kiện đạt) THÌ
            TRẢ VỀ giải pháp
        KHOẢNG CÁCH TỪ MỚI
        CHO MỌI lựa chọn có thể THÌ
            LỰA CHỌN = lựa chọn hiện tại
            NẾU backtrack(dữ liệu, điều kiện) THÌ
                TRẢ VỀ giải pháp
        KẾT THÚC CHO
    KẾT THÚC
KẾT THÚC
# 10. Thuật Toán Reinforcement Learning

BẮT ĐẦU
    KHỞI TẠO trạng thái ban đầu
    KHI (không đến trạng thái cuối) THÌ
        CHỌN hành động theo chính sách hiện tại
        THỰC HIỆN hành động và nhận phần thưởng
        CẬP NHẬT giá trị trạng thái theo phần thưởng
        CẬP NHẬT chính sách
    KẾT THÚC KHI
KẾT THÚC
# 11. Thuật Toán RRT

BẮT ĐẦU
    KHỞI TẠO RRT với đỉnh bắt đầu S
    KHI (không đến đỉnh đích T) THÌ
        TẠO một điểm ngẫu nhiên trong không gian
        Tìm đỉnh gần nhất trong RRT
        Mở rộng RRT về phía điểm ngẫu nhiên
        THÊM đỉnh mới vào RRT
    KẾT THÚC KHI
KẾT THÚC
