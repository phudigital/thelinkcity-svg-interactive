# Interactive SVG Map - The Link City

Bản đồ tương tác chất lượng cao với các hiệu ứng chuyển động CSS tinh tế, được thiết kế cho trải nghiệm người dùng hiện đại.

## 🌟 Tính Năng Nổi Bật
- **Line Motion**: Hiệu ứng mờ hiện cho các tuyến đường chính.
- **Dash Flow**: Hiệu ứng dòng chảy cho các đường nét đứt (mô phỏng giao thông/hướng di chuyển).
- **Logo Highlight**: Hiệu ứng Pulse và Glow cho vị trí trung tâm.
- **Responsive**: Tối ưu hiển thị trên mọi kích thước màn hình.

## 🚀 Hướng Dẫn Sử Dụng
### 1. Xem Preview
Mở file `preview.html` bằng trình duyệt bất kỳ để xem toàn bộ chuyển động.

### 2. Nhúng vào Website
Cách tốt nhất để giữ lại các hiệu ứng CSS trong SVG là sử dụng thẻ `<object>`:
```html
<object data="mapthelinkcity.svg" type="image/svg+xml" width="100%"></object>
```

---

## 🛠 Hướng Dẫn Kỹ Thuật: Tạo SVG Chuyển Động

Để tạo hiệu ứng cho bất kỳ file SVG nào, bạn cần thực hiện theo 3 bước chuẩn chuyên nghiệp sau:

### Bước 1: Khai báo CSS trong file SVG
Mở file `.svg` bằng trình soạn thảo mã nguồn và thêm thẻ `<style>` ngay sau tag `<svg>` mở:

```xml
<svg ...>
  <style>
    /* Định nghĩa các Keyframes và Class ở đây */
  </style>
  ...
</svg>
```

### Bước 2: Các hiệu ứng phổ biến (Tra cứu nhanh)

| Tên Class | Hiệu ứng | Mã CSS Gợi Ý |
| :--- | :--- | :--- |
| `.line-motion` | Mờ hiện nhẹ nhàng | `0% { opacity: 0.3; } 100% { opacity: 1; }` |
| `.dashed-flow` | Dòng chảy nét đứt | `to { stroke-dashoffset: -16; }` |
| `.logo-pulse` | Đập/Tỏa sáng | `transform: scale(1.1); filter: brightness(1.2);` |
| `.rotate-slow` | Xoay chậm | `to { transform: rotate(360deg); }` |

### Bước 3: Gán Class vào các thẻ SVG
Tìm đến thẻ cần tạo hiệu ứng (ví dụ: `<path>`, `<rect>`, `<g>`) và thêm thuộc tính `class`:

```xml
<!-- Trước khi sửa -->
<path style="fill:#84AD8C;" d="..." />

<!-- Sau khi thêm hiệu ứng -->
<path style="fill:#84AD8C;" class="line-motion" d="..." />
```

---

## 💡 Lưu Ý Quan Trọng
1. **Transform Origin**: Khi sử dụng hiệu ứng `scale` hoặc `rotate`, hãy luôn xác định `transform-origin` theo tọa độ tâm của đối tượng đó để tránh bị lệch (ví dụ: `transform-origin: 700px 250px;`).
2. **Stroke-dasharray**: Hiệu ứng di chuyển nét đứt chỉ hoạt động với các thẻ có thuộc tính `stroke-dasharray`.
3. **Hardware Acceleration**: Sử dụng `transform` thay vì thay đổi trực tiếp tọa độ để đạt hiệu năng tốt nhất.

## 📄 License
Dự án được phát triển bởi **Phu Digital Vibe Coding**. Trình bày và tối ưu hóa bởi Antigravity AI.
