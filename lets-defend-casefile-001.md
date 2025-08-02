# 🛡️ Let’s Defend: Case File 001 – Operation: Data Extractor

**Mission Type:** Covert Reconnaissance  
**Status:** ✅ Concluded  
**Analyst:** Samuel Fwelo

---

## 🎯 Mission Objective

Simulate an ethical web scraping operation against a public product listing page.  
Extract and analyze structured data like name, price, and availability — without tripping alarms.

---

## 🧰 Tools Used

- `requests`
- `BeautifulSoup`
- `pandas`
- `fake_useragent`
- `sleep()` for delay logic

---

## 🔍 HTML Snapshot

```html
<div class="product-card">
  <h2 class="title">Organic Olive Oil</h2>
  <span class="price">$12.99</span>
  <p class="availability">In stock</p>
</div>
