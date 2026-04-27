# 📚 HƯỚNG DẪN TOÀN BỘ HỆ THỐNG THU NHIÊN EDUCATION

## 🎯 Tổng Quan Hệ Thống

Bạn có một hệ thống **7-in-1 hoàn chỉnh**:

### 📋 File & Chức Năng

| File | Chức Năng | URL |
|------|----------|-----|
| `index-final.html` | Website chính (SEO + Social + Livestream + Blog) | `/` |
| `admin-dashboard-v5.html` | Admin Dashboard (Blog + Leads + Settings) | `/admin-dashboard.html` |
| `booking-system.html` | Booking Calendar (Livestream + 1:1 Coaching) | `/booking-system.html` |
| `email-analytics.html` | Email Automation + Data Analytics | `/email-analytics.html` |

---

## 🚀 SETUP & DEPLOYMENT

### Bước 1: Upload GitHub

```bash
# 1. Xóa files cũ
# Delete: index.html, admin-dashboard.html

# 2. Upload files mới
- index-final.html → Rename: index.html
- admin-dashboard-v5.html → Rename: admin-dashboard.html
- booking-system.html → Keep tên (dùng relative link)
- email-analytics.html → Keep tên
```

### Bước 2: Vercel Deploy
- Vercel tự động deploy khi push GitHub
- Wait 1-2 phút
- Test: https://thunhienedu.vercel.app

### Bước 3: Verify Links
```
✅ Website: https://thunhienedu.vercel.app
✅ Admin: https://thunhienedu.vercel.app/admin-dashboard.html
✅ Booking: https://thunhienedu.vercel.app/booking-system.html
✅ Email: https://thunhienedu.vercel.app/email-analytics.html
```

---

## 📝 VIẾT BÀI BLOG (Chi Tiết)

### Đăng Nhập Admin
```
URL: /admin-dashboard.html
Password: 123456
```

### Flow Viết Bài

**Tab "📝 Quản Lý Bài Viết"**

#### Bước 1: Điền Thông Tin Bài
```
Tiêu Đề: "5 Cách Giảm Lo Âu Con"
Icon: 😌 (tùy chọn)
Meta Description: "Hướng dẫn 5 kỹ năng từ coach" (max 160 ký tự)
Từ Khóa: "giảm lo âu con" (sẽ kiểm tra lặp lại)
Cloudinary Image: (paste URL ảnh - tùy chọn)
```

#### Bước 2: Viết Nội Dung HTML
```html
<h2>Vấn Đề Phổ Biến</h2>
<p>Giảm lo âu con là vấn đề mà nhiều bố mẹ...</p>

<h2>5 Cách Giảm Lo Âu Con Hiệu Quả</h2>
<ol>
  <li>Cách thứ 1: Mindfulness - Dạy con chánh niệm</li>
  <li>Cách thứ 2: Reframing - Thay đổi cách nhìn</li>
  <li>Cách thứ 3: Mirroring - Bắt chước cảm xúc con</li>
  <li>Cách thứ 4: Anchoring - Gắn cảm xúc tích cực</li>
  <li>Cách thứ 5: Future Pacing - Hình dung tương lai</li>
</ol>

<h2>Kết Luận</h2>
<p>Khi áp dụng các kỹ năng này...</p>
```

#### Bước 3: Kiểm Tra SEO
```
SEO Score tự động tính:
✅ Tiêu đề: 50-100 ký tự
✅ Meta Desc: ≤ 160 ký tự
✅ Nội dung: ≥ 1500 từ
✅ Từ khóa: lặp 2-5 lần
✅ Icon: có mặt

→ Score ≥ 80 là tốt (nhưng có thể đăng dù < 80)
```

#### Bước 4: Đăng Bài
- Click "✅ Đăng Bài Viết"
- Bài sẽ hiện trên Blog page
- Người dùng có thể bấm để đọc full

---

## 📅 BOOKING SYSTEM (Lịch Đặt)

### Cách Hoạt Động

**URL:** `/booking-system.html`

#### 1️⃣ Livestream Hàng Tuần
```
Thứ 2-5, 8:30 PM
→ Không cần đặt lịch riêng
→ Khách điền form → Gửi link livestream qua email
```

#### 2️⃣ Tư Vấn 1:1 (Coaching)
```
Thứ 3-4, giờ tùy chọn
→ Hiện calendar (chọn ngày)
→ Chọn giờ trống
→ Điền thông tin
→ System sẽ lưu vào Google Sheets

Giá: 99K/30p hoặc 199K/60p
Status: "Chưa thanh toán" (thanh toán sau buổi)
```

