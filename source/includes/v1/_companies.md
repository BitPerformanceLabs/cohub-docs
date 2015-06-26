# Companies

### Endpoint

/api/v1/companies

### Attributes

| Name                  | Type    | Editable | Description                                                              |
|:----------------------|:--------|:---------|:-------------------------------------------------------------------------|
| id                    | integer | no       | Identifier                                                               |
| name                  | string  | yes      | Company Name                                                             |
| federal_employer_id   | string  | yes      | EIN or tax number                                                        |
| phone_number          | string  | yes      | Phone Number                                                             |
| fax_number            | string  | yes      | Fax Number                                                               |
| starting_order_number | integer | yes      | The number that the next order should start at                           |
| tax_nexus             | array   | yes      | An array of states or regions where tax should be collected              |
| url                   | string  | yes      | Company website url                                                      |
| timezone              | string  | yes      | The primary timezone for your company                                    |
| receipt_bccs          | array   | yes      | Array of email addresss that will be Bcc'd on sales order receipt emails |
| address               | address | yes      | The primary company address                                              |
| logos                 | array   | yes      | An array of company logos                                                |

### Links

| Name                     | Description                                    |
|:-------------------------|:-----------------------------------------------|
| self                     | This company                                   |
| brands                   | Brands for this company                        |
| blogs                    | Blogs for this company                         |
| blog_categories          | Blog categories for this company               |
| box_sizes                | Box sizes for this company                     |
| categories               | Categories for this company                    |
| cogs_categories          | Cost of Goods Sold categories for this company |
| collections              | Collections for this company                   |
| collection_memberships   | Collection Memberships for this company        |
| customers                | Customers for this company                     |
| customer_fields          | Custom customer fields for this company        |
| discounts                |                                                |
| inventories              |                                                |
| invoices                 |                                                |
| inventory_transfers      |                                                |
| locations                |                                                |
| logos                    |                                                |
| products                 |                                                |
| product_fields           |                                                |
| product_variant_fields   |                                                |
| product_option_templates |                                                |
| product_variants         |                                                |
| purchase_orders          |                                                |
| purchase_order_items     |                                                |
| purchase_order_fields    |                                                |
| purchasing_cost_types    |                                                |
| purchasing_terms         |                                                |
| receipts                 |                                                |
| rmas                     |                                                |
| sales_orders             |                                                |
| sales_order_fields       |                                                |
| shipments                |                                                |
| shipment_items           |                                                |
| stores                   |                                                |
| vendors                  |                                                |


## List

```shell
curl http://your-subdomain.cohub.com/api/v1/companies
```

> The above command returns JSON structured like this:

