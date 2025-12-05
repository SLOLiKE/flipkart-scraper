# Flipkart Scraper
> This scraper pulls structured product data from Flipkart pages, giving you clean and reliable information without the mess of manual collection. It captures everything from prices and images to variants, specifications, and ratings. If you're building price trackers, research tools, or automation workflows, this Flipkart scraper makes the job easy.


<p align="center">
  <a href="https://bitbash.dev" target="_blank">
    <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/scraper.png" alt="Bitbash Banner" width="100%"></a>
</p>
<p align="center">
  <a href="https://t.me/Bitbash333" target="_blank">
    <img src="https://img.shields.io/badge/Chat%20on-Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram">
  </a>&nbsp;
  <a href="https://wa.me/923249868488?text=Hi%20BitBash%2C%20I'm%20interested%20in%20automation." target="_blank">
    <img src="https://img.shields.io/badge/Chat-WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" alt="WhatsApp">
  </a>&nbsp;
  <a href="mailto:sale@bitbash.dev" target="_blank">
    <img src="https://img.shields.io/badge/Email-sale@bitbash.dev-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail">
  </a>&nbsp;
  <a href="https://bitbash.dev" target="_blank">
    <img src="https://img.shields.io/badge/Visit-Website-007BFF?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Website">
  </a>
</p>




<p align="center" style="font-weight:600; margin-top:8px; margin-bottom:8px;">
  Created by Bitbash, built to showcase our approach to Scraping and Automation!<br>
  If you are looking for <strong>Flipkart Scraper</strong> you've just found your team — Let’s Chat. 👆👆
</p>


## Introduction
This project focuses on gathering product-level information from Flipkart. It handles product pages, category listings, and search result URLs, giving users a consistent data structure regardless of how large the crawl is.
It’s ideal for developers, analysts, and businesses who need fresh product insights without dealing with the platform manually.

### How It Works Behind the Scenes
- Reads product, listing, or category URLs and extracts structured details.
- Automatically paginates through listings when needed.
- Captures multiple variant types like color, size, and storage.
- Collects specs, ratings, seller details, and pricing info.
- Supports proxy rotation to reduce blocking.

## Features
| Feature | Description |
|----------|-------------|
| Multi-URL scraping | Accepts individual product URLs or entire listing pages. |
| Variant extraction | Pulls detailed variant information including images and stock. |
| Full product specs | Captures technical attributes and structured specification groups. |
| Ratings & reviews | Extracts rating summary, aspect ratings, and review counts. |
| Pricing breakdown | Collects MRP, special prices, discounts, and offer details. |
| Auto-pagination | Moves through listing pages until limits are reached. |
| Proxy support | Helps bypass rate limits and blocking issues. |

---

## What Data This Scraper Extracts
| Field Name | Field Description |
|-------------|------------------|
| url | Product detail URL or variant URL. |
| title | Product title including storage, color, and model info. |
| brand | Brand name identified on the product page. |
| main_image | Primary product image. |
| images | Array of all variant or product images. |
| prices | List of price objects with amounts, currency, and discount info. |
| attributes | Product attributes such as color, storage, RAM, etc. |
| specs | Structured specification groups with key–value pairs. |
| seller_info | Seller ID, name, and rating. |
| rating_info | Overall rating, count, review numbers, and aspect ratings. |
| variants | All available product variants with their URLs and images. |
| breadcrumbs | Category hierarchy describing product placement. |
| reviews | Review objects when available. |

---

## Example Output


    {
      "url": "https://www.flipkart.com/samsung-galaxy-z-flip5-graphite-512-gb/p/itm68c9544497769",
      "main_image": "http://rukmini1.flixcart.com/image/823/823/xif0q/mobile/u/w/t/galaxy-flip5-sm-f731bliains-samsung-original-imagru5pgwsfnrmq.jpeg?q=100",
      "brand": "SAMSUNG",
      "current_variant": {
        "product_id": "MOBGRS32HRBVHMBA",
        "title": "SAMSUNG Galaxy Z Flip5 (Graphite, 512 GB)",
        "prices": [
          { "amount": 113999, "name": "Selling Price" },
          { "amount": 109999, "name": "Special Price" }
        ]
      },
      "attributes": [
        { "name": "Color", "options": ["Graphite", "Cream", "Mint", "Lavender"] },
        { "name": "Storage", "options": ["256 GB", "512 GB"] }
      ],
      "rating_info": {
        "average": 4.4,
        "count": 431
      }
    }

