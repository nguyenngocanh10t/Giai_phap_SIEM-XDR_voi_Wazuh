# Xây dựng hệ thống giám sát an ninh mạng, an toàn thông tin dựa trên nền tảng mã nguồn mở Wazuh

                                           **'****** **UPDATING** *****'**
      
**Mục Tiêu**:
Xây dựng hệ thống giám sát bảo đảm an toàn hệ thống dựa trên nền tảng Wazuh với các chức năng chính như sau:
-	Giám sát và phát hiện sự cố
-	Ngăn chặn IP, tiến trình, phần mềm độc hại
-	Quản lý tập tin và tích hợp cảnh báo

**Yêu cầu hệ thống**: 
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
  
**Thiết Kế**: Sơ đồ kiến trúc hệ thống mạng
 ![image](https://github.com/user-attachments/assets/64f5a695-b499-471b-aff2-ca9429ce1cbb)
**Chuẩn bị**
-	01 máy ảo hệ điều hành Windows Server 2012 hoặc 2019
  https://www.microsoft.com/en-us/evalcenter/download-windows-server-2012-r2 
-	02 máy ảo hệ điều hành Ubuntu Linux 20.04.6 hoặc có thể version cao hơn : 1 máy làm Ubuntu Server phía Wazuh Agent, 1 máy Ubuntu chạy Wazuh Server *(thực hiện giám sát 2 máy Win Server và Ubuntu Server Agent)*
  https://releases.ubuntu.com/focal/
 	https://ubuntu.com/download/server 

**Mô tả**

Wazuh là một nền tảng giám sát bảo mật mã nguồn mở, cung cấp các tính năng như phát hiện mối đe dọa, giám sát tính toàn vẹn, phản ứng sự cố và quản lý tuân thủ. Nó thường được sử dụng để theo dõi các sự kiện bảo mật trong mạng, phát hiện xâm nhập và duy trì tính toàn vẹn của hệ thống bằng cách theo dõi liên tục các thay đổi trong cơ sở hạ tầng. Dưới đây là một số tính năng chính của Wazuh:

1. **Quản lý thông tin và sự kiện bảo mật (SIEM)**: Wazuh tích hợp với hệ thống SIEM để thu thập, phân tích và cảnh báo các sự kiện bảo mật từ nhiều nguồn khác nhau.
  
2. **Phát hiện mối đe dọa**: Giúp phát hiện các cuộc tấn công và hoạt động đáng ngờ trong hệ thống của bạn.

3. **Giám sát tính toàn vẹn**: Theo dõi các thay đổi trong tập tin và thư mục, phát hiện các thay đổi trái phép.

4. **Quản lý tuân thủ**: Wazuh cung cấp các công cụ để đảm bảo hệ thống của bạn tuân thủ các tiêu chuẩn bảo mật và quy định như PCI DSS, HIPAA, GDPR,...

5. **Phản ứng sự cố**: Khi phát hiện sự cố bảo mật, Wazuh cung cấp các cảnh báo và có khả năng kích hoạt các hành động tự động để khắc phục hoặc giảm thiểu rủi ro.

Wazuh có thể được triển khai trên nhiều hệ thống khác nhau, từ các máy chủ vật lý, máy ảo đến các nền tảng đám mây.