```json
{
    "companies": [
        {
            "id": 1,
            "name": "Acme Inc.",
            "federal_employer_id": "123456789",
            "email_address": "jimmy@example.com",
            "phone_number": "555-555-5555",
            "fax_number": "555-555-5555",
            "starting_order_number": 1000,
            "tax_nexus": ["TN", "TX"],
            "url": "http://example.com",
            "timezone": "UTC",
            "receipt_bccs": ["jimmy@example.com", "orders@example.com"],
            "_links": {
                "self": "/api/v1/companies/1",
                "brands": "/api/v1/companies/1/brands",
                "blogs": "/api/v1/companies/1/blogs",
                "blog_categories": "/api/v1/companies/1/blog_categories",
                "box_sizes": "/api/v1/companies/1/box_sizes",
                "categories": "/api/v1/companies/1/categories",
                "cogs_categories": "/api/v1/companies/1/cogs_categories",
                "collections": "/api/v1/companies/1/collections",
                "collection_memberships": "/api/v1/companies/1/collection_memberships",
                "customers": "/api/v1/companies/1/customers",
                "customer_fields": "/api/v1/companies/1/customer_fields",
                "discounts": "/api/v1/companies/1/discounts",
                "inventories": "/api/v1/companies/1/inventories",
                "invoices": "/api/v1/companies/1/invoices",
                "inventory_transfers": "/api/v1/companies/1/inventory_transfers",
                "locations": "/api/v1/companies/1/locations",
                "logos": "/api/v1/companies/1/logos",
                "products": "/api/v1/companies/1/products",
                "product_fields": "/api/v1/companies/1/product_fields",
                "product_variant_fields": "/api/v1/companies/1/product_variant_fields",
                "product_option_templates": "/api/v1/companies/1/product_option_templates",
                "product_variants": "/api/v1/companies/1/product_variants",
                "purchase_orders": "/api/v1/companies/1/purchase_orders",
                "purchase_order_items": "/api/v1/companies/1/purchase_order_items",
                "purchase_order_fields": "/api/v1/companies/1/purchase_order_fields",
                "purchasing_cost_types": "/api/v1/companies/1/purchasing_cost_types",
                "purchasing_terms": "/api/v1/companies/1/purchasing_terms",
                "receipts": "/api/v1/companies/1/receipts",
                "rmas": "/api/v1/companies/1/rmas",
                "sales_orders": "/api/v1/companies/1/sales_orders",
                "sales_order_fields": "/api/v1/companies/1/sales_order_fields",
                "shipments": "/api/v1/companies/1/shipments",
                "shipment_items": "/api/v1/companies/1/shipment_items",
                "stores": "/api/v1/companies/1/stores",
                "vendors": "/api/v1/companies/1/vendors"
            },
            "address": {
                "id": 2046,
                "first_name": "Jimmy",
                "last_name": "Baker",
                "street": "1 Test Dr",
                "street_two": "Suite 1",
                "city": "Nashville",
                "state": "TN",
                "postal_code": "37211",
                "country_code": "US",
                "phone_number": "555-555-5555",
                "email_address": "jimmy@example.com",
                "company_name": "Acme Inc.",
                "created_at": "2015-06-04T22:21:24.201Z",
                "updated_at": "2015-06-04T22:21:24.201Z"
            },
            "logos": []
        },
        {
            "id": 2,
            "name": "Wolf and Sons",
            "federal_employer_id": "987654321",
            "email_address": "jimmy@example.com",
            "phone_number": "555-555-5555",
            "fax_number": "555-555-5555",
            "starting_order_number": 1000,
            "tax_nexus": ["CA", "AL"],
            "url": "http://example2.com/",
            "timezone": "UTC",
            "receipt_bccs": ["info@example2.com"],
            "_links": {
                "self": "/api/v1/companies/2",
                "brands": "/api/v1/companies/2/brands",
                "blogs": "/api/v1/companies/2/blogs",
                "blog_categories": "/api/v1/companies/2/blog_categories",
                "box_sizes": "/api/v1/companies/2/box_sizes",
                "categories": "/api/v1/companies/2/categories",
                "cogs_categories": "/api/v1/companies/2/cogs_categories",
                "collections": "/api/v1/companies/2/collections",
                "collection_memberships": "/api/v1/companies/2/collection_memberships",
                "customers": "/api/v1/companies/2/customers",
                "customer_fields": "/api/v1/companies/2/customer_fields",
                "discounts": "/api/v1/companies/2/discounts",
                "inventories": "/api/v1/companies/2/inventories",
                "invoices": "/api/v1/companies/2/invoices",
                "inventory_transfers": "/api/v1/companies/2/inventory_transfers",
                "locations": "/api/v1/companies/2/locations",
                "logos": "/api/v1/companies/2/logos",
                "products": "/api/v1/companies/2/products",
                "product_fields": "/api/v1/companies/2/product_fields",
                "product_variant_fields": "/api/v1/companies/2/product_variant_fields",
                "product_option_templates": "/api/v1/companies/2/product_option_templates",
                "product_variants": "/api/v1/companies/2/product_variants",
                "purchase_orders": "/api/v1/companies/2/purchase_orders",
                "purchase_order_items": "/api/v1/companies/2/purchase_order_items",
                "purchase_order_fields": "/api/v1/companies/2/purchase_order_fields",
                "purchasing_cost_types": "/api/v1/companies/2/purchasing_cost_types",
                "purchasing_terms": "/api/v1/companies/2/purchasing_terms",
                "receipts": "/api/v1/companies/2/receipts",
                "rmas": "/api/v1/companies/2/rmas",
                "sales_orders": "/api/v1/companies/2/sales_orders",
                "sales_order_fields": "/api/v1/companies/2/sales_order_fields",
                "shipments": "/api/v1/companies/2/shipments",
                "shipment_items": "/api/v1/companies/2/shipment_items",
                "stores": "/api/v1/companies/2/stores",
                "vendors": "/api/v1/companies/2/vendors"
            },
            "address": {
                "id": 2056,
                "first_name": "Jimmy",
                "last_name": "Baker",
                "street": "1 Test Dr",
                "street_two": "Suite 2",
                "city": "Nashville",
                "state": "TN",
                "postal_code": "37211",
                "country_code": "US",
                "phone_number": "555-555-5555",
                "email_address": "info@example.com",
                "company_name": "Wolf and Sons",
                "created_at": "2015-06-12T16:20:44.618Z",
                "updated_at": "2015-06-12T16:20:44.618Z"
            },
            "logos": []
        }
    ]
}
```

