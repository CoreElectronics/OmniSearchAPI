# OmniSearchAPI

## Endpoints
### 1. Get Search Domains
Retrieves all available search domains that can be searched/filtered.

**REQUEST:**
``` GET /api/domains ```

**RESPONSE:**
``` JSON
{
  "response_status": "success",
  "response_code": 200,
  "domains": [
    {
      "id": "all",
      "name": "All"
    },
    {
      "id": "products",
      "name": "Products"
    },
    {
      "id": "product_catalog",
      "name": "Product Catalog"
    },
    {
      "id": "brands",
      "name": "Brands"
    },
    {
      "id": "technology",
      "name": "Technology"
    },
    {
      "id": "guides",
      "name": "Guides"
    },
    {
      "id": "projects",
      "name": "Projects"
    },
    {
      "id": "discussions",
      "name": "Discussions"
    },
    {
      "id": "services",
      "name": "Services"
    },
    {
      "id": "store_info",
      "name": "Store Info"
    },
    {
      "id": "events",
      "name": "Events"
    }
  ]
}
```

### 2. Get Popular Search Terms
Returns a list of all the popular search terms when the user clicks on/focuses on the search bar.

**REQUEST:**

``` GET /api/popular ```

**RESPONSE:**
``` JSON
{
  "response_status": "success",
  "response_code": 200,
  "popular_terms": [
    {
      "term": "Raspberry Pi",
      "count": 15420
    },
    {
      "term": "Raspberry Pi 5 Starter Kit",
      "count": 8765
    },
    {
      "term": "Raspberry Pi 5 4 GB",
      "count": 7650
    },
    {
      "term": "Raspberry Pi 5 8 GB",
      "count": 6543
    },
    {
      "term": "Arduino",
      "count": 5487
    },
    {
      "term": "Micro:bit",
      "count": 4356
    },
    {
      "term": "Raspberry Pi Pico",
      "count": 3876
    },
    {
      "term": "Sensors",
      "count": 3245
    },
    {
      "term": "LED",
      "count": 2987
    },
    {
      "term": "Power Supply",
      "count": 2765
    }
  ]
}
```

### 3. Search
Performs a search based on the query string and selected domain.

**REQUEST:**
``` GET /api/search?query=raspberry%20pi%205&domain=all&limit=10 ```

**RESPONSE:**

