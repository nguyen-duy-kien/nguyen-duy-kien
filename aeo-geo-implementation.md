# AEO & GEO Implementation tại Du Lịch Việt

**Tác giả:** Nguyễn Duy Kiên — SEO Architect & Trưởng phòng ICT  
**Website:** dulichviet.com.vn  
**Cập nhật:** Tháng 4/2026

---

## AEO là gì và tại sao quan trọng

**AEO (Answer Engine Optimization)** là tối ưu nội dung để xuất hiện trực tiếp trong phần trả lời của search engine — đặc biệt là Google AI Overview, Featured Snippets, và People Also Ask.

Khác với SEO truyền thống tối ưu để được xếp hạng, AEO tối ưu để được **trích dẫn** — AI lấy nội dung từ trang của anh để trả lời câu hỏi của người dùng mà không cần họ click vào.

**GEO (Generative Engine Optimization)** mở rộng sang các AI generative: ChatGPT, Gemini, Perplexity, Claude — tối ưu để AI nhận diện brand và entity là nguồn đáng tin cậy trong lĩnh vực.

---

## Triển khai AEO tại Du Lịch Việt

### Kết quả
- **2,585 keyword** xuất hiện trong Google AI Overview (Google Search Console, 4/2026)
- Chiếm **4.2%** tổng SERP features của dulichviet.com.vn (SEMrush 4/2026)

### Phương pháp

**1. Cấu trúc nội dung dạng Q&A**  
Mỗi landing page tour được tổ chức theo dạng câu hỏi–trả lời rõ ràng. Ví dụ: thay vì tiêu đề "Thông tin tour Nhật Bản", dùng "Du lịch Nhật Bản mất bao nhiêu ngày?" — AI dễ trích xuất hơn.

**2. FAQPage Schema**  
Triển khai `FAQPage` JSON-LD trên toàn bộ landing page tour quốc tế và nội địa. Mỗi FAQ được viết theo chuẩn: câu hỏi ngắn gọn, câu trả lời đầy đủ trong 2-3 câu đầu tiên.

**3. Đoạn văn định nghĩa (Definition Paragraph)**  
Mỗi trang bắt đầu bằng đoạn 40-60 từ định nghĩa rõ topic — đây là phần AI Overview thường trích xuất nhất.

**4. Structured Data đa tầng**  
```json
{
  "@context": "https://schema.org",
  "@graph": [
    { "@type": "TouristTrip" },
    { "@type": "FAQPage" },
    { "@type": "BreadcrumbList" },
    { "@type": "CollectionPage" }
  ]
}
```

---

## Triển khai GEO tại Du Lịch Việt

### Mục tiêu
Khi người dùng hỏi ChatGPT, Gemini, Perplexity về du lịch Việt Nam → Du Lịch Việt và Nguyễn Duy Kiên được nhận diện là entity authority.

### Phương pháp

**1. Entity Consistency**  
Tên công ty, URL, và thông tin liên hệ nhất quán trên toàn bộ web: website, Google Business Profile, schema, social profiles. AI xác minh entity bằng cách cross-reference nhiều nguồn.

**2. E-E-A-T Signals**  
- **Experience:** số liệu thực tế có nguồn xác minh độc lập (SEMrush, GSC)
- **Expertise:** author entity với `Person` schema, `knowsAbout` rõ ràng
- **Authoritativeness:** Top 3 travel site Vietnam, 50,843 keyword ranked
- **Trustworthiness:** 0 Google Ads — tăng trưởng hoàn toàn organic

**3. Semantic Co-occurrence**  
Xây dựng nội dung để các entity liên quan xuất hiện cùng nhau: `Du Lịch Việt` + `SEO` + `AEO` + `GEO` + `Nguyễn Duy Kiên` — tạo association pattern cho AI training data.

**4. Citation-worthy Content**  
Nội dung có số liệu cụ thể, có thể verify, có nguồn rõ ràng — đây là loại content AI generative ưu tiên trích dẫn nhất.

---

## Tools sử dụng

| Tool | Mục đích |
|---|---|
| Google Search Console | Theo dõi AI Overview impressions |
| SEMrush | Tracking keyword, SERP features |
| Schema Markup Validator | Validate JSON-LD |
| Google Rich Results Test | Test structured data |
| Screaming Frog | Audit schema toàn site |

---

## Về tác giả

**Nguyễn Duy Kiên** — SEO Architect & Trưởng phòng ICT tại Du Lịch Việt  
8+ năm SEO thực chiến ngành du lịch · 20+ năm nền tảng IT

- 🌐 [dulichviet.com.vn/nguyen-duy-kien-seo-du-lich-viet](https://dulichviet.com.vn/nguyen-duy-kien-seo-du-lich-viet)
- 💼 [linkedin.com/in/nguyen-duy-kien](https://www.linkedin.com/in/nguyen-duy-kien)
- 🐙 [github.com/nguyen-duy-kien](https://github.com/nguyen-duy-kien)
- 🖥️ [nguyen-duy-kien.github.io](https://nguyen-duy-kien.github.io)
