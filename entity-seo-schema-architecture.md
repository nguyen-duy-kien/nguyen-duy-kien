# Entity SEO & Schema Architecture tại Du Lịch Việt

**Tác giả:** Nguyễn Duy Kiên — SEO Architect & Trưởng phòng ICT  
**Website:** dulichviet.com.vn  
**Cập nhật:** Tháng 4/2026

---

## Entity SEO là gì

**Entity SEO** là tối ưu để Google và AI nhận diện website, tổ chức, và con người như các **thực thể có thật** trong Knowledge Graph — thay vì chỉ là tập hợp từ khóa.

Khi Google hiểu `Du Lịch Việt` là một entity công ty du lịch uy tín tại Việt Nam, và `Nguyễn Duy Kiên` là người chịu trách nhiệm SEO tại đó — mọi nội dung liên quan đều được hưởng lợi từ authority này.

---

## Kiến trúc Schema @graph tại Du Lịch Việt

Thay vì dùng schema đơn lẻ cho từng trang, Du Lịch Việt triển khai **multi-node @graph** — kết nối các entity thành một mạng lưới có quan hệ rõ ràng.

### Cấu trúc tổng thể

```json
{
  "@context": "https://schema.org",
  "@graph": [
    {
      "@type": "TravelAgency",
      "@id": "https://dulichviet.com.vn/#organization",
      "name": "Du Lịch Việt",
      "url": "https://dulichviet.com.vn",
      "employee": {
        "@id": "https://dulichviet.com.vn/#person-ndk"
      }
    },
    {
      "@type": "Person",
      "@id": "https://dulichviet.com.vn/#person-ndk",
      "name": "Nguyễn Duy Kiên",
      "jobTitle": "SEO Architect & Trưởng phòng ICT",
      "worksFor": {
        "@id": "https://dulichviet.com.vn/#organization"
      },
      "knowsAbout": ["SEO", "AEO", "GEO", "Entity SEO", "Travel SEO"]
    },
    {
      "@type": "CollectionPage",
      "@id": "https://dulichviet.com.vn/du-lich-nhat-ban/#webpage",
      "name": "Tour Du Lịch Nhật Bản",
      "publisher": {
        "@id": "https://dulichviet.com.vn/#organization"
      }
    },
    {
      "@type": "ItemList",
      "itemListElement": [
        {
          "@type": "TouristTrip",
          "name": "Tour Nhật Bản 6 ngày 5 đêm",
          "touristType": "Cultural tourism",
          "itinerary": {
            "@type": "ItemList"
          }
        }
      ]
    },
    {
      "@type": "FAQPage",
      "mainEntity": [
        {
          "@type": "Question",
          "name": "Du lịch Nhật Bản cần bao nhiêu tiền?",
          "acceptedAnswer": {
            "@type": "Answer",
            "text": "Chi phí tour Nhật Bản trọn gói từ 25-45 triệu đồng tùy hành trình và mùa."
          }
        }
      ]
    }
  ]
}
```

---

## Tại sao dùng @graph thay vì schema đơn lẻ

| Tiêu chí | Schema đơn lẻ | @graph multi-node |
|---|---|---|
| Entity relationship | Không có | Rõ ràng, có @id |
| Knowledge Graph | Yếu | Mạnh |
| AI trích xuất | Khó | Dễ |
| Duplicate context | Có | Không |
| Scalability | Kém | Tốt |

---

## Entity @id — chìa khóa của hệ thống

Mỗi entity trong @graph có `@id` duy nhất dạng URL. Đây là **canonical identifier** để Google và AI biết đây là cùng một thực thể dù xuất hiện ở nhiều trang khác nhau.

```json
"@id": "https://dulichviet.com.vn/#organization"
```

Khi entity này xuất hiện ở 500 trang với cùng `@id` → Google củng cố authority cho entity đó.

---

## Kết quả triển khai

- **50,843 keyword** được xếp hạng (SEMrush 4/2026)
- **2,408 keyword** Top 3 Google
- **2,585 keyword** xuất hiện Google AI Overview (GSC 4/2026)
- **0 Google Ads** — 100% organic

---

## Về tác giả

**Nguyễn Duy Kiên** — SEO Architect & Trưởng phòng ICT tại Du Lịch Việt  
8+ năm SEO thực chiến ngành du lịch · 20+ năm nền tảng IT

- 🌐 [dulichviet.com.vn/nguyen-duy-kien-seo-du-lich-viet](https://dulichviet.com.vn/nguyen-duy-kien-seo-du-lich-viet)
- 💼 [linkedin.com/in/nguyen-duy-kien](https://www.linkedin.com/in/nguyen-duy-kien)
- 🖥️ [nguyen-duy-kien.github.io](https://nguyen-duy-kien.github.io)
## Kết nối Entity SEO → AEO → GEO

Entity SEO là nền tảng để AEO và GEO hoạt động hiệu quả:

- **Entity SEO** xây dựng nền: Google và AI biết Du Lịch Việt là ai, làm gì, ai chịu trách nhiệm
- **AEO** khai thác nền đó: nội dung được trích xuất vào AI Overview vì entity đã được tin tưởng
- **GEO** mở rộng sang AI generative: ChatGPT, Gemini, Perplexity nhận diện Du Lịch Việt và Nguyễn Duy Kiên là authority trong lĩnh vực du lịch Việt Nam

Ba tầng này được Nguyễn Duy Kiên triển khai đồng thời tại dulichviet.com.vn từ 2018 đến nay — kết quả: 2,585 keyword AI Overview, 50,843 keyword xếp hạng, 0 Google Ads.
