---
title: "Hướng dẫn nhanh mạch MVS01"
date: 2025-02-02T17:55:28+08:00
description: "Hướng dẫn đơn giản, dễ hiểu để điều chỉnh nhanh mạch MVS01-SDWF (cơ bản) ngay sau khi đấu nối."
tags: ["guides", "mach_han_cell", "mach_rong"]
type: post
weight: 25
showTableOfContents: true
image: "/posts/huong-dan-nhanh-mach-mvs01sdwf/cover.png"
---

{{< figure src="mvs01.png" alt="Mạch MVS01-SDWF" >}}


## 1. Đồng bộ điện áp hiển thị trên mạch

* Tắt nguồn điện.
* **Ấn giữ núm xoay**, sau đó **bật nguồn** để vào Setup
* Tại vol Calib: Chỉnh cho **điện áp hiển thị khớp với điện áp thực tế**.
* Để lưu và thoát: Đạp cóc → Khởi động

---

## 2. Chỉnh thông số hàn

Ví dụ hiển thị trên màn hình:

```
Vol: 220 W:   82
P1 25 C 50 M1 60
```

### Giải thích thông số

#### 🔹 Vol: 220 W:     82 - Thông tin 
* Vol: 220 là đồng hồ hiển thị điện lưới.
* W:    80 là bộ đếm số lần hàn.


#### 🔹 P1 25 — Xung hàn mồi (Pre, 10 ms)

* P1 25 = công suất **25%**.
* Đây là **xung làm mềm kẽm** trước khi hàn chính.
* Khuyến nghị để nhỏ: **15% – 25%**.

#### 🔹 C 50 — Thời gian nghỉ

* C 50 = **50 ms** nghỉ giữa xung mồi và xung chính.
* Điều chỉnh phù hợp với biến áp vì nó liên quan đến độ đẹp của mối hàn.

#### 🔹 M1 60 — Xung hàn chính (Main, 10 ms)

* M1 60 = công suất **60%**.
* Đây là **xung hàn chính**, ảnh hưởng trực tiếp đến độ ngấu.
* Nên chỉnh cao hơn P1 và tùy theo độ dày kẽm.

## 4. Video/ Link
* Hướng dẫn chi tiết: [Tài liệu](/guides/esp32-dragon/). 
* Cách chọn BTA100: [Bài viết](https://www.facebook.com/my.my.63808)
* Liên hệ My My: [facebook](https://www.facebook.com/my.my.63808)
---

> **Gợi ý:** Mỗi biến áp khác nhau sẽ có một thông số khác nhau, cho nên cần chỉnh theo nguyên lý. Sau đó hàn thử và điều chỉnh phù hợp cho đến khi đạt được kết quả tối ưu.
