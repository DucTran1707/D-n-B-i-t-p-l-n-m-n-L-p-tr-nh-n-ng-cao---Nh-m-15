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


auction-client/
├── pom.xml (hoặc build.gradle)      <-- File cấu hình thư viện (JavaFX, thư viện vẽ biểu đồ)
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/auction/client/
│   │   │       ├── ClientMain.java  <-- Khởi tạo ứng dụng JavaFX (kế thừa Application)
│   │   │       ├── network/         <-- Lớp quản lý kết nối Socket Client/gọi REST API tới Server
│   │   │       ├── controller/      <-- Chứa các JavaFX Controller (xử lý sự kiện click nút, nhập text)
│   │   │       └── model/           <-- Các class hứng dữ liệu (JSON) trả về từ Server
│   │   └── resources/
│   │       ├── fxml/                <-- Chứa các file giao diện (.fxml) vẽ bằng SceneBuilder
│   │       │   ├── LoginView.fxml
│   │       │   ├── AuctionListView.fxml
│   │       │   └── BiddingView.fxml
│   │       ├── css/                 <-- File style (.css) để làm đẹp giao diện
│   │       └── images/              <-- Hình ảnh minh họa (icon, ảnh sản phẩm mặc định)