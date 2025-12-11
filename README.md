# Linktree Profile Listing Scraper
> Linktree Profile Listing Scraper helps you automatically collect creator profiles from Linktree’s public profile directory, turning scattered pages into a clean, structured dataset. It solves the tedious task of manually browsing thousands of profiles and centralizes creator insights for marketing, research, and business intelligence. With this Linktree profile scraper, you can quickly discover, segment, and analyze creators at scale.


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
  If you are looking for <strong>linktree-profile-listing-scraper</strong> you've just found your team — Let’s Chat. 👆👆
</p>


## Introduction
Linktree Profile Listing Scraper is a specialized tool that navigates Linktree’s public profile directory and extracts key information about creators, including usernames, categories, avatars, and verification status. It replaces manual copy-paste workflows with an automated, repeatable process that outputs ready-to-use data.

This project is ideal for marketing teams, influencer platforms, talent agencies, growth strategists, and researchers who need to understand the digital creator landscape. Instead of clicking through endless profile pages, users can configure a few parameters and generate consistent, structured results.

### Why Linktree Profile Data Matters
- Captures verified and unverified creators across categories for market mapping and segmentation.
- Enables scalable creator discovery for influencer campaigns and partnership pipelines.
- Provides clean fields for analytics, dashboards, and CRM enrichment.
- Helps identify niche communities and emerging talent via category-based exploration.
- Supports geo-targeted research by aligning proxy locations with regional creator directories.

## Features
| Feature | Description |
|--------|-------------|
| Category-based profile discovery | Crawls Linktree profile listing pages filtered by category and pagination, so you can target specific creator niches. |
| Configurable retry logic | Uses a max retries per URL setting to gracefully handle timeouts, slow responses, or transient failures without stalling. |
| Proxy-aware crawling | Integrates residential-style proxy configuration to reduce bot detection and align with the target region of interest. |
| Result size control | Limits the number of profiles per URL via a max items setting, helping you control runtime and resource usage. |
| Structured JSON output | Produces consistently structured records for each profile, ready for import into databases, BI tools, or spreadsheets. |
| Source URL tracking | Stores the origin URL for every profile, making it easy to trace results back to the exact listing page. |
| Flexible URL list input | Accepts multiple profile directory URLs so you can batch different categories, regions, or pages in a single run. |
| Optimized for large directories | Designed to handle pagination-heavy directories efficiently, making it suitable for large-scale creator discovery. |

---

## What Data This Scraper Extracts
| Field Name | Field Description |
|-----------|-------------------|
| profile_title | The display title or headline shown on the creator’s Linktree profile, often representing their brand or personal tagline. |
| username | The creator’s unique Linktree handle, used to directly reference or visit their profile. |
| category.category_id | The internal category identifier (such as "business" or "entertainment") describing the creator’s main niche. |
| category.label | The human-readable label for the category, suitable for reporting and dashboards. |
| avatar_url | Direct URL to the creator’s profile image, useful for visual review, directory UIs, or identity checks. |
| verification_tick | Boolean value indicating whether Linktree has marked the profile as verified, signaling trust and prominence. |
| profile_badges | A list or value representing special badges or achievements associated with the profile, if any are present. |
| from_url | The exact listing page URL where the profile was discovered, useful for traceability and auditability. |

---

## Example Output
    [
      {
        "profile_title": "Thanks for stopping by!",
        "username": "yourmeetecoach",
        "category": {
          "category_id": "business",
          "label": "Business"
        },
        "avatar_url": "https://d1fdloi71mui9q.cloudfront.net/0zrO7sbRT3rEzrDPIybe_IMG_6134.JPG",
        "verification_tick": false,
        "profile_badges": null,
        "from_url": "https://linktr.ee/discover/profile-directory/c/all/page-4/"
      }
    ]

---

## Directory Structure Tree
    linktree-profile-listing-scraper (IMPORTANT :!! always keep this name as the name of the apify actor !!! Linktree Profile Listing Scraper )/
    ├── src/
    │   ├── main.ts
    │   ├── crawler/
    │   │   ├── linktreeClient.ts
    │   │   ├── listingNavigator.ts
    │   │   └── profileExtractor.ts
    │   ├── config/
    │   │   ├── defaults.ts
    │   │   └── schema.ts
    │   └── utils/
    │       ├── logger.ts
    │       ├── proxyManager.ts
    │       └── retryHelper.ts
    ├── data/
    │   ├── sample-input.json
    │   └── sample-output.json
    ├── tests/
    │   ├── profileExtractor.test.ts
    │   └── listingNavigator.test.ts
    ├── package.json
    ├── tsconfig.json
    ├── .env.example
    └── README.md

---

## Use Cases
- **Influencer marketing teams** use it to build category-filtered creator lists from Linktree, so they can quickly shortlist influencers for targeted campaigns.
- **Talent and creator agencies** use it to enrich their internal rosters with usernames, categories, and verification status, so they can identify high-potential prospects.
- **Market researchers** use it to map creator categories across regions, so they can understand content trends and digital creator ecosystems.
- **Growth and partnership managers** use it to discover collaboration-ready creators in specific niches, so they can launch co-branded initiatives more efficiently.
- **Data engineers and analysts** use it to feed clean Linktree profile data into analytics pipelines, so they can build dashboards and scoring models.

---

## FAQs

### How do I choose the right URLs to crawl?
Start from Linktree’s profile directory pages that match your target audience, such as all creators or specific categories. Each page typically represents a slice of the directory (for example, a given category and page number). Add multiple URLs if you want coverage across several categories or pagination levels.

### Why do I need proxies for this scraper?
Profile directories can load dynamically and may impose rate limits or anti-bot checks. Proxies help distribute requests and align traffic with the region you are targeting. For example, using a Singapore-based proxy can help when targeting global creator listings, while region-specific proxies can be useful for localized research.

### What should I set for max_items_per_url?
For initial tests, keep max_items_per_url relatively low (around 10–20) to validate that configuration and network settings work correctly. Once you are confident in the results and performance, you can gradually increase the limit to capture more profiles per run while monitoring runtime and resource usage.

### What if I am not getting any profiles in the output?
If the output is empty, first check that the URLs you provided are accessible in a browser and still show creator listings. Next, verify that your proxies (if configured) are active and correctly set. Finally, review retry and timeout settings to ensure the scraper has enough time to load dynamic content on each page.

---

### Performance Benchmarks and Results

**Primary Metric:** On a stable network, the scraper can process dozens of profile listing pages in a single session, typically extracting hundreds of profiles in a matter of minutes when max_items_per_url is tuned appropriately.

**Reliability Metric:** With a sensible max_retries_per_url value (for example, 2–3), the scraper maintains a high success rate on profile listing pages, gracefully handling intermittent timeouts and transient errors.

**Efficiency Metric:** By capping max_items_per_url and batching URLs, the scraper keeps memory and CPU usage modest, making it suitable for both local runs and integration into larger data pipelines.

**Quality Metric:** The output emphasizes completeness and consistency of core fields such as username, category, avatar URL, and verification status, resulting in datasets that require minimal post-processing before being used in analytics, CRMs, or campaign tools.


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