``` JSON
{
  "response_status": "success",
  "response_code": 200,
  "query": "raspberry pi 5",
  "domain": "all",
  "result_count": {
    "products": 5,
    "brands": 1,
    "product_catalog": 1,
    "projects": 2,
    "services": 0,
    "guides": 1,
    "technology": 1,
    "discussions": 1,
    "store_info": 1,
    "events": 1
  },
  "suggested_terms": [
    "Raspberry Pi 5",
    "Raspberry Pi 5 Starter Kit",
    "Raspberry Pi 5 4GB",
    "Raspberry Pi 5 8GB",
    "Raspberry Pi 5 Case",
    "Raspberry Pi 5 Power Supply",
    "Raspberry Pi 5 Desktop Kit",
    "Raspberry Pi 5 Projects",
    "Raspberry Pi 5 Cooling",
    "Raspberry Pi 5 Compatibility"
  ],
  "results": {
    "products": [
      {
        "id": 482192,
        "id_web": 55113,
        "title": "Raspberry Pi 5 Model B 8GB",
        "sku": "CE09788",
        "price": 138.20,
        "currency": "AUD",
        "description": "The Raspberry Pi 5 Model B with 8GB RAM, featuring the new RP1 southbridge and BCM2712 CPU.",
        "image_url": "/images/products/raspberry-pi-5-8gb.jpg",
        "url": "/product/raspberry-pi-5-model-b-8gb",
        "in_stock": true,
        "attributes": {
          "memory": "8GB",
          "processor": "Broadcom BCM2712",
          "wifi": "802.11ac",
          "bluetooth": "5.0",
          "usb_ports": 4,
          "hdmi_ports": 2,
          "voltage_rating": "5.1V",
          "power_input": "USB-C"
        },
        "rank": 1,
        "relevance_score": 0.98
      },
      {
        "id": 484211,
        "id_web": 56981,
        "title": "Raspberry Pi 5 Model B 16GB",
        "sku": "CE10111",
        "price": 212.50,
        "currency": "AUD",
        "description": "The Raspberry Pi 5 Model B with 16GB RAM, featuring the new RP1 southbridge and BCM2712 CPU.",
        "image_url": "/images/products/raspberry-pi-5-16gb.jpg",
        "url": "/product/raspberry-pi-5-model-b-16gb",
        "in_stock": true,
        "attributes": {
          "memory": "16GB",
          "processor": "Broadcom BCM2712",
          "wifi": "802.11ac",
          "bluetooth": "5.0",
          "usb_ports": 4,
          "hdmi_ports": 2,
          "voltage_rating": "5.1V",
          "power_input": "USB-C"
        },
        "rank": 2,
        "relevance_score": 0.96
      },
      {
        "id": 482189,
        "id_web": 55110,
        "title": "Raspberry Pi 5 Model B 4GB",
        "sku": "CE09785",
        "price": 100.98,
        "currency": "AUD",
        "description": "The Raspberry Pi 5 Model B with 4GB RAM, featuring the new RP1 southbridge and BCM2712 CPU.",
        "image_url": "/images/products/raspberry-pi-5-4gb.jpg",
        "url": "/product/raspberry-pi-5-model-b-4gb",
        "in_stock": true,
        "attributes": {
          "memory": "4GB",
          "processor": "Broadcom BCM2712",
          "wifi": "802.11ac",
          "bluetooth": "5.0",
          "usb_ports": 4,
          "hdmi_ports": 2,
          "voltage_rating": "5.1V",
          "power_input": "USB-C"
        },
        "rank": 3,
        "relevance_score": 0.95
      },
      {
        "id": 482194,
        "id_web": 55115,
        "title": "Raspberry Pi 5 Case, Black/Grey (Official)",
        "sku": "CE09790",
        "price": 17.75,
        "currency": "AUD",
        "description": "Official Raspberry Pi 5 case in black and grey, with proper ventilation and access to all ports.",
        "image_url": "/images/products/raspberry-pi-5-case.jpg",
        "url": "/product/raspberry-pi-5-case",
        "in_stock": true,
        "attributes": {
          "color": "Black/Grey",
          "material": "Plastic",
          "compatibility": "Raspberry Pi 5 Model B"
        },
        "rank": 4,
        "relevance_score": 0.88
      },
      {
        "id": 482188,
        "id_web": 55109,
        "title": "Raspberry Pi 5 Model B 2GB",
        "sku": "CE09784",
        "price": 84.22,
        "currency": "AUD",
        "description": "The Raspberry Pi 5 Model B with 2GB RAM, featuring the new RP1 southbridge and BCM2712 CPU.",
        "image_url": "/images/products/raspberry-pi-5-2gb.jpg",
        "url": "/product/raspberry-pi-5-model-b-2gb",
        "in_stock": true,
        "attributes": {
          "memory": "2GB",
          "processor": "Broadcom BCM2712",
          "wifi": "802.11ac",
          "bluetooth": "5.0",
          "usb_ports": 4,
          "hdmi_ports": 2,
          "voltage_rating": "5.1V",
          "power_input": "USB-C"
        },
        "rank": 5,
        "relevance_score": 0.87
      }
    ],
    "brands": [
      {
        "id": 136,
        "id_web": 359,
        "title": "Raspberry Pi",
        "relevance_score": 0.88,
        "rank": 1
      }
    ],
    "product_catalog": [
      {
        "id": 221,
        "id_web": 134,
        "title": "Raspberry Pi 5",
        "description": "The Raspberry Pi 5 series of single-board computers",
        "product_count": 12,
        "url": "/catalog/raspberry-pi-5",
        "rank": 1,
        "relevance_score": 0.95,
        "type": "category"
      }
    ],
    "projects": [
      {
        "id": 53,
        "id_web": 233,
        "title": "Build a Raspberry Pi 5 Media Center",
        "description": "Create a powerful media center using Raspberry Pi 5 and LibreELEC.",
        "url": "/projects/raspberry-pi-5-media-center",
        "rank": 1,
        "relevance_score": 0.78
      },
      {
        "id": 94,
        "id_web": 274,
        "title": "Retro Gaming Console with Raspberry Pi 5",
        "description": "Build your own retro gaming machine using a Raspberry Pi 5.",
        "url": "/projects/raspberry-pi-5-retro-gaming",
        "rank": 2,
        "relevance_score": 0.75
      }
    ],
    "services": [],
    "guides": [
      {
        "id": 1,
        "id_web": 1,
        "title": "Getting Started with Raspberry Pi 5",
        "description": "A comprehensive guide to setting up your new Raspberry Pi 5.",
        "url": "/guides/raspberry-pi-5-setup",
        "rank": 1,
        "relevance_score": 0.85
      }
    ],
    "technology": [
      {
        "id": 44,
        "id_web": 3212,
        "title": "Raspberry Pi 5 Technical Specifications",
        "description": "Detailed technical specifications and performance metrics for the Raspberry Pi 5.",
        "rank": 1,
        "relevance_score": 0.82
      }
    ],
    "discussions": [
      {
        "id": 7131,
        "id_web": 18143,
        "title": "Raspberry Pi 5 Model B 8GB (CE09786)",
        "description": "Share your Raspberry Pi 5 projects, ideas, and experiences with the community.",
        "url": "/t/raspberry-pi-5-model-b-8gb-ce09786/18143",
        "rank": 1,
        "relevance_score": 0.93,
        "type": "forum"
      }
    ],
    "store_info": [
      {
        "id": 212,
        "id_web": 2,
        "title": "Raspberry Pi Customer Buying Restrictions",
        "description": "Important information regarding the purchase of Raspberry Pi products.",
        "url": "/store-info/raspberry-pi-buying-restrictions",
        "rank": 1,
        "relevance_score": 0.72
      }
    ],
    "events": [
      {
        "id": 1,
        "id_web": 1,
        "title": "Raspberry PI Workshop - Beginners",
        "description": "Join us for a hands-on workshop to learn the basics of Raspberry Pi.",
        "date": "2022-03-15",
        "url": "/events/raspberry-pi-workshop-beginners",
        "rank": 1,
        "relevance_score": 0.85
      }
    ]
  }
}
```

