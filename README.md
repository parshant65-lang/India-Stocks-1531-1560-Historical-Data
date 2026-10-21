# India-Stocks-1531-1560-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 1531 to 1560)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-1531-1560-Historical-Data/
├── .github/workflows/daily_ingest.yml
├── fetch_batch.py
├── README.md
├── <SYMBOL>/
│   └── 1m/
│       ├── README.md
│       └── <YYYY>/
│           └── <MM>/
│               ├── <SYMBOL>_1m_<YYYY-MM-DD>.csv
```

---

## ⏰ 4-Tier Automated Schedule (Mon–Fri)

| Trigger | Time (IST) | Cron (UTC) | Role |
|:---|:---:|:---:|:---|
| **Primary Trigger** | **15:45 IST** | `15 10 * * 1-5` | 15 mins post-market close |
| **Backup Trigger 1** | **16:45 IST** | `15 11 * * 1-5` | 1 hour safety net |
| **Backup Trigger 2** | **17:45 IST** | `15 12 * * 1-5` | 2 hours safety net |
| **Backup Trigger 3** | **18:45 IST** | `15 13 * * 1-5` | 3 hours safety net |

---

## 📦 Constituents (1531 to 1560)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 1531 | `LATENTVIEW` | Latent View Analytics Limited | `LATENTVIEW.NS` |
| 1532 | `LATTEYS` | Latteys Industries Limited | `LATTEYS.NS` |
| 1533 | `LAXMICOT` | Laxmi Cotspin Limited | `LAXMICOT.NS` |
| 1534 | `LAXMIDENTL` | Laxmi Dental Limited | `LAXMIDENTL.NS` |
| 1535 | `LAXMIINDIA` | Laxmi India Finance Limited | `LAXMIINDIA.NS` |
| 1536 | `LCCINFOTEC` | LCC Infotech Limited | `LCCINFOTEC.NS` |
| 1537 | `LCCPROJECT` | LCC Projects Limited | `LCCPROJECT.NS` |
| 1538 | `LCL` | Lohia Corp Limited | `LCL.NS` |
| 1539 | `LEAPIND` | LEAP India Limited | `LEAPIND.NS` |
| 1540 | `LEENEE` | Lee & Nee Softwares Exports Limited | `LEENEE.NS` |
| 1541 | `LEMERITE` | Le Merite Exports Limited | `LEMERITE.NS` |
| 1542 | `LEXUS` | Lexus Granito (India) Limited | `LEXUS.NS` |
| 1543 | `LFIC` | Lakshmi Finance & Industrial Corporation Limited | `LFIC.NS` |
| 1544 | `LGBBROSLTD` | LG Balakrishnan & Bros Limited | `LGBBROSLTD.NS` |
| 1545 | `LGHL` | Laxmi Goldorna House Limited | `LGHL.NS` |
| 1546 | `LIBAS` | Libas Consumer Products Limited | `LIBAS.NS` |
| 1547 | `LIBERTSHOE` | Liberty Shoes Limited | `LIBERTSHOE.NS` |
| 1548 | `LIKHITHA` | Likhitha Infrastructure Limited | `LIKHITHA.NS` |
| 1549 | `LINC` | Linc Limited | `LINC.NS` |
| 1550 | `LINCOLN` | Lincoln Pharmaceuticals Limited | `LINCOLN.NS` |
| 1551 | `LKPSEC` | LKP Securities Limited | `LKPSEC.NS` |
| 1552 | `LLOYDSENGG` | LLOYDS ENGINEERING WORKS LIMITED | `LLOYDSENGG.NS` |
| 1553 | `LLOYDSENT` | Lloyds Enterprises Limited | `LLOYDSENT.NS` |
| 1554 | `LMW` | LMW Limited | `LMW.NS` |
| 1555 | `LOKESHMACH` | Lokesh Machines Limited | `LOKESHMACH.NS` |
| 1556 | `LORDSCHLO` | Lords Chloro Alkali Limited | `LORDSCHLO.NS` |
| 1557 | `LOTUSCHO` | Lotus Chocolate Company Limited | `LOTUSCHO.NS` |
| 1558 | `LOTUSDEV` | Sri Lotus Developers and Realty Limited | `LOTUSDEV.NS` |
| 1559 | `LOTUSEYE` | Lotus Eye Hospital and Institute Limited | `LOTUSEYE.NS` |
| 1560 | `LOVABLE` | Lovable Lingerie Limited | `LOVABLE.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream LATENTVIEW 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-1531-1560-Historical-Data/main/LATENTVIEW/1m/2026/10/LATENTVIEW_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
