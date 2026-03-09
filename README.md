# JMeter Performance Test

## Website Tested

Website được kiểm thử: https://vnexpress.net

Công cụ sử dụng: **Apache JMeter**

Mục tiêu của bài test là kiểm tra hiệu năng website khi nhiều người dùng truy cập cùng lúc.

---

# Thread Group 1 – Basic Test

* Users: 10
* Loop Count: 5

Request:
GET /

Kết quả:

![result](images/summary1.png)

---

# Thread Group 2 – Heavy Load

* Users: 50
* Ramp-up: 30s

Request:
GET /
GET /tin-tuc-24h

Kết quả:

![result](images/summary2.png)

---

# Thread Group 3 – Custom Test

* Users: 20
* Duration: 60s

Request:
GET /
GET /kinh-doanh

Kết quả:

![result](images/summary3.png)

---

# Kết luận

Qua kiểm thử bằng JMeter, website hoạt động ổn định với các mức tải khác nhau. Response time tăng khi số lượng người dùng tăng nhưng không xuất hiện lỗi request.
