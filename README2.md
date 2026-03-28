auction-server/
├── pom.xml (hoặc build.gradle)      <-- File cấu hình thư viện (JDBC, JSON, JUnit)
├── src/
│   ├── main/
│   │   └── java/
│   │       └── com/auction/server/
│   │           ├── ServerMain.java  <-- File chạy server chính
│   │           ├── network/         <-- Lớp quản lý Socket Server hoặc REST API endpoint
│   │           ├── controller/      <-- Xử lý request từ Client (nhận Bid, tạo User, update Item)
│   │           ├── model/           <-- Chứa các class Entity cốt lõi (User, Item, Auction, BidTransaction)
│   │           ├── dao/             <-- Chứa logic truy xuất Database (Data Access Object)
│   │           └── util/            <-- Các class tiện ích (Singleton kết nối DB, mã hóa mật khẩu)
│   └── test/
│       └── java/
│           └── com/auction/server/  <-- Chứa các file JUnit test cho logic quan trọng (ví dụ: test placeBid)