### Admin View
- Nhìn danh sách booking trong Google Sheets
- Xác nhận lịch qua email
- Cập nhật Zoom/Meet link

---

## 📧 EMAIL AUTOMATION (Gửi Email Hàng Loạt)

### URL
`/email-analytics.html` → Tab "📧 Email Automation"

### 4 Email Templates Có Sẵn

#### 1️⃣ Email Chào Mừng (Welcome)
```
Khi: Ngay sau đăng ký
Nội dung: Cảm ơn + Thông tin khóa + Link livestream
Đối tượng: Khách mới (< 7 ngày)
```

#### 2️⃣ Email Nuôi Dưỡng (Nurture)
```
Khi: Ngày 2-7 sau đăng ký
Nội dung: 3 mẹo NLP miễn phí + Tips thực hành
Đối tượng: Khách quan tâm
```

#### 3️⃣ Email Offer (Khuyến Mãi)
```
Khi: Ngày 8-10 sau đăng ký
Nội dung: GIẢM 20% khóa học + Deadline 24h
Đối tượng: Chưa mua
```

#### 4️⃣ Email Reminder (Lần Cuối)
```
Khi: Cuối campaign (ngày 12-14)
Nội dung: Ưu đãi sắp hết + Lời gọi hành động
Đối tượng: Chưa mua
```

### Cách Gửi Email

**Bước 1:** Chọn Template
- Click nút "🎉 Email Chào Mừng" (hoặc template khác)
- Chỉnh sửa subject & body nếu muốn
- Xem preview

**Bước 2:** Chọn Nhóm Khách
```
Lựa chọn:
- 🆕 Khách Mới (< 7 ngày)
- ⭐ Quan Tâm (xem khóa > 1 lần)
- 🛒 Chưa Mua (xem > 3 lần)
- 📧 Tất Cả Khách

Hoặc filter theo khóa học cụ thể
```

**Bước 3:** Gửi
- Click "📤 Gửi Email Hàng Loạt"
- Email sẽ được gửi ngay
- Lưu lịch sử trong "Email History"

### Placeholders Có Thể Dùng
```
{name} - Tên khách
{email} - Email khách
{course} - Khóa học đã đăng ký
{phone} - Số điện thoại
```

Ví dụ:
```
"Xin chào {name}, bạn đã đăng ký {course}. 
Liên hệ qua {phone} để biết thêm chi tiết."
```

---

## 📊 DATA ANALYTICS (Phân Tích Dữ Liệu)

### URL
`/email-analytics.html` → Tab "📊 Data Analytics"

### Dữ Liệu Hiển Thị

#### Stats Overview
```
👥 Tổng Khách Hàng: 150
💰 Tổng Doanh Thu: 500,000,000 VND
📈 Conversion Rate: 35%
🔴 Livestream Followers: 120
```

#### Charts
```
1. 📊 Khóa Học Phổ Biến Nhất (Doughnut Chart)
   → Hiển thị khóa nào được đăng ký nhiều

2. 📈 Xu Hướng Đăng Ký (Line Chart)
   → Đăng ký tăng/giảm 7 ngày qua

3. 🎯 Phân Bố Vấn Đề (Bar Chart)
   → Vấn đề nào khách quan tâm nhất
   (lo âu, học tập, mâu thuẫn, tự tin...)
```

#### Insights & Recommendations
```
Tự động sinh:
- "Có 45 khách chưa mua. Gửi email offer!"
- "120 khách muốn livestream. Chuẩn bị nội dung!"
- "Lo âu cao. Viết bài blog: '5 cách giảm lo âu'!"
```

#### Phân Khúc Khách (Customer Segments)
```
| Phân Khúc | Số Lượng | Email Template |
|-----------|----------|---|
| Khách Mới (< 7 ngày) | 25 | Welcome Email |
| Quan Tâm (xem 1-3) | 50 | Nurture Email |
| Chưa Mua (xem > 3) | 75 | Offer Email |
```

Quick action: Click "Gửi Email" để gửi ngay cho segment

---

## 👥 QUẢN LÝ KHÁCH HÀNG (CRM)

### Ở Đâu
Admin Dashboard → Tab "👥 Quản Lý Khách Hàng"

### Thông Tin Khách

