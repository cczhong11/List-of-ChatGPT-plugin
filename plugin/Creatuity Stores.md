# Creatuity Stores

## Description for Model

Use plugin to search for products for given description in all on-line stores integrated with the plugin. Description may contain any product details such as name, brand, category, usage or any other data which describes ideal product matching user's needs. Description is the only required parameter and have to be provided as parameter called 'text'. Additionally you can specify product brands as 'brand' parameter or product categories as 'category' parameter to prioritize such products. Both 'brand' and 'category' parameters can be provided as space-separated list. If user provided a budged you can use 'min_price' or 'max_price' fields to get only products with price in given range. Prices must be in USD. As a reply, a product list will be provided. Every product on the list will contain obligatory name, description, price, currency code, image url and direct link to product in store. Optionally every product on the list may contain some other product-specific attributes like color, size, etc. To get suggested product list use /api/search endpoint. To get integrated with the plugin store list use /api/stores endpoint.

