# OmniSearchAPI

## Endpoints
### 1. GET /api/domains
``` JSON
{
  "status": "success",
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

### 2. GET /api/popular

``` JSON
{
  "status": "success",
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

### 3. GET /api/search?query=raspberry%20pi%205&domain=all&limit=10

``` JSON
{
  "status": "success",
  "query": "raspberry pi 5",
  "domain": "all",
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
        "id": "CE09788",
        "name": "Raspberry Pi 5 Model B 8GB",
        "sku": "CE09788",
        "price": 138.20,
        "currency": "AUD",
        "description": "The Raspberry Pi 5 Model B with 8GB RAM, featuring the new RP1 southbridge and BCM2712 CPU.",
        "image_url": "/images/products/raspberry-pi-5-8gb.jpg",
        "url": "/product/raspberry-pi-5-model-b-8gb",
        "in_stock": true,
        "rank": 1,
        "relevance_score": 0.98,
        "type": "product"
      },
      {
        "id": "CE10111",
        "name": "Raspberry Pi 5 Model B 16GB",
        "sku": "CE10111",
        "price": 212.50,
        "currency": "AUD",
        "description": "The Raspberry Pi 5 Model B with 16GB RAM, featuring the new RP1 southbridge and BCM2712 CPU.",
        "image_url": "/images/products/raspberry-pi-5-16gb.jpg",
        "url": "/product/raspberry-pi-5-model-b-16gb",
        "in_stock": true,
        "rank": 2,
        "relevance_score": 0.96,
        "type": "product"
      },
      {
        "id": "CE09785",
        "name": "Raspberry Pi 5 Model B 4GB",
        "sku": "CE09785",
        "price": 100.98,
        "currency": "AUD",
        "description": "The Raspberry Pi 5 Model B with 4GB RAM, featuring the new RP1 southbridge and BCM2712 CPU.",
        "image_url": "/images/products/raspberry-pi-5-4gb.jpg",
        "url": "/product/raspberry-pi-5-model-b-4gb",
        "in_stock": true,
        "rank": 3,
        "relevance_score": 0.95,
        "type": "product"
      },
      {
        "id": "CE09790",
        "name": "Raspberry Pi 5 Case, Black/Grey (Official)",
        "sku": "CE09790",
        "price": 17.75,
        "currency": "AUD",
        "description": "Official Raspberry Pi 5 case in black and grey, with proper ventilation and access to all ports.",
        "image_url": "/images/products/raspberry-pi-5-case.jpg",
        "url": "/product/raspberry-pi-5-case",
        "in_stock": true,
        "rank": 4,
        "relevance_score": 0.88,
        "type": "product"
      },
      {
        "id": "CE09784",
        "name": "Raspberry Pi 5 Model B 2GB",
        "sku": "CE09784",
        "price": 84.22,
        "currency": "AUD",
        "description": "The Raspberry Pi 5 Model B with 2GB RAM, featuring the new RP1 southbridge and BCM2712 CPU.",
        "image_url": "/images/products/raspberry-pi-5-2gb.jpg",
        "url": "/product/raspberry-pi-5-model-b-2gb",
        "in_stock": true,
        "rank": 5,
        "relevance_score": 0.87,
        "type": "product"
      }
    ],
    "product_catalog": [
      {
        "id": "cat-rpi5",
        "name": "Raspberry Pi 5",
        "description": "The Raspberry Pi 5 series of single-board computers",
        "product_count": 12,
        "url": "/catalog/raspberry-pi-5",
        "rank": 1,
        "relevance_score": 0.95,
        "type": "product_catalog"
      }
    ],
    "projects": [
      {
        "id": "proj-rpi5-media",
        "name": "Build a Raspberry Pi 5 Media Center",
        "description": "Create a powerful media center using Raspberry Pi 5 and LibreELEC.",
        "difficulty": "Beginner",
        "estimated_time": "2 hours",
        "components": ["Raspberry Pi 5", "MicroSD Card", "Case", "Power Supply"],
        "url": "/projects/raspberry-pi-5-media-center",
        "image_url": "/images/projects/rpi5-media-center.jpg",
        "rank": 1,
        "relevance_score": 0.78,
        "type": "project"
      },
      {
        "id": "proj-rpi5-retro",
        "name": "Retro Gaming Console with Raspberry Pi 5",
        "description": "Build your own retro gaming machine using a Raspberry Pi 5.",
        "difficulty": "Intermediate",
        "estimated_time": "3 hours",
        "components": ["Raspberry Pi 5", "MicroSD Card", "Controller", "Case"],
        "url": "/projects/raspberry-pi-5-retro-gaming",
        "image_url": "/images/projects/rpi5-retro-gaming.jpg",
        "rank": 2,
        "relevance_score": 0.75,
        "type": "project"
      }
    ],
    "guides": [
      {
        "id": "guide-rpi5-setup",
        "name": "Getting Started with Raspberry Pi 5",
        "description": "A comprehensive guide to setting up your new Raspberry Pi 5.",
        "reading_time": "15 minutes",
        "difficulty": "Beginner",
        "url": "/guides/raspberry-pi-5-setup",
        "image_url": "/images/guides/rpi5-setup.jpg",
        "rank": 1,
        "relevance_score": 0.85,
        "type": "guide"
      }
    ],
    "technology": [
      {
        "id": "tech-rpi5-specs",
        "name": "Raspberry Pi 5 Technical Specifications",
        "description": "Detailed technical specifications and performance metrics for the Raspberry Pi 5.",
        "url": "/technology/raspberry-pi-5-specifications",
        "rank": 1,
        "relevance_score": 0.82,
        "type": "technology"
      }
    ]
  }
}
```

## Error Responses
All non 200 responses will have a JSON payload with the status, code, and a message explaining the error.

```JSON
{
  "status": "error",
  "code": 400,
  "message": "Missing required parameter: query"
}
```

```JSON
{
  "status": "error",
  "code": 500,
  "message": "Internal server error"
}
```