Mỗi khách có:
```
✓ Tên, Email, Số điện thoại
✓ Khóa học đã đăng ký
✓ Trạng thái: Chưa liên hệ / Đã liên hệ / Đã mua
✓ Ngày đăng ký
```

### Hành Động

#### Update Trạng Thái
```
Dropdown: Chưa liên hệ → Đã liên hệ → Đã mua
Dùng để tracking quá trình sales
```

#### Xóa Khách
```
Click "🗑️ Xóa" (cẩn thận, không hoàn tác)
```

#### Export CSV
```
Click "📥 Export CSV"
Tải về Excel để phân tích thêm
```

---

## ⚙️ ADMIN SETTINGS

### Đổi Mật Khẩu

**Tab "⚙️ Cấu Hình"**

```
Mật khẩu cũ: 123456
Mật khẩu mới: Nhập cái mới
Xác nhận: Nhập lại

⚠️ Lưu ý: Cần backend để lưu trữ persistent
   (Hiện tại chỉ làm được qua code)
```

### Reset Dữ Liệu

```
Nút "⚠️ Xóa Toàn Bộ Dữ Liệu"
→ XÓA: Blog posts, Leads, Bookings (không hoàn tác!)
→ Dùng để test/reset
```

---

## 🖼️ CLOUDINARY SETUP (Ảnh Blog)

### Tạo Account
1. Đi https://cloudinary.com
2. Đăng ký (free 10GB/tháng)
3. Dashboard → Upload ảnh

### Upload Ảnh Blog
1. Cloudinary → Upload ảnh
2. Copy URL (dạng: `https://res.cloudinary.com/.../image.jpg`)
3. Admin → Viết Bài → Field "Cloudinary Image URL"
4. Paste URL & đăng bài

### Lợi Ích
```
✅ Không tốn server Vercel (free 50MB)
✅ Tự do upload/thay ảnh
✅ CDN nhanh toàn cầu
✅ Miễn phí cho 10GB/tháng
```

---

## 📱 SOCIAL MEDIA INTEGRATION

### Links Đã Setup
```
📘 Facebook: facebook.com/thunhienbetterminds
💬 Zalo: 0987654321
🎵 TikTok: @thunhienbetterminds
📧 Email: dangky@thunhienedu.vn
```

### Ở Trên Website
```
1. Hero Section: 3 nút CTA (Đăng Ký, Xem Khóa, Livestream)
2. Social Section: Icon tròn bấm được
3. Livestream Banner: Ở top header
4. Livestream Popup: Chi tiết & link follow
```

---

## 🔗 GOOGLE SHEETS INTEGRATION

### Setup (Đã Làm)
```
Google Sheets: https://docs.google.com/spreadsheets/d/1wKUz02Hlk5m6Hfe4Z8unGpJXhOp-gtgtU_mE1dV4u6M/edit

Apps Script Webhook: 
https://script.google.com/macros/s/AKfycbzXfueXIUdEuK3iU08vWz97aCaJWqFZkoHE61hBkP_rmOg4Llh65YBsHR0Py9Xejfj5/exec
```

### Dữ Liệu Sync
```
✓ Form đăng ký → Sheet "Leads"
✓ Booking livestream → Sheet "Livestream"
✓ Booking 1:1 → Sheet "Coaching"
✓ Email history → localStorage (local)
```

### Xem Dữ Liệu
- Vào Google Sheet
- Mỗi sheet là một form type
- Data real-time từ website

---

## 🎬 LIVESTREAM WORKFLOW

### Chuẩn Bị
```
Thứ 2-5, 8:30 PM

1. Chuẩn bị nội dung (NLP tips, Q&A)
2. Setup Zoom/Meet
3. Gửi link cho followers (Zalo/TikTok)
```

### Khách Đăng Ký
```
1. Bấm "🔴 Tham Gia Livestream" trên website
2. Điền form (tên, email, topic)
3. Nhận email xác nhận + link Zoom

Hoặc: Follow TikTok @thunhienbetterminds
     → Bấm nút "Follow" → Nhận thông báo live
```

### Post-Livestream
```
1. Gửi email "Cảm ơn" + Recording link
2. Chọn Q&A tốt để làm content blog
3. Update: Followers số, retention rate
```

---

## 💡 BEST PRACTICES

