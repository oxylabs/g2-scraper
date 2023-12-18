# G2 Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs’ [G2 Scraper](https://oxylabs.io/products/scraper-api/web/g2?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an G2 website effortlessly. This brief guide explains how an G2 Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get G2 results by providing your own URLs to our service. We can return the HTML for any G2 page you like.

#### Python code example

The example below illustrates how you can get HTML of G2 page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://www.g2.com/categories/drop-shipping'
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('user', 'pass1'),
    json=payload,
)

# Instead of response with job status and results url, this will return the
# JSON response with the result.
pprint(response.json())
```
Find code examples for other programming languages [**here**](https://github.com/oxylabs/g2-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html class=\" cors history json svg es6object promises cssgradients fontface csstrans ... </html>",
      "created_at": "2023-12-18 10:38:31",
      "updated_at": "2023-12-18 10:38:57",
      "page": 1,
      "url": "https://www.g2.com/categories/drop-shipping",
      "job_id": "7142463132672215041",
      "status_code": 200
    }
  ]
}
```
With our G2 Scraper, you can seamlessly draw out public data from any G2 webpage. Compile the essential software information, like feature lists, user ratings, or detailed summaries, to conduct an in-depth market analysis and keep an edge over your rivals. Should you require assistance or have any questions, feel free to contact our support team via live chat or send us an email at hello@oxylabs.io.