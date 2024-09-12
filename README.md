# Xay_dung_he_thong_giam_sat_voi_cong_cu_ma_nguon_mo_Wazuh

      ********UPDATING*******
      
•	Mục Tiêu:
Xây dựng hệ thống giám sát bảo đảm an toàn hệ thống mạng cho công ty, doanh nghiệp, trường học,… với công cụ mã nguồn mở Wazuh với các chức năng chính như sau:
-	Giám sát và phát hiện sự cố
-	Ngăn chặn IP độc hại
-	Quản lý tập tin và tích hợp

•	Yêu cầu hệ thống: 
-	Cấu hình chặn địa chỉ IP độc hại truy cập đến Web Server
-	Giám sát tính toàn vẹn file(FIM) trên Wazuh
-	Phát hiện cuộc tấn công Brute-force trên Wazuh
-	Giám sát các sự kiên Docker
-	Phát hiện các tiến trình không được ủy quyền
-	Phát hiện các cuộc tấn công SQL Injection
-	Phát hiện các tệp nhị phân đáng ngờ trên Endpoint
-	Tích hợp VirusTotal và Wazuh để phát hiện và xóa các phần mềm độc hại
-	Tích hợp Yara và Wazuh để phát hiện phần mềm độc hại
-	Phát hiện lỗ hổng
-	Phát hiện tiến trình ẩn trên Ubuntu endpoint 
-	Giám sát việc thực thi các lệnh độc hại trên Wazuh
-	Phát hiện tấn công Shellshock
  
•	Thiết Kế: Sơ đồ kiến trúc hệ thống mạng
 ![image](https://github.com/user-attachments/assets/12517104-4e3f-4751-952e-ef3984cf89b2)


1.1	Mô tả

Công cụ: Wazuh là một nền tảng giám sát bảo mật mã nguồn mở, cung cấp các tính năng như phát hiện mối đe dọa, giám sát tính toàn vẹn, phản ứng sự cố và quản lý tuân thủ. Nó thường được sử dụng để theo dõi các sự kiện bảo mật trong mạng, phát hiện xâm nhập và duy trì tính toàn vẹn của hệ thống bằng cách theo dõi liên tục các thay đổi trong cơ sở hạ tầng. Dưới đây là một số tính năng chính của Wazuh:

1. Quản lý thông tin và sự kiện bảo mật (SIEM): Wazuh tích hợp với hệ thống SIEM để thu thập, phân tích và cảnh 
  
2. Phát hiện mối đe dọa: Giúp phát hiện các cuộc tấn công và hoạt động đáng ngờ trong hệ thống của bạn.

3. Giám sát tính toàn vẹn: Theo dõi các thay đổi trong tập tin và thư mục, phát hiện các thay đổi trái phép.


 1.2	Chuẩn bị

-	01 máy ảo hệ điều hành Windows Server 2012
-	02 máy ảo hệ điều hành Ubuntu Linux 24.04.1 : 1 máy làm Ubuntu Server phía Wazuh Agent, 1 máy Ubuntu chạy Wazuh Server



5. Quản lý tuân thủ: Wazuh cung cấp các công cụ để đảm bảo hệ thống của bạn tuân thủ các tiêu chuẩn bảo mật và quy định như PCI DSS, HIPAA, GDPR,...

6. Phản ứng sự cố: Khi phát hiện sự cố bảo mật, Wazuh cung cấp các cảnh báo và có khả năng kích hoạt các hành động tự động để khắc phục hoặc giảm thiểu rủi ro.

Wazuh có thể được triển khai trên nhiều hệ thống khác nhau, từ các máy chủ vật lý, máy ảo đến các nền tảng đám mây.