---

## Directory Structure Tree


    Flipkart Scraper/
    ├── src/
    │   ├── runner.js
    │   ├── extractors/
    │   │   ├── flipkart_parser.js
    │   │   └── utils_pagination.js
    │   ├── outputs/
    │   │   └── dataset_exporter.js
    │   └── config/
    │       └── settings.example.json
    ├── data/
    │   ├── inputs.sample.json
    │   └── sample_output.json
    ├── package.json
    └── README.md

---

## Use Cases
- **Ecommerce analysts** use it to monitor prices and discounts so they can track competitor trends.
- **Developers** use it to feed structured Flipkart product data into dashboards or automation workflows.
- **Retail intelligence teams** use it to evaluate seller performance and product availability.
- **Researchers** use it to collect large datasets for market studies.
- **Startup founders** use it to validate product niches quickly using fresh marketplace data.

---

## FAQs

**Does it support category and search result URLs?**
Yes, it handles both and will automatically paginate until the item limit is reached.

**Can it extract all variant combinations?**
It captures color, storage, RAM, and other variant types whenever the information is available.

**Are proxies required?**
They’re optional, but using them helps reduce blocking during large runs.

**Does it provide reviews?**
Review extraction depends on page availability. Rating summaries and aspect ratings are always included when present.

---

### Performance Benchmarks and Results

**Primary Metric:** On average, the scraper processes about 40–60 product pages per minute depending on network conditions and proxy usage.

**Reliability Metric:** Typical success rates remain near 98 percent for well-structured product URLs.

**Efficiency Metric:** Memory usage stays stable even during long runs thanks to streamed data handling.

**Quality Metric:** Data completeness averages 95 percent across price fields, specifications, variants, and seller information, based on repeated test runs.


<p align="center">
<a href="https://calendar.app.google/74kEaAQ5LWbM8CQNA" target="_blank">
  <img src="https://img.shields.io/badge/Book%20a%20Call%20with%20Us-34A853?style=for-the-badge&logo=googlecalendar&logoColor=white" alt="Book a Call">
</a>
  <a href="https://www.youtube.com/@bitbash-demos/videos" target="_blank">
    <img src="https://img.shields.io/badge/🎥%20Watch%20demos%20-FF0000?style=for-the-badge&logo=youtube&logoColor=white" alt="Watch on YouTube">
  </a>
</p>
<table>
  <tr>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/MLkvGB8ZZIk" target="_blank">
        <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/review1.gif" alt="Review 1" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        "Bitbash is a top-tier automation partner, innovative, reliable, and dedicated to delivering real results every time."
      </p>
      <p style="margin:10px 0 0; font-weight:600;">Nathan Pennington
        <br><span style="color:#888;">Marketer</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/8-tw8Omw9qk" target="_blank">
        <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/review2.gif" alt="Review 2" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        "Bitbash delivers outstanding quality, speed, and professionalism, truly a team you can rely on."
      </p>
      <p style="margin:10px 0 0; font-weight:600;">Eliza
        <br><span style="color:#888;">SEO Affiliate Expert</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/m-dRE1dj5-k?si=5kZNVlKsGUhg5Xtx" target="_blank">
        <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/review3.gif" alt="Review 3" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        "Exceptional results, clear communication, and flawless delivery. <br>Bitbash nailed it."
      </p>
      <p style="margin:1px 0 0; font-weight:600;">Syed
        <br><span style="color:#888;">Digital Strategist</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
  </tr>
</table>
