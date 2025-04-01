# Các miền chức năng của xe và yêu cầu của chúng

## 1.1 Bối cảnh chung

Ngành công nghiệp ô tô hiện nay đóng vai trò quan trọng vào doanh thu trên thế giới. Vì thế lĩnh vực Embedded Electronics và Embedded Software đã trở nên rất nóng trong mảng nghiên cứu về xe hơi. Những xu hướng chung này đã dẫn đến việc hiện nay có thể nhúng tới nhiều MB dữ liệu trên hơn nhiều vi xử lý được kết nối trong các mạng truyền thông.

Công nghệ điện tử đã tạo ra những bước tiến lớn về chất lượng của các linh kiện điện tử như hiệu suất, độ bền và độ tin cậy. Hơn nữa, một số automotive-embedded network được phát triển như LIN, CAN, TTP/C, FlexRay, MOST, and IDB-1394.

Một lý do công nghệ khác cho sự gia tăng của các hệ thống nhúng ô tô là thực tế các công nghệ phần cứng và phần mềm mới tạo sự phát triển cho các chức năng của xe mà ít tốn kém hơn hoặc không khả thi nếu chỉ sử dụng công nghệ cơ khí. Do đó, chúng đáp ứng các yêu cầu của người dùng cuối về độ an toàn, sự tiện lợi và chi phí. Ví dụ như động cơ điện tử, phanh ABS, ESP,...

Nói tóm lại, nhờ những công nghệ này, khách hàng có thể mua một chiếc xe an toàn, hiệu quả và được cá nhân hóa, trong khi các nhà sản xuất ô tô có thể nắm vững sự khác biệt giữa các biến thể sản phẩm và đổi mới.

Các ứng dụng đa phương tiện và viễn thông trên ô tô đang tăng nhanh do nhu cầu của người tiêu dùng. Ví dụ như các thiết bị giải trí, thiết bị âm thanh / radio, hệ thống định vị. Tóm lại các hệ thống điện tử tiến bộ vô hạn, áp lực lớn nhất của thiết bị điện tử là chi phí.

Cuộc cách mạng điện tử liên tục phát triển mang lại hai tín hiệu tích cực chính. Đầu tiên là dành cho người dùng, những người yêu cầu tăng hiệu suất, sự tiện lợi, hiệu quả trong việc di chuyển, an toàn và ít tốn chi phí nhiên liệu. Tín hiệu tích cực thứ hai là đối với sự phát triển, nghiên cứu công nghệ dựa trên phần mềm của các các nhà sản xuất ô tô và nhà cung cấp.

Tuy nhiên có một thách thức đó chính là sự cố hỏng hóc trong các hệ thống điện tử. Do đó, việc phát triển và sản xuất chúng cần dựa trên một phương pháp phù hợp, bao gồm mô hình hóa, đánh giá và xác nhận tiên nghiệm và thử nghiệm.

Các hệ thống nhúng trong xe thường được phân loại theo các miền tương ứng với các chức năng, ràng buộc và mô hình khác nhau.

## 1.2 Miền chức năng

Các nhà sản xuất ô tô phân biệt một số miền cho các thiết bị điện tử nhúng trong ô tô, mặc dù đôi khi một miền chỉ là một chức năng. Theo bảng thuật ngữ của dự án ITEA EAST-EEA, một miền được định nghĩa là "một phạm vi kiến thức, ảnh hưởng và hoạt động trong đó một hoặc nhiều hệ thống sẽ được xử lý. Thuật ngữ miền có thể được sử dụng như một phương tiện để nhóm các hệ thống cơ khí và điện tử.

Trong lịch sử, 5 miền được xác định là: hệ thống truyền lực, khung gầm, thân xe, HMI và viễn thông. Hệ thống truyền lực có liên quan đến hệ thống tham gia vào động cơ đẩy dọc của xe bao gồm động cơ, hộp số và các thành phần phụ khác. Miền khung gầm bao gồm 4 bánh xe và vị trí chuyển động tương đối của chúng. Theo định nghĩa của EAST-EEA, miền thân xe bao gồm các thực thể không thuộc động lực học của xe chẳng hạn như túi khí, cần gạt nước, đèn chiếu sáng, bộ nâng cửa sổ, điều hòa không khí, thiết bị ghế, v.v. Miền HMI bao gồm thiết bị cho phép trao đổi thông tin giữa các hệ thống điện tử và trình điều khiển (màn hình và công tắc). Cuối cùng, miền viễn thông có liên quan đến các thành phần cho phép trao đổi thông tin giữa xe và thế giới bên ngoài như radio, hệ thống định vị, truy cập Internet, v.v.

### 1.2.1 Miền hệ thống truyền động

Miền này đại diện cho hệ thống điều khiển động cơ từ người lái xe và các yêu cầu từ các bộ phận khác của hệ thống nhúng như climate control, ESP...

Miền này được thiết kế để tối ưu hóa các thông số nhất định "certain parameters" như mức tiêu thụ nhiên liệu, sự tiện lợi khi lái xe... Một parameter có thể được kiểm soát bởi một hệ thống như là lượng nhiên liệu phải được phun vào mỗi xi lanh ở mỗi chu kỳ động cơ theo số vòng quay mỗi phút (RPM) của động cơ và vị trí của bàn đạp ga.

Các đặc điểm chính của các hệ thống nhúng của miền hệ thống truyền lực là:
- Từ quan điểm chức năng: Điều khiển hệ thống truyền lực có tính đến các chế độ làm việc khác nhau của động cơ.
- Từ quan điểm phần cứng: Miền này yêu cầu các cảm biến có thông số kỹ thuật phải xem xét việc giảm thiểu các tiêu chí chi phí.
- Từ quan điểm thực hiện: Các chức năng được chỉ định được thực hiện dưới dạng một số nhiệm vụ với các quy tắc kích hoạt khác nhau theo quy tắc lấy mẫu, với các hạn chế nghiêm ngặt về thời gian được áp dụng đối với việc lập lịch tác vụ, làm chủ giao tiếp an toàn với các hệ thống khác và với các cảm biến hoặc bộ truyền động cục bộ.

### 1.2.2 Miền khung gầm