### 4. Domain-Specific Search
When a specific domain is selected, the search is focused on that domain.
limit = 128

**REQUEST:**
``` GET /api/search?query=raspberry%20pi%205&domain=products&limit=128 ```

**RESPONSE:**
``` JSON
{
  "response_status": "success",
  "response_code": 200,
  "query": "raspberry pi 5",
  "result_count": 128,
  "domain": "products",
  "suggested_terms": [
    "Raspberry Pi 5 8GB",
    "Raspberry Pi 5 4GB",
    "Raspberry Pi 5 16GB",
    "Raspberry Pi 5 Case",
    "Raspberry Pi 5 Power Supply",
    "Raspberry Pi 5 Cooling Fan",
    "Raspberry Pi 5 Starter Kit",
    "Raspberry Pi 5 2GB",
    "Raspberry Pi 5 Desktop Kit",
    "Raspberry Pi 5 Accessories"
  ],
  "results": {
    "products": [
      {
        "id": 482192,
        "id_web": 55113,
        "title": "Raspberry Pi 5 Model B 8GB",
        "sku": "CE09788",
        "price": 138.20,
        "currency": "AUD",
        "description": "The Raspberry Pi 5 Model B with 8GB RAM, featuring the new RP1 southbridge and BCM2712 CPU.",
        "image_url": "/images/products/raspberry-pi-5-8gb.jpg",
        "url": "/product/raspberry-pi-5-model-b-8gb",
        "in_stock": true,
        "attributes": {
          "memory": "8GB",
          "processor": "Broadcom BCM2712",
          "wifi": "802.11ac",
          "bluetooth": "5.0",
          "usb_ports": 4,
          "hdmi_ports": 2,
          "voltage_rating": "5.1V",
          "power_input": "USB-C"
        },
        "rank": 1,
        "relevance_score": 0.98
      },
      {
        "id": 484211,
        "id_web": 56981,
        "title": "Raspberry Pi 5 Model B 16GB",
        "sku": "CE10111",
        "price": 212.50,
        "currency": "AUD",
        "description": "The Raspberry Pi 5 Model B with 16GB RAM, featuring the new RP1 southbridge and BCM2712 CPU.",
        "image_url": "/images/products/raspberry-pi-5-16gb.jpg",
        "url": "/product/raspberry-pi-5-model-b-16gb",
        "in_stock": true,
        "attributes": {
          "memory": "16GB",
          "processor": "Broadcom BCM2712",
          "wifi": "802.11ac",
          "bluetooth": "5.0",
          "usb_ports": 4,
          "hdmi_ports": 2,
          "voltage_rating": "5.1V",
          "power_input": "USB-C"
        },
        "rank": 2,
        "relevance_score": 0.96
      },
      {
        "id": 482189,
        "id_web": 55110,
        "title": "Raspberry Pi 5 Model B 4GB",
        "sku": "CE09785",
        "price": 100.98,
        "currency": "AUD",
        "description": "The Raspberry Pi 5 Model B with 4GB RAM, featuring the new RP1 southbridge and BCM2712 CPU.",
        "image_url": "/images/products/raspberry-pi-5-4gb.jpg",
        "url": "/product/raspberry-pi-5-model-b-4gb",
        "in_stock": true,
        "attributes": {
          "memory": "4GB",
          "processor": "Broadcom BCM2712",
          "wifi": "802.11ac",
          "bluetooth": "5.0",
          "usb_ports": 4,
          "hdmi_ports": 2,
          "voltage_rating": "5.1V",
          "power_input": "USB-C"
        },
        "rank": 3,
        "relevance_score": 0.95
      },
      {
        "id": 482194,
        "id_web": 55115,
        "title": "Raspberry Pi 5 Case, Black/Grey (Official)",
        "sku": "CE09790",
        "price": 17.75,
        "currency": "AUD",
        "description": "Official Raspberry Pi 5 case in black and grey, with proper ventilation and access to all ports.",
        "image_url": "/images/products/raspberry-pi-5-case.jpg",
        "url": "/product/raspberry-pi-5-case",
        "in_stock": true,
        "attributes": {
          "color": "Black/Grey",
          "material": "Plastic",
          "compatibility": "Raspberry Pi 5 Model B"
        },
        "rank": 4,
        "relevance_score": 0.88
      },
      {
        "id": 482188,
        "id_web": 55109,
        "title": "Raspberry Pi 5 Model B 2GB",
        "sku": "CE09784",
        "price": 84.22,
        "currency": "AUD",
        "description": "The Raspberry Pi 5 Model B with 2GB RAM, featuring the new RP1 southbridge and BCM2712 CPU.",
        "image_url": "/images/products/raspberry-pi-5-2gb.jpg",
        "url": "/product/raspberry-pi-5-model-b-2gb",
        "in_stock": true,
        "attributes": {
          "memory": "2GB",
          "processor": "Broadcom BCM2712",
          "wifi": "802.11ac",
          "bluetooth": "5.0",
          "usb_ports": 4,
          "hdmi_ports": 2,
          "voltage_rating": "5.1V",
          "power_input": "USB-C"
        },
        "rank": 5,
        "relevance_score": 0.87
      },
      {},
      {},
      {},
      {},
      {},
      {}
    ]
  }
}
```

## Error Responses
All non 200 responses will have a JSON payload with the status, code, and a message explaining the error.

```JSON
{
  "response_status": "error",
  "response_code": 400,
  "message": "Missing required parameter: query"
}
```

```JSON
{
  "response_status": "error",
  "response_code": 500,
  "message": "Internal server error"
}
```
