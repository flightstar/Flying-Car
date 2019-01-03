## Giới thiệu 
![](https://lh3.googleusercontent.com/odqXB6YeHJ0aBEX8RdEpAXkYL2oyOXfNSo2Tnjl5QMcx_seanjVbmouyG9j3RlZC2qjL33WXsS8cJN9mViD8gTa5iAZvK18CDm_74kZL5yIkz0jkAAFHXrYxViowu9bN6yNxols7JH4l9keHlIObDClRNogtvPhfXLUUWaqcVBdl3TU7kvIwRCRyEJYMbTBgtub1VC3wnRY1j9UTqdO1CVLB1gJBy1ToxCeJgRFwDIaIEeSaMbU2Wlo-F3FRPsFVEX7uXwNsd4c2AVonUNozBDI5qPlJVC6eDillZEt4xfW1Y0FsmOI-5psFxYj4Jp9TSmY8sxb43D-hKjB_DMfsHRbNyBup6sDtETS3HuCV0ccaHcViUYkZEiSaliCouE0QNkL0bQndwEFpJZTzFKpXWYEMVKOy9mBUKUAUAYeMN3sp-o7WYWiQoSFSR-UxmGn-c0R6qi65UTi8RC7Qouq3yU9Gc-uAoXC4RJKW4PNB1_walggPmcULWwBhzFuNq93LQZywcck7EJCKVxN7KL6W8dR_Bud-TG0YDeQtcN3j6dHp-OaEfbiwCibO3u7DI6BPaz3kTBiXl6woc4dPJVhc2jAbOSguQiTbi2G9S2rz9xMgGjjwvtqe2BHzTnY4tUlvq7hSpLBc9e9Nf_kUpok-V8QmSLebNs3Eab5J3H4BvMyLxmTWry28cO77LdkpxAi1BWe9vE-XfDAVZK6ZUw=w479-h269-no)

Tại phần đầu tiên, tôi sẽ nói về cách lập trình máy bay không người lái bằng code Python và test flight simulator. 

Thị trường máy bay không người lái hay còn được gọi là Drone ngày càng phát triển một cách ghê gớm trên toàn Thế giới. Drone được sử dụng rất nhiều trong an ninh quốc phòng, tìm kiếm vật liệu hóa chất, tìm người lạc, nông nghiệp có thể chăm sóc cây trồng, điện ảnh cho những khung cảnh trên cao vời vợi, giao vận,...

Phương tiện bay không người lái hay Máy bay không người lái, viết tắt tiếng Anh là UAV (Unmanned aerial vehicle) là **tên gọi chỉ chung cho các loại máy bay mà không có người lái ở buồng lái, hoạt động tự lập và thường được điều khiển từ xa từ trung tâm hay máy điều khiển.** Theo sự phát triển công nghệ hiện có các dạng UAV:

+ **Máy bay theo nghĩa truyền thống được trang bị hệ thống điều khiển và lái tự động**, được gọi là UAS (unmanned aircraft system) 
+ **Phương tiện bay kiểu mới**, được chế tạo rất đa dạng, **có kích thước và công suất động cơ nhỏ đến trung bình, được gọi là drone.**
+ **Các drone có lắp camera để quan sát, và thường được gọi là flycam. Để thuận tiện điều khiển thao tác thì drone có nhiều cánh quạt, thường là 4.**

Có nhiều hãng sản xuất thiết bị không người lái và bạn có thể lập trình phát triển trên mobile, tablet, ứng dụng desktop:
+ [DJI](http://developer.dji.com/)
+ [Parrot](https://developer.parrot.com/index.html)
+ [Flytbase](https://flytbase.com/flytos/)
+ [DroneDeploy](https://www.dronedeploy.com/)
+ [DroneKit](http://dronekit.io/)

Một số hệ điều hành đã từng sử dụng trong hệ thống tên lửa, quý bạn cũng có thể đọc thêm: Zephyr OS, gOS, IBM System/360, SunOS, HP-UX, AIX, Irix systems,... để cho quý bạn phát triển vi mạch điều khiển cho hệ thống nhúng. 

Tôi cũng xin phép giới thiệu sơ qua các loại máy bay:
+ Lighter-than-air aircraft
  
  Đề cập đến các vật liệu (thường là khí) nổi trong không khí vì chúng có mật độ trung bình thấp hơn không khí. Không khí khô có mật độ khoảng 1,29 g / L (gram mỗi lít) ở điều kiện tiêu chuẩn về nhiệt độ và áp suất (STP) và khối lượng phân tử trung bình là 28,97 g / mol (do 78% Nitơ, 21% Oxi, 1% là khí khác)
  
  Bất kỳ khí nào có khối lượng phân tử dưới 29 như Neon, hơi nước, metan, amoniac, Hydrogen, helium,... đều nhẹ hơn không khí

  ![](https://cdn.britannica.com/s:700x450/30/91830-004-5560E6CB.jpg)
 
  Một số loại phương tiện bay nhẹ hơn không khí như các loại khí cầu.
  
+ Heavier-than-air aircraft

  ![](https://cdn.britannica.com/s:700x450/11/129811-004-9D34C115.jpg)
  
  Là loại máy bay phải sử dụng nguồn năng lượng để cung cấp lực đẩy cần thiết để có được lực nâng. Ví dụ về thiết bị bay nặng hơn không khí như diều, máy bay không người lái, tàu lượn bay (hang-gliding), trực thăng,...
  ![](https://cdn.britannica.com/s:700x450/63/100263-004-8F5C54B4.jpg)
+ Civil aircraft
  
  Tất cả các máy bay phi quân sự là máy bay dân dụng. Chúng bao gồm máy bay tư nhân và kinh doanh và máy bay thương mại.
  
  ![](https://cdn.britannica.com/s:700x450/44/93544-004-A211D18D.jpg)
  
  Hai cánh và ở giữa hai hai cánh (nơi giữa thân máy bay) để chứa xăng máy bay. Người ta thường bơm xăng vào hai cánh trước rồi mới thân giữa.
  Đôi cánh chính là nơi nâng toàn bộ máy bay trên không. Có các loại cánh máy bay:
  + Fixed-wing Aircraft (Máy bay cánh cố định)
    
    Là một loại máy bay có khả năng bay bằng cách sử dụng cánh tạo ra lực nâng được tạo ra bởi sự chuyển dịch về phía trước nhờ động cơ đẩy và hình dạng của cánh máy bay.

    ![](http://images.policemag.com/articles/M-Beechcraft-2014-Baron-ISR-A2A-sz.jpg)
    
  + Rotary-wing Aircraft (Máy bay lên thẳng)
    Là một loại phương tiện bay có động cơ, hoạt động bay bằng cánh quạt, có thể cất cánh, hạ cánh thẳng đứng, có thể bay đứng trong không khí và thậm chí bay lùi.
    
    ![](http://farm4.static.flickr.com/3254/2347122394_e84c04b09e.jpg)
    
    Chúng có khả năng VTOL (Vertical TakeOff and Landing), tức là cất cánh và hạ cánh theo phương thẳng đứng, hỗ trợ công tác ở những nơi có không gian hẹp như thung lũng, đầm lầy, núi rừng; không gian rộng trên trời dưới nước, cửa sông, biển lớn,...  
    
  + Tandem-wing craft (Máy bay cánh song song)
    
    Là loại khí cụ bay có hai cánh chính, một đối cánh nằm ở phía trước và đối cánh kia ở phía sau. Cả hai cánh góp phần nâng. Trong trường hợp cánh song song phía sau nhỏ hơn cánh phía trước, giống như cánh đuôi quá khổ, nó được gọi là **cánh Delanne** (từ trong [Maurice Delanne](https://fr.wikipedia.org/wiki/Maurice_Delanne), một nhà thiết kế máy bay cánh song song của Pháp.).
    
    ![](https://upload.wikimedia.org/wikipedia/commons/thumb/5/5d/HB-YBK_mignet_HM-380.jpg/200px-HB-YBK_mignet_HM-380.jpg)

## Unmanned Aerial Vehicle (UAV)

Có nhiều loại máy bay không người lái được sử dụng cho nhiều lĩnh vực. Nhưng ở đây xin đề cập tới loại Drone kích cỡ vừa được sử dụng phổ biến là **[Quadcopter](https://en.wikipedia.org/wiki/Quadcopter)**. Những loại UAV khác, nếu có nhu cầu sản xuất và phát triển UAV thì Trung Quốc, Israel và Mỹ là nơi có nguồn nguyên liệu dồi dào, giá cả phù hợp và công nghệ hàng đầu như [Dajiang Innovations - DJI](https://www.dji.com/) có trụ sở tại Thâm Quyến, Quảng Đông Trung Quốc; [Airobotics](https://www.airoboticsdrones.com/), [SwiftNav](https://www.swiftnav.com/), [3D Robotics](https://3dr.com/),... dành cho quý bạn.

**Quad hoặc Quadrotor hoặc Quadro có thân hình chữ X và có 4 cánh quạt được gắn trên mỗi cánh tay. Có 2 cánh quay cùng chiều kim đồng hồ và hai cánh quay ngược chiều kim đồng hồ. Đều này để bảo toàn momen góc (momen động lượng) để cho thân thiết bị bay không xoay vòng**. Định luật bảo toàn mômen động lượng được phát biểu: Mômen động lượng của một hệ không đổi khi hệ chịu tổng cộng các mômen ngoại lực bằng không.

   ![](https://www.mydroneview.blog/wp-content/uploads/2018/08/drone-yaw-elegant-quadcopter-of-drone-yaw.png)   ![](https://lh3.googleusercontent.com/tbKAh6LxJOtAbOxZLkeMTGgFSpuF3vpWIchXiyq01tBR8-K6RWQTU9sbjU0VBAZuUI9A8jNwL7ebgZ509Kf5X5LdeGceGu27w6eQFvbK8ndyLb_hJUYobYQe94COFFgU9epptwgbtdRzZNbFx0RW-TzANvuF1p_4odWvqPnV7fNZNd7bqtwwCx7eHmQ80SXtoQczsTfvx6QNE64_hA41Qaq0oi-CGqovGNThmmJ7MwuMSIeVIDOb4hJ-4iplgCI7oyaF3xmxJiZWY_EF59jJdWo0lLAOVJP4lU5jj5G66RoIl_o2dK-5OWtd1H8DdM4s0GeW5j2MqRHKR4YP-tfpsdSanwjUDqgNdL1EF0RMAVuhrdgs1qzzA5NJYLIAIn2DctC08EdKxxhozfwK6x-MVaKiz6SolHsIsT1FxZFxPBG55hnVDSYVM75rlwExQ10Y1xBv4Zh2uFWoLmivcGT6D4IKYxSrU3qyoShbJKTUvEUjLUvrRqWQTHG296jXPuFB_irpTE5bkrsNzEWe67OvRjyEviOTB9GRqs_ZWosFFdWI0NBueYBfSlPDxVxlxfbWQY9YTNeZH5K6NtHsaV4UFdYF-eFslviUjpQCay-GfyNoAcjJit0rD3B4Q6P9DRuzOCHYm0B4fo2khTptML-9JjBeWAQFP208e4claYABL0yjGYV_eNHd4AttE538FmpQGsUVSuSU5_G9fgJnsw=s277-no)   ![](https://upload.wikimedia.org/wikipedia/commons/2/2a/Quadrotor_yaw_torque.png)

Được ứng dụng nhiều trong nghiên cứu robotics; quân đội và công an được sử dụng để giám sát, trinh sát bởi các cơ quan thực thi quân sự, pháp luật, cũng như các nhiệm vụ tìm kiếm và cứu hộ trong môi trường đô thị; nhiếp ảnh; báo chí trong việc quay phim và chụp ảnh những nhân vật và diễn viên nổi tiếng; hoạt động nhân đạo cứu tế và bảo tồn thiên nhiên; nghệ thuật; thể thao drone racing,...
## Implementation
### Real devices
### Simulator