### 📝 Blog Content
```
✓ Tiêu đề catchy (50-100 ký tự)
✓ Meta description hấp dẫn (120-160 ký tự)
✓ Nội dung ≥ 1500 từ (chi tiết, giá trị cao)
✓ Từ khóa lặp 2-5 lần (tự nhiên, không spam)
✓ Ảnh đẹp từ Cloudinary
✓ HTML formatting sạch: h2, p, strong, ul, ol

→ Nên viết bài 2-3/tuần để SEO tốt
```

### 📧 Email Campaign
```
✓ Gửi tối đa 2-3 email/tuần (không spam)
✓ Timing: Sáng 9h, trưa 12h, chiều 5p
✓ Subject line catchy & short (< 60 ký tự)
✓ Nội dung 200-300 từ (ngắn gọn, rõ ràng)
✓ 1 CTA chính (Đăng ký, Xem khóa, Tham gia)
✓ Personalization: Dùng {name}, {course}

→ A/B test subject lines để tối ưu open rate
```

### 🎯 Booking System
```
✓ Mở booking sớm (2-3 tuần trước)
✓ Update available slots thường xuyên
✓ Gửi reminder email 24h trước
✓ Follow-up sau buổi (cảm ơn + feedback form)

→ Goal: 80%+ show-up rate
```

### 📊 Analytics
```
✓ Xem analytics hàng tuần
✓ Focus metrics: Conversion rate, Email open rate, Booking rate
✓ A/B test: Email template, Landing page, CTA button
✓ Iterate: Dữ liệu cho biết phải làm gì tiếp

→ Target:
  - Conversion rate: 25-40% (mục tiêu)
  - Email open rate: 20-30%
  - Booking rate: 5-10% từ leads
```

---

## 🐛 TROUBLESHOOTING

### Form Không Gửi?
```
❌ "CORS error"
✅ Giải pháp: Google Sheets Apps Script đã setup mode: 'no-cors'
   → Bình thường

❌ "Email không nhận"
✅ Giải pháp: 
   - Kiểm tra email đó đúng không
   - Kiểm tra spam folder
   - Dữ liệu lưu vào localStorage (dev tools > Application)
```

### Ảnh Blog Không Hiển Thị?
```
❌ Ảnh từ Cloudinary lỗi
✅ Giải pháp:
   - Kiểm tra URL đúng không
   - Cloudinary public folder phải public
   - Thử upload lại ảnh
```

### Calendar Booking Lỗi?
```
❌ Slots không update
✅ Giải pháp:
   - F5 refresh page
   - Clear localStorage (⚙️ Settings → Xóa Dữ Liệu)
   - Kiểm tra thứ 3-4 được bật chưa (ngày khác thì disabled)
```

---

## 📞 LIÊN HỆ & SUPPORT

```
📧 Email: dangky@thunhienedu.vn
💬 Zalo: 0987654321
🎵 TikTok: @thunhienbetterminds
```

---

## 📋 CHECKLIST DEPLOYMENT

- [ ] Upload files GitHub (index.html, admin-dashboard.html, booking-system.html, email-analytics.html)
- [ ] Vercel deploy & test links
- [ ] Test Admin Login (password: 123456)
- [ ] Viết 3-5 bài blog demo
- [ ] Upload ảnh blog qua Cloudinary
- [ ] Setup Google Sheets integration
- [ ] Kiểm tra form submit → Google Sheets
- [ ] Test email template gửi
- [ ] Test booking calendar
- [ ] Setup Zoom/Meet link livestream
- [ ] Share link website + booking page với khách
- [ ] Monitor analytics & optimize

---

## 🎓 Tips Nâng Cao

### SEO Blog
```
1. Keyword research: Google Trends, SEMrush
2. Long-form content: 2000+ từ cho top ranking
3. Internal linking: Link bài cũ vào bài mới
4. External link: Nhúng link authority cao
5. Meta tags: Schema.org cho recipe/breadcrumb
```

### Email Automation
```
1. Segment sophistication: Thêm chi tiết khách
2. Dynamic content: {name}, {course}, {ageGroup}
3. Automated workflow: Welcome → Nurture → Offer
4. Re-engagement: Email cho khách cũ
5. Win-back: Email cho khách inactive
```

### Booking Optimization
```
1. Reduce friction: 3-4 fields là max
2. Confirmation: Email + SMS reminder
3. Cancellation policy: Clear, fair
4. Feedback loop: Post-session survey
5. Upsell: Recommend khóa khác trong confirmation
```

---

**Good luck! 🚀**

---

*Last Updated: April 27, 2025*
*Version: System v5 Final*
