# Hướng dẫn cách chạy
DATABASE:
1) truy cập firebase console -> tạo project mới
2) vào Authentication, add email/password và xác nhận
3) vào firestore database -> tạo database -> tạo index với 2 path fields là UserId (ascending) và Timestamp (decending)
4) vào project settings -> add web -> lấy mã api key -> chuyển mục service accounts generate new private key( chọn Python) trong Admin SDK configuration snippet
   -> được file your_firebase_key.json và mã API Key
   <br>

COLAB:
1) tạo tài khoản colab 
2) mở notebook là file notebook jupiter (source code)
3) chuyển Runtime type sang gpu
4) upload your_firebase_key.json vào notebook
   <br>
   
SOURCE CODE:
1) chạy lần lượt các cell:
   + cell 1 để install các công cụ cần thiết
   + cell 2 thiết lập ollama
   + cell 3 install mistral và tạo cổng api cloudflare -> chạy xong nhận được một URL
   + cell 4 app.py phụ trách các hàm và gửi search Request
     * copy URL của cell 3 vào OLLAMA_URL
     * copy API Key lấy được từ bước 4 trong database vào FIREBASE_API_KEY
     * các chỗ firebase.json, đổi tên file your_firebase_key.json cho trùng khớp với các chỗ
   + cell 5 khởi động streamlit, nhấp url đích dẫn tới trang streamlit và test
     


