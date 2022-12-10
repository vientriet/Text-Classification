# Sentiment Analysis
Phân tích cảm xúc văn bản (Sentiment Analysis) thuộc nhóm bài toán phân loại văn bản. Đầu vào là đơn vị văn bản: từ, cụm từ, câu, đoạn, văn bản,... Với mục tiêu đầu ra xem xét các bình luận là tích cực hay tiêu cực về một sản phẩm hay đối tượng nào đó.

Việc phân tích cảm xúc trong văn bản được ứng dụng trong hàng loạt các vấn đề như: Quản trị thương hiệu doanh nghiệp, thương hiệu sản phẩm, quản trị quan hệ khách hàng, khảo sát ý kiến xã hội học, phân tích trạng thái tâm lý con người...

Bài toán phân tích cảm xúc có nhiều hướng tiếp cận khác nhau. Trong project này tập trung vào hai hướng chính: sử dụng naive bayes và logistic regression. Bộ dữ liệu sử dụng là các bình luận trên tweets.
# Sentiment Analysis using Naive Bayes Classifier
Thuật toán Naive Bayes Classifier ứng dụng cho phân tích cảm xúc (hay phân loại văn bản) được mô tả như sau:

Thuật toán mô tả gồm 2 phần:
- Huấn luyện mô hình: Xây dựng bộ từ điển tần suất xuấn hiện của các từ theo các class. Sau đó tính xác xuất tiên nghiệm và xác suất likelihood. Phương pháp trích chọn đặc trưng để biểu diễn văn bản là túi các từ - Bow (Bag-of-words).

Phương pháp BoW giúp mã hóa (biểu diễn) các văn bản thành các đặc trưng là tần suất xuất hiện của các từ trong văn bản dựa vào bộ từ điển.
- Dự đoán mô hình: Với các dữ liệu kiểm thử. Tính xác suất của các class và chọn ra class có xác suất cao nhất.
# Sentiment Analysis using Logistic Regression
Thuật toán Logistic Regression sử dụng hàm sigmoid để tìm ra mối quan hệ giữa các đặc trưng. Trong bài toán phân loại nhị phân (phân tích cảm xúc với đầu ra hai lớp: tích cực và tiêu cực).

Trong đó phương pháp trích chọn đặc trưng để biểu diễn văn bản thành các vector là các đặc trưng thống kê dựa vào bộ từ điển tần suất xuất hiện các từ.

Gồm 2 đặc trưng:
- Đặc trưng thứ nhất: Tổng tần suất xuất hiện các từ là tích cực (positive) trong văn bản.
- Đặc trưng thứ hai: Tổng tần suất xuất hiện các từ là tiêu cực (negative) trong văn bản.

Sau khi trích xuất đặc trưng của các văn bản chúng ta áp dụng huấn luyện mô hình logistic regression để phân loại nhị phân với ngưỡng là 0.5.