Lists all companies for the tenant

### HTTP Request

`GET http://your-subdomain.cohub.com/api/v1/companies`


## Show

```shell
curl http://your-subdomain.cohub.com/api/v1/companies/1
```

> The above command returns JSON structured like this:

```json
{
  "company": {
      "id": 1,
      "name": "Acme Inc.",
      "federal_employer_id": "123456789",
      "email_address": "jimmy@example.com",
      "phone_number": "555-555-5555",
      "fax_number": "555-555-5555",
      "starting_order_number": 1000,
      "tax_nexus": ["TN", "TX"],
      "url": "http://example.com",
      "timezone": "UTC",
      "receipt_bccs": ["jimmy@example.com", "orders@example.com"],
      "_links": {
          "self": "/api/v1/companies/1",
          "brands": "/api/v1/companies/1/brands",
          "blogs": "/api/v1/companies/1/blogs",
          "blog_categories": "/api/v1/companies/1/blog_categories",
          "box_sizes": "/api/v1/companies/1/box_sizes",
          "categories": "/api/v1/companies/1/categories",
          "cogs_categories": "/api/v1/companies/1/cogs_categories",
          "collections": "/api/v1/companies/1/collections",
          "collection_memberships": "/api/v1/companies/1/collection_memberships",
          "customers": "/api/v1/companies/1/customers",
          "customer_fields": "/api/v1/companies/1/customer_fields",
          "discounts": "/api/v1/companies/1/discounts",
          "inventories": "/api/v1/companies/1/inventories",
          "invoices": "/api/v1/companies/1/invoices",
          "inventory_transfers": "/api/v1/companies/1/inventory_transfers",
          "locations": "/api/v1/companies/1/locations",
          "logos": "/api/v1/companies/1/logos",
          "products": "/api/v1/companies/1/products",
          "product_fields": "/api/v1/companies/1/product_fields",
          "product_variant_fields": "/api/v1/companies/1/product_variant_fields",
          "product_option_templates": "/api/v1/companies/1/product_option_templates",
          "product_variants": "/api/v1/companies/1/product_variants",
          "purchase_orders": "/api/v1/companies/1/purchase_orders",
          "purchase_order_items": "/api/v1/companies/1/purchase_order_items",
          "purchase_order_fields": "/api/v1/companies/1/purchase_order_fields",
          "purchasing_cost_types": "/api/v1/companies/1/purchasing_cost_types",
          "purchasing_terms": "/api/v1/companies/1/purchasing_terms",
          "receipts": "/api/v1/companies/1/receipts",
          "rmas": "/api/v1/companies/1/rmas",
          "sales_orders": "/api/v1/companies/1/sales_orders",
          "sales_order_fields": "/api/v1/companies/1/sales_order_fields",
          "shipments": "/api/v1/companies/1/shipments",
          "shipment_items": "/api/v1/companies/1/shipment_items",
          "stores": "/api/v1/companies/1/stores",
          "vendors": "/api/v1/companies/1/vendors"
      },
      "address": {
          "id": 2046,
          "first_name": "Jimmy",
          "last_name": "Baker",
          "street": "1 Test Dr",
          "street_two": "Suite 1",
          "city": "Nashville",
          "state": "TN",
          "postal_code": "37211",
          "country_code": "US",
          "phone_number": "555-555-5555",
          "email_address": "jimmy@example.com",
          "company_name": "Acme Inc.",
          "created_at": "2015-06-04T22:21:24.201Z",
          "updated_at": "2015-06-04T22:21:24.201Z"
      },
      "logos": []
  }
}
```

Shows a specific company

### HTTP Request

`GET http://your-subdomain.cohub.com/api/v1/companies/1`
