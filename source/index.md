---
title: Cohub API Reference

language_tabs:
  - shell
  - ruby
  - python

toc_footers:
  - <a href='http://cohub.com'>Cohub.com</a>

includes:
  - v1/blogs
  - v1/box_sizes
  - v1/brands
  - v1/categories
  - v1/categorizations
  - v1/charges
  - v1/cogs_categories
  - v1/collections
  - v1/collection_memberships
  - v1/companies
  - v1/customers
  - v1/customer_fields
  - v1/purchase_orders
  - v1/sales_orders
  - v1/vendors
  - errors

search: true
---

# Introduction

This site details the core cohub.com API for which tenants can use to create, read, update and delete specific resources.

# API Hostname

Each tenant has their own subdomain which was specified upon creation of the account. This subdomain must be used when making API requests.

https://*YOUR_SUBDOMAIN*.cohub.com

When making API requests, each endpoint accepts and most require HTTPS.

# Authentication

```shell
curl -X POST https://bpl.cohub.com/api/v1/users/authenticate \
      -d 'email=jimmy@example.com' \
      -d 'password=mysecretpassword'
```

> The above command returns JSON structured like this:

```json
{
    "user": {
        "id": 1,
        "first_name": "Jimmy",
        "last_name": "Baker",
        "email": "jimmy@example.com",
        "created_at": "2015-05-29T17:18:52.790Z",
        "updated_at": "2015-05-29T17:18:52.790Z",
        "deleted_at": null,
        "admin": true,
        "otp_enabled": false,
        "api_key": "b59778b4c7bd9a418da312b07775a68a"
    }
}
```


The cohub.com API uses token based authentication. To get your api token, you will need to send a **POST** request containing your email and password to the following endpoint:

`POST https://your-subdomain.cohub.com/api/v1/users/authenticate